# Fathom Analytics (fathom)

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

Fathom Analytics is a privacy-first website analytics platform that provides GDPR-compliant, cookie-free analytics as a simple and accurate alternative to Google Analytics. The platform serves thousands of companies, including Fortune 100 enterprises and government agencies, without tracking personally identifiable information. Fathom exposes a REST API at `https://api.usefathom.com/v1` that enables developers to manage sites, events, and milestones, generate flexible aggregation reports, and retrieve real-time visitor counts — all authenticated via Bearer token API keys with configurable permissions.

APIs.json: [https://raw.githubusercontent.com/api-evangelist/fathom/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fathom/refs/heads/main/apis.yml)

Naftiko: [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=fathom-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=fathom-api-evangelist&utm_content=repo)

## Tags

- Analytics
- Privacy
- GDPR
- Website Analytics
- Cookieless
- Page Views
- Events
- Reporting

## APIs

### Fathom Analytics REST API

The Fathom Analytics REST API provides programmatic access to account data, sites, events, milestones, aggregation reports, and real-time current visitor counts. All requests authenticate via Bearer token and use cursor-based pagination (using `starting_after` and `ending_before` parameters with limits of 1–100 results per request).

- **Base URL:** `https://api.usefathom.com/v1`
- **Authentication:** Bearer token (API keys generated at https://app.usefathom.com/api)
- **Documentation:** https://usefathom.com/api

**Endpoints:**
- `GET /account` — Retrieve account information
- `GET /sites`, `GET /sites/{site_id}`, `POST /sites`, `POST /sites/{site_id}`, `DELETE /sites/{site_id}` — Site management
- `GET /sites/{site_id}/events`, `POST /sites/{site_id}/events`, etc. — Event management
- `GET /sites/{site_id}/milestones`, `POST /sites/{site_id}/milestones`, etc. — Milestone management
- `GET /aggregations` — Generate custom aggregation reports
- `GET /current_visitors` — Real-time visitor counts

## Plans / Rate Limits / FinOps

- **Plans & Pricing:** [plans/fathom-plans-pricing.yml](plans/fathom-plans-pricing.yml) — Tiered paid subscriptions from $15/month (100K pageviews) to enterprise custom pricing (25M+ pageviews); 17% savings with annual billing; 7-day free trial; all plans include API access and up to 50 sites.
- **Rate Limits:** [rate-limits/fathom-rate-limits.yml](rate-limits/fathom-rate-limits.yml) — 2,000 requests/hour for site and event management endpoints; 10 requests/minute for aggregation and current_visitors reporting endpoints; 429 status code on throttle.
- **FinOps:** [finops/fathom-finops.yml](finops/fathom-finops.yml) — Subscription billing model; metered by monthly pageview volume; annual billing discount; API requests count against pageview quota.

## Timestamps

- **Created:** 2026-06-12
- **Modified:** 2026-06-12

## Common Properties

| Type | URL |
|------|-----|
| Website | https://usefathom.com/ |
| Documentation | https://usefathom.com/docs |
| API Documentation | https://usefathom.com/api |
| Blog | https://usefathom.com/blog |
| Blog Feed | https://usefathom.com/blog/feed.xml |
| Changelog | https://usefathom.com/changelog |
| Changelog Feed | https://usefathom.com/changelog/feed.xml |
| Pricing | https://usefathom.com/pricing |
| Status Page | https://status.usefathom.com/ |
| GitHub Organization | https://github.com/usefathom |
| X / Twitter | https://twitter.com/usefathom |
| LinkedIn | https://www.linkedin.com/company/fathom-analytics |

## Maintainers

- **Kin Lane** — kin@apievangelist.com
