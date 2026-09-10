# F-012 — Prepaid packs / invoice

- **Status:** planned
- **Module:** Payments
- **Priority:** see feature-inventory.md

## Problem
Institutions want prepaid credits or invoice instead of per-check card.

## Users
- Firm billing owners

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Firm buys pack or requests invoice → credits applied to orders → audit of draw-downs

## Edge cases
Insufficient credits; invoice unpaid; pack expiry TODO

## Acceptance criteria
- [ ] Pack purchase or invoice request path
- [ ] Credits applied atomically TODO

## Out of scope
- Complex usage-based enterprise contracts

## Analytics (no PII)
- pack_purchased, invoice_requested
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-02 pricing
