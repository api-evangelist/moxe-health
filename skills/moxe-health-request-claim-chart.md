---
name: Request a claim-supporting chart from Moxe Health
description: >-
  Initiate a claim-management request to retrieve the clinical chart supporting a specific claim
  (payment integrity / denials), then poll for status until Moxe delivers the chart via SFTP.
api: openapi/moxe-health-claim-management-initiate-openapi.json
operations:
- initiateClaimManagementRequest
- getClaimManagementRequestStatus
---

# Request a claim-supporting chart from Moxe Health

Use this skill to retrieve the clinical documentation that supports a specific claim — for payment
integrity, denial management, and claim adjudication. Access is partner-gated; credentials are issued
by Moxe during onboarding.

## Authenticate
1. Obtain an OAuth2 client-credentials bearer token (`grant_type=client_credentials` with your Moxe
   `client_id`, `client_secret`, `audience`). Tokens live 900 seconds — refresh before expiry.
2. Send both `Authentication: Bearer {access_token}` and `x-api-key: {api_key}` on every request.

## Initiate the request (`initiateClaimManagementRequest`)
- `POST /v1/claim-management-request` with the required body: `RequestId`, `SubscriberId`, `PatientId`,
  `PatientIdType`, `DateOfBirth`, `FirstName`, `LastName`, `AdministrativeGender`, `VisitId`,
  `PurposeOfUse`, `RequestSourceId`, `StartDate`, `EndDate`, `ClaimId`, `DenialRemarkCode`, and
  `ProviderOrganizationId`. Optional: `ProviderNpi`, `GroupNpi`, `TaxId`, `PatientAccountNumber`,
  `ProcedureCode`.
- A `202 Accepted` returns `data.moxeRequestId` and `data.links[]`.

## Poll for status (`getClaimManagementRequestStatus`)
- `GET /v1/claim-management-request/{moxeRequestId}/status`. Read `data.requestStatusCode`. A `404`
  means not found OR not authorized.

## Receive the chart
- Delivered out-of-band via **SFTP** to your predetermined location; not returned on the API.

## Rules and errors
- No idempotency key — do not blindly retry the initiate call (it creates a new request). Retry only
  on `429`/`500` with backoff. Error semantics match the chart-retrieval family; see
  `errors/moxe-health-problem-types.yml` and `conventions/moxe-health-conventions.yml`.
