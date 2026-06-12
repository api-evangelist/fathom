# Fathom Analytics (fathom)

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
