# NZ AML/CFT adaptation

**Goal:** reuse this FreeAML spec + codebase patterns for NZ AML (teammate bot: NZ AML), not a fork-from-zero narrative.

## Swap checklist

| AU (FreeAML) | NZ (TODO fill) |
|---|---|
| AUSTRAC / Tranche 2 | AML/CFT Act regime / supervisor |
| ABN/ACN entity search | NZBN / Companies Office |
| Personr | TODO provider |
| freeaml.com.au copy / SEO | NZ domain + content |
| AUD Stripe | NZD Stripe |
| AU PEP/sanctions sources | NZ/local lists as required |

## Keep

- Client-pays + optional markup on order
- `/v/{code}` login-free client path
- Dead-simple OTP UX
- Strangler module map
- No-phone GTM preference
- Business rules R-001–R-012 (adapt legal refs only)

## Process

1. Copy `FreeAML/` → `NzAml/` (or twin folder) when starting NZ
2. Replace jurisdiction strings and providers via checklist
3. Do not claim AU compliance artefacts satisfy NZ obligations
