---
name: Request a patient chart from Moxe Health
description: >-
  Initiate a release-of-information (ROI) request for a patient's clinical chart through the
  Moxe Health Chart Retrieval API, then poll for status until Moxe delivers the chart via SFTP.
api: openapi/moxe-health-chart-retrieval-initiate-openapi.json
operations:
- initiateChartRequest
- getChartRequestStatus
---

# Request a patient chart from Moxe Health

Use this skill to pull the minimum-necessary clinical chart for a member from a connected EHR
for risk adjustment, quality improvement, or care management. Access is partner-gated — Moxe
issues your OAuth2 client credentials and API key during onboarding.

## Authenticate
1. POST `grant_type=client_credentials` with your Moxe-issued `client_id`, `client_secret`, and
   `audience` to the Moxe token endpoint. You receive `access_token`, `token_type=Bearer`, and
   `expires_in=900` (15-minute lifetime — cache and refresh before expiry).
2. Send BOTH headers on every API call:
   - `Authentication: Bearer {access_token}` (note: the header is named `Authentication`, not `Authorization`)
   - `x-api-key: {api_key}`

## Initiate the request (`initiateChartRequest`)
- `POST /v1/patient-chart-request` with the required body fields: `RequestId` (your own correlation
  id — does not need to be unique), `MemberId`, `DateOfBirth`, `FirstName`, `LastName`,
  `AdministrativeGender`, `PurposeOfUse`, `RequestSourceId`, `StartDate`, `EndDate`, and
  `ProviderOrganizationId`. Optional demographics (address, `MiddleName`, `TIN`) sharpen EHR matching.
- Confirm the `PurposeOfUse` and `RequestSourceId` allowed values with your Moxe representative first.
- A `202 Accepted` returns `data.moxeRequestId` (Moxe's unique id) and `data.links[]` (status links).

## Poll for status (`getChartRequestStatus`)
- `GET /v1/patient-chart-request/{moxeRequestId}/status`. Read `data.requestStatusCode` and
  `data.requestStatusDescription`. A `404` means the request does not exist OR you are not
  authorized to view it.

## Receive the chart
- The extracted chart is NOT returned on the API. Moxe delivers it out-of-band via **SFTP** to your
  predetermined location once processing completes.

## Rules and errors
- Idempotency: there is none. `RequestId` is not an idempotency key, so avoid blind retries of
  `initiateChartRequest` — a retry creates a new request. Retry only on `429`/`500` with backoff.
- Errors are bare HTTP statuses: `400` invalid input, `401` reauthenticate (refresh the 15-min token),
  `403` missing scope, `429` global rate limit (no published numbers), `500` server error. See
  `errors/moxe-health-problem-types.yml`.
