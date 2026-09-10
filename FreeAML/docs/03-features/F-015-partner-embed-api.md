# F-015 — Partner embed / API

- **Status:** planned
- **Module:** Partner
- **Priority:** see feature-inventory.md

## Problem
Partners need embed/API without phone-sales GTM.

## Users
- Partner integrators

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Partner embeds widget or calls API → creates capability link → webhook callbacks

## Edge cases
API key abuse; no-phone GTM; rate limits

## Acceptance criteria
- [ ] Documented embed/API surface
- [ ] Creates capability codes ≥12 chars

## Out of scope
- White-label full theme engine (beyond BrandProvider)

## Analytics (no PII)
- partner_embed_loaded, partner_api_call (route + status)
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- Partner docs TODO
