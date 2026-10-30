# Moxe Health

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Moxe Health is a United States healthcare data interoperability company, headquartered in Madison, Wisconsin, that operates the Clinical Data Clearinghouse for secure clinical data exchange between health plans (payers) and health systems (providers). Moxe's API-first platform ingests release-of-information (ROI) requests, searches connected electronic health records (EHRs) to extract the minimum-necessary contextual clinical data for a specified patient and date range, and securely delivers that data to the partner's system. Its Chart Retrieval API supports risk adjustment, quality improvement, claim management, payment integrity, care management, and forecasting use cases. The public developer portal documents a REST (OpenAPI 3.0.1) Chart Retrieval API secured with OAuth2 client-credentials plus an x-api-key header; retrieved charts are returned to a predetermined location via SFTP. Moxe is HIPAA and SOC 2 Type 2 compliant and was named number 1 Best in KLAS for Payer-Provider Data Exchange. The documented API is REST/JSON rather than HL7 FHIR, and full access is granted through a partner onboarding agreement.

**Areas:** Healthcare · United States · Interoperability · Clinical Data · Payers · Providers · Electronic Health Records · Health Data Exchange · Claims · Risk Adjustment

## Moxe Health on APIs.io

Everything profiled for Moxe Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/moxe-health/](https://apis.io/providers/moxe-health/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Moxe Health Claims API](https://apis.io/apis/moxe-health/moxe-health-claims-api/) — The Claims API from Moxe Health — 2 operation(s) for claims.
- [Moxe Health Patient API](https://apis.io/apis/moxe-health/moxe-health-patient-api/) — The Patient API from Moxe Health — 2 operation(s) for patient.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [Request a claim-supporting chart and poll for status](https://apis.io/arazzos/moxe-health/moxe-health-request-claim-chart/)
- [Request a patient chart and poll for status](https://apis.io/arazzos/moxe-health/moxe-health-request-patient-chart/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [moxe-health](https://apis.io/servers/moxe-health/moxe-health/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Moxe Health Agentic Access](https://apis.io/agentic-access/moxe-health/moxe-health-agentic-access/)

#### Collections (4)

Postman and Open Collection request collections.

- [Chart Retrieval API](https://apis.io/collections/moxe-health/open-moxe-health-chart-retrieval-initiate/)
- [Chart Retrieval API](https://apis.io/collections/moxe-health/open-moxe-health-chart-retrieval-status/)
- [Chart Retrieval API](https://apis.io/collections/moxe-health/open-moxe-health-claim-management-initiate/)
- [Chart Retrieval API](https://apis.io/collections/moxe-health/open-moxe-health-claim-management-status/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Moxe Health Chart Retrieval Initiate Overlay](https://apis.io/overlays/moxe-health/moxe-health-chart-retrieval-initiate-overlay/)
- [Moxe Health Chart Retrieval Status Overlay](https://apis.io/overlays/moxe-health/moxe-health-chart-retrieval-status-overlay/)
- [Moxe Health Claim Management Initiate Overlay](https://apis.io/overlays/moxe-health/moxe-health-claim-management-initiate-overlay/)
- [Moxe Health Claim Management Status Overlay](https://apis.io/overlays/moxe-health/moxe-health-claim-management-status-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Moxe Health Authentication](https://apis.io/security/moxe-health/moxe-health-authentication/)
- [Moxe Health Domain Security](https://apis.io/security/moxe-health/moxe-health-domain-security/)
- [Moxe Health Trust Center](https://apis.io/security/moxe-health/moxe-health-trust-center/)
- [Moxe Health Vulnerability Disclosure](https://apis.io/security/moxe-health/moxe-health-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Moxe Health Scopes](https://apis.io/scopes/moxe-health/moxe-health-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Moxe Health Plans Pricing](https://apis.io/plans/moxe-health/moxe-health-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Moxe Health Rate Limits](https://apis.io/rate-limits/moxe-health/moxe-health-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://moxehealth.com/)
- [Documentation](https://developer.moxehealth.com/docs/getting-started)
- [Getting started](https://developer.moxehealth.com/docs/getting-started)
- [API reference](https://developer.moxehealth.com/reference/overview)
- [Sign up](https://developer.moxehealth.com/login)
- [Support](https://moxehealth.com/contact/)
- [Blog](https://moxehealth.com/insights)
- [Security](https://moxehealth.com/security/)
- [Compliance](https://moxehealth.com/security/)
- [Terms of service](https://moxehealth.com/moxe-technology-governing-agreement/)
- [Privacy policy](https://moxehealth.com/privacy-policy/)
- [GitHub](https://github.com/moxehealth)

## API Evangelist rating

**Kin Score 43.6** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 47.8 |
| Contract governance | 18.2 |
| Operational transparency | 13.2 |
| Developer ergonomics | 33.9 |
| Access clarity | 43.4 |

**Agent readiness 25.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 46.1** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/moxe-health/](https://apis.io/providers/moxe-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Moxe Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/moxe-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
