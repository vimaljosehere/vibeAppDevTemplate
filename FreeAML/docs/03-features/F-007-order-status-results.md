# F-007 — Order status / results (/results, /r)

- **Status:** live
- **Module:** Core
- **Priority:** see feature-inventory.md

## Problem
Parties and clients need status without leaking short_code/PII/Personr links ungated.

## Users
- Party (auth); anonymous viewers of public status

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-006/R-007:** Ungated payload redacts short_code/PII/Personr link; expired JWT → anonymous public, not hard 401.
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Auth party opens `/results/[id]` with full detail; anonymous/expired sees redacted public status

## Edge cases
Expired JWT soft-degrade; ungated must omit short_code/PII/Personr; `/r` alias if present

## Acceptance criteria
- [ ] Auth results show allowed detail
- [ ] Ungated omits short_code/PII/Personr link
- [ ] Expired JWT → anonymous payload

## Out of scope
- Exposing Personr links ungated

## Analytics (no PII)
- results_viewed_auth, results_viewed_anonymous, jwt_expired_soft
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PAR-01, CLI-04; C-025, C-026
