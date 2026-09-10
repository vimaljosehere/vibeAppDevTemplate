# F-017 — UBO capture via /u/{code}

- **Status:** live
- **Module:** Core
- **Priority:** see feature-inventory.md

## Problem
Beneficial owners need a dedicated login-free capture link separate from /v.

## Users
- UBO individuals

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
UBO opens `/u/{code}` → confirms details → completes capture → parent KYB updates

## Edge cases
Wrong recipient; code reuse; incomplete UBO set blocks KYB complete

## Acceptance criteria
- [ ] `/u/{code}` login-free capture
- [ ] Updates parent order UBO state

## Out of scope
- UBO on `/v` primary path

## Analytics (no PII)
- ubo_page_opened, ubo_submitted
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-03; C-030
