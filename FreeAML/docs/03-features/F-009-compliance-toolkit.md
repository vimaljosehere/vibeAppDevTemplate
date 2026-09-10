# F-009 — Compliance toolkit

- **Status:** live
- **Module:** Toolkit / SEO
- **Priority:** see feature-inventory.md

## Problem
Tranche 2 SMEs need free program/risk/training/docs as SEO wedge and utility.

## Users
- Public + logged-in party

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Visitor uses `/compliance` hub → program/risk/training/docs → CTA into VerificationForm

## Edge cases
Redirect pages `/program`, `/risk-assessment` must keep SEO targets

## Acceptance criteria
- [ ] Compliance hub + docs/training/reports reachable
- [ ] CTAs use VerificationForm pattern
- [ ] URLs frozen

## Out of scope
- Paid consulting delivery

## Analytics (no PII)
- toolkit_page_view, toolkit_cta_click, training_module_complete
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-33–39; C-014, C-023
