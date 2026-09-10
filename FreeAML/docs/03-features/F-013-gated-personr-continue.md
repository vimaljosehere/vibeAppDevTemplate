# F-013 — Gated Personr /continue

- **Status:** planned
- **Module:** Personr / M1b
- **Priority:** see feature-inventory.md

## Problem
Raw Personr URLs must never appear in UI/JSON; server-gated redirect required.

## Users
- Clients continuing IDV

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Never expose raw Personr URL in UI, JSON, or analytics; `/continue` is the only client entry to provider.
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Paid+eligible client hits `/continue` → server validates → 302 to Personr; UI never shows provider URL

## Edge cases
Unpaid → deny; wrong code → generic; already complete → status page

## Acceptance criteria
- [ ] `/continue` validates eligibility server-side
- [ ] 302 to Personr only when allowed
- [ ] UI never renders provider URL

## Out of scope
- Client-side Personr URL construction

## Analytics (no PII)
- continue_redirect_ok, continue_denied_unpaid/unauthorized
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-02; security: no Personr URL
