# F-014 — PDF CDD report

- **Status:** planned
- **Module:** Reporting
- **Priority:** see feature-inventory.md

## Problem
Firms need downloadable CDD evidence packs.

## Users
- Party / firm staff

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Completed order → generate PDF CDD → download from results (auth)

## Edge cases
Incomplete order no PDF; regenerate versioning TODO

## Acceptance criteria
- [ ] PDF generates for completed CDD
- [ ] Auth-only download

## Out of scope
- Editable Word exports

## Analytics (no PII)
- cdd_pdf_generated, cdd_pdf_downloaded
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PAR-01, INT-01
