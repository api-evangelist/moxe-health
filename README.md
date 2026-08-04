# Moxe Health (moxe-health)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
