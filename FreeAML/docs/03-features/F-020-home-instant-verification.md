# F-020 — Home instant verification start (/)

- **Status:** live
- **Module:** Marketing/Core
- **Priority:** see feature-inventory.md

## Problem
Homepage must start verification instantly (make AML dead simple).

## Users
- Public DIY + firm visitors

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
`/` shows VerificationForm → user starts individual/business check immediately

## Edge cases
Form errors; SEO vs conversion balance; mobile

## Acceptance criteria
- [ ] `/` primary CTA starts verification
- [ ] Works without account

## Out of scope
- Firm dashboard (separate `/my`)

## Analytics (no PII)
- home_view, home_verification_start
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-01; C-003, C-008, C-009
