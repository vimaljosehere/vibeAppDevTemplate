# F-019 — Pro marketing + signup (/pro)

- **Status:** partial
- **Module:** Pro
- **Priority:** see feature-inventory.md

## Problem
Surface Pro markup value prop and signup path before full productization.

## Users
- Prospective Pro firms

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
`/pro` explains markup → `/pro/signup` → `/pro/welcome` onboarding

## Edge cases
Signup without Connect; welcome with incomplete onboarding

## Acceptance criteria
- [ ] `/pro`, `/pro/signup`, `/pro/welcome` exist
- [ ] Explains markup-on-order model

## Out of scope
- Full billing portal (later)

## Analytics (no PII)
- pro_page_view, pro_signup_started, pro_signup_complete
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-03–05; F-005
