# Axiad Webflow Site Audit — Oct 6, 2026

Read-only audit of the main Axiad site via the Webflow MCP connector. Nothing was changed in Webflow.

## Site

- **Site:** Axiad (`67287422d51824fcbb67e68b`)
- **Last published:** Oct 2, 2026
- **Domains:** axiad.ai, www.axiad.ai, axiad.com, www.axiad.com, secuera.com, www.secuera.com
- **Also in workspace:** Federal Axiad (`689eef8430ed8538e43ea603`) — federal.axiad.com + 8 other domains. Not audited here.

## Summary

| | Count |
|---|---|
| Pages total | 98 |
| Static pages | 78 |
| CMS template pages | 20 |
| Draft pages | 6 |
| CMS collections | 20 |
| CMS items (approx.) | ~500 |
| Live pages missing meta description | 59 |
| Pages missing Open Graph (social share) image | 68 |

## Issues

### 1. Old/new page pairs still live

All of these are published. Once the transition is done, each "old" page should get a 301 redirect to its replacement and be removed, and "-new" pages should take over the clean slug.

- `/book-a-demo-old` / `/book-a-demo-new` (and `/request-a-demo`)
- `/axiad-conductor-old` / `/axiad-conductor-new`
- `/resources-center-old` / `/resources-center-new`
- `/axiad-confirm-old` (vs `/axiad-confirm`)
- `/about-us-old`
- `/axiad-mesh-old`
- `/contact-new` (vs `/contact-us`)

Draft only: `/solutions/identity-hygiene-needs-automation-old`

### 2. Temporary CMS collections

Each has 1 item and a live template page.

| Collection | Items | Template path |
|---|---|---|
| Insights-temps | 1 | `/insights-temp` |
| Events-temps | 1 | `/events-temps` |
| Blogs temps | 1 | `/blogs-temp` |
| Webinars-temps | 1 | `/webinars-temps` |

Check with the agency whether these are mid-migration or safe to delete.

### 3. Missing meta descriptions (live pages)

**High-priority marketing pages:**

- `/pricing`
- `/contact-us`
- `/request-a-demo`, `/book-a-demo-new`
- `/blog`, `/resources`, `/newsroom`, `/webinars-events`
- `/industries/public-sector` + `/vs-entrust`, `/procurement`, `/mandates`
- `/solutions/unify-identity-sprawl`
- `/solutions/quantify-identity-risk-in-dollars`
- `/solutions/govern-non-human-and-agentic-identities`
- `/federal-trust-center`, `/federal-post-quantum-readiness`
- `/axiad-foundation`, `/axiad-confirm`
- `/become-a-partner`, `/register-a-deal`, `/aws-marketplace-contact-axiad`

**Support / legal (lower priority):**

- `/support/submit-a-support-ticket`, `/support/report-security-incident`, `/axiad-technical-support`
- `/privacy-policy`, `/website-terms-and-conditions`, `/mobile-terms-and-conditions`
- `/axiad-eula`, `/axiad-cloud-terms-of-use`, `/axiad-cloud-sla`, `/axiad-cloud-reseller-agreement`
- `/software-subscription-agreement`, `/axiad-software-subscription-agreement`

**Utility (probably should be noindex instead):**

- `/search`, `/404`, `/thank-you-demo`, `/llm-info`
- `/customer-newsletter-pqc`, `/analyst-newsletter-pqc`

**CMS templates without a page-level description** (may be bound to a CMS field; spot-check):

Authors, Awards, Team, Featured Banners, Blog Categories, News Categories, Resources, Resources Categories, Resources Industries, Resources Usecases, Resources Audiences, Speakers, plus the 4 temp templates.

### 4. Duplicate SEO titles

- `Axiad - Trusted Identity. At the speed of now.` used on 2 pages (homepage + one other)
- 3 templates share a CMS-bound title (`meta-title-seo` field). Fine if each item fills that field; check for empty values.

### 5. Draft pages

- `/lottie` (Lottie Test)
- `/style-guide`
- `/trust` (Trust Center)
- `/news`
- `/solutions/mitigate-identity-risks`
- `/solutions/identity-hygiene-needs-automation-old`

Decide keep vs delete. `/style-guide` is worth keeping as an internal reference.

## CMS collections

| Collection | Items | Notes |
|---|---|---|
| Blogs | 185 | |
| News | 144 | |
| Resources | 41 | |
| Webinars & Events | 34 | |
| Authors | 15 | |
| Team | 15 | |
| Awards | 15 | |
| Blog Categories | 11 | |
| Landings | 8 | |
| Resources Categories | 7 | |
| Featured Banners | 7 | Has a public template page; likely shouldn't |
| Resources Industries | 5 | New Sept 2026 |
| Speakers | 4 | New Sept 2026 |
| News Categories | 2 | |
| Resources Usecases | 2 | New Sept 2026 |
| Resources Audiences | 2 | New Sept 2026 |
| Insights-temps | 1 | Temp |
| Events-temps | 1 | Temp |
| Blogs temps | 1 | Temp |
| Webinars-temps | 1 | Temp |

## Suggested next steps

1. Confirm with the agency which old/new pages and temp collections they will clean up before end of October.
2. Build a redirect map (old slug → new slug) for everything left over.
3. Write meta descriptions for the high-priority marketing pages first.
4. Set noindex on utility pages (search, 404, thank-you, newsletters, CMS-only templates like Featured Banners).
5. Add a default Open Graph image for pages without one.
6. Re-run this audit after the agency handoff and compare.
