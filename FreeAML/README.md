# FreeAML — Product Spec (AU)

Living build specification for **FreeAML** (`freeaml.com.au`): AUSTRAC Tranche 2 AML/KYC/KYB, client-pays checks, free compliance toolkit.

**Use this folder to:**
1. Strangler-rebuild `complyin30` module-by-module behind frozen public URLs
2. Clone/adapt for **NZ AML/CFT** (see `docs/14-locale/nz-adaptation.md`)

**Rules for editors:** keep each file short; prefer bullets; mark unknowns with `TODO:`; never invent production secrets.

## Doc map

| Folder | What it answers |
|---|---|
| `00-product` | What / why / goals |
| `01-users` | Who / roles |
| `02-architecture` | Sitemap / IA |
| `03-features` | Feature inventory |
| `04-flows` | End-to-end journeys |
| `05-pages` | Page inventory + template |
| `06-components` | UI building blocks |
| `07-design` | UX principles / tokens |
| `08-business-rules` | Hard product rules |
| `09-data` | Entities |
| `10-api` | Integrations |
| `11-technical` | Stack, strangler, security |
| `12-analytics` | Events (no PII) |
| `13-roadmap` | Module order + milestones |
| `14-locale` | AU ↔ NZ adaptation |
| `prompts/` | Agent build prompts |

Start here: `docs/00-product/product-overview.md` then `docs/13-roadmap/milestones.md`.
