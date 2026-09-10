# F-004 — Client-pays Stripe

- **Status:** live
- **Module:** Payments
- **Priority:** see feature-inventory.md

## Problem
Firms want clients to fund the check; Personr must not mint until paid.

## Users
- Client payer; firm that configures client-pays

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-001:** Never mint Personr until order paid (402 if unpaid).
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Unpaid client order → Stripe Checkout → webhook paid → then Personr mint allowed

## Edge cases
Abandoned checkout; double-pay race → idempotent paid; currency AUD only TODO confirm

## Acceptance criteria
- [ ] Checkout only when unpaid client-pays
- [ ] Webhook marks paid before mint
- [ ] ClientPaysCallout/PayCTA present

## Out of scope
- Non-AUD currencies until specified

## Analytics (no PII)
- checkout_started, checkout_paid (Stripe webhook truth) — amount band OK, no card data
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-01, FLOW-002; C-006, C-007, C-027
