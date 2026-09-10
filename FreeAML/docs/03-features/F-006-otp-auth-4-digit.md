# F-006 — OTP auth 4-digit

- **Status:** live
- **Module:** Auth
- **Priority:** see feature-inventory.md

## Problem
Parties need passwordless access to their orders without Clerk yet.

## Users
- Party owners of orders

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-004:** 4-digit OTP via secure RNG; durable attempt/rate limits.
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Party enters email/phone → 4-digit OTP → durable rate limit → session to `/my/*`

## Edge cases
Wrong OTP; lockout after durable limit; SMS/email delivery fail; clock skew

## Acceptance criteria
- [ ] OTP exactly 4 digits
- [ ] Durable rate limits persist across instances
- [ ] Success lands in `/my` area

## Out of scope
- Password auth; Clerk (separate)

## Analytics (no PII)
- otp_requested, otp_verified, otp_rate_limited — never OTP value
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PAR-02; C-024
