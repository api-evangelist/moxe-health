# Moxe Health (moxe-health)

Moxe Health is a United States healthcare data interoperability company, headquartered in Madison, Wisconsin, that operates the Clinical Data Clearinghouse for secure clinical data exchange between health plans (payers) and health systems (providers). Moxe's API-first platform ingests release-of-information (ROI) requests, searches connected electronic health records (EHRs) to extract the minimum-necessary contextual clinical data for a specified patient and date range, and securely delivers that data to the partner's system. Moxe is HIPAA and SOC 2 Type 2 compliant and was named #1 Best in KLAS for Payer-Provider Data Exchange.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/moxe-health/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/moxe-health/refs/heads/main/apis.yml)

## Tags

- Healthcare
- United States
- Interoperability
- Clinical Data
- Payer
- Provider
- EHR
- Health Data Exchange
- Claims
- Risk Adjustment

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## API Posture

Moxe's public developer portal documents a single REST **Chart Retrieval API** (OpenAPI 3.0.1, version 0.1.0) that segments into patient chart retrieval and claim management request families. It is REST/JSON — **not** HL7 FHIR: there is no FHIR CapabilityStatement (`/metadata`) and no SMART-on-FHIR `.well-known/smart-configuration`. Requests are initiated with member/subscriber identifiers plus patient demographics and a date-of-service range; Moxe searches connected EHRs and delivers the extracted chart to a predetermined SFTP location (the API returns `202 Accepted` plus a status endpoint). Authentication is **OAuth2 client-credentials** (Bearer access token) plus an **`x-api-key`** header, with credentials provisioned by Moxe to onboarded partners.

## APIs

### Moxe Health Chart Retrieval API

Initiate a patient chart request and check its status. Ingests a release-of-information request, searches connected EHRs for the specified patient and date-of-service range, and delivers the extracted clinical data to a predetermined SFTP location.

- **Human URL:** [https://developer.moxehealth.com/reference/overview](https://developer.moxehealth.com/reference/overview)
- **Base URL:** `https://int-api.moxehealth.com/chart-retrieval`

#### Properties

- [OpenAPI — Initiate Request](openapi/moxe-health-chart-retrieval-initiate-openapi.json)
- [OpenAPI — Get Status](openapi/moxe-health-chart-retrieval-status-openapi.json)
- [Documentation](https://developer.moxehealth.com/reference/overview)
- [API Reference — Initiate Request](https://developer.moxehealth.com/reference/initiatechartrequest)
- [API Reference — Get Status](https://developer.moxehealth.com/reference/getchartrequeststatus)
- [Authentication](https://developer.moxehealth.com/docs/authentication)

### Moxe Health Claim Management API

Initiate a claim management request and check its status. Retrieves the clinical chart supporting a specific claim, then delivers the extracted data to a predetermined location.

- **Human URL:** [https://developer.moxehealth.com/reference/overview](https://developer.moxehealth.com/reference/overview)
- **Base URL:** `https://int-api.moxehealth.com/chart-retrieval`

#### Properties

- [OpenAPI — Initiate Claim Request](openapi/moxe-health-claim-management-initiate-openapi.json)
- [OpenAPI — Get Claim Status](openapi/moxe-health-claim-management-status-openapi.json)
- [Documentation](https://developer.moxehealth.com/reference/overview)
- [API Reference — Initiate Claim Request](https://developer.moxehealth.com/reference/initiateclaimmanagementrequest)
- [API Reference — Get Claim Status](https://developer.moxehealth.com/reference/getclaimmanagementrequeststatus)
- [Authentication](https://developer.moxehealth.com/docs/authentication)

## Common Properties

- [Website](https://moxehealth.com/)
- [Developer Portal](https://developer.moxehealth.com/)
- [Documentation](https://developer.moxehealth.com/docs/getting-started)
- [Getting Started](https://developer.moxehealth.com/docs/getting-started)
- [API Reference](https://developer.moxehealth.com/reference/overview)
- [Authentication](https://developer.moxehealth.com/docs/authentication)
- [Sign Up / Login](https://developer.moxehealth.com/login)
- [GitHub Organization](https://github.com/moxehealth)
- [LinkedIn](https://www.linkedin.com/company/moxe-health)
- [Blog / Insights](https://moxehealth.com/insights)
- [Security](https://moxehealth.com/security/)
- [Privacy Policy](https://moxehealth.com/privacy-policy/)
- [Terms of Service](https://moxehealth.com/moxe-technology-governing-agreement/)
- [Support](https://moxehealth.com/contact/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
