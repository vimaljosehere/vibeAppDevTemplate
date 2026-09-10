# F-002 — Business KYB + UBO chain

- **Status:** live
- **Module:** Core / Personr
- **Priority:** see feature-inventory.md

## Problem
Business entities require KYB plus beneficial-owner capture and screening.

## Users
- Party initiating business check; UBOs via /u/{code}

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-001:** Never mint Personr until order paid (402 if unpaid).
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Business order → entity search → pay → directors/UBOs invited via `/u` → chain complete → party results

## Edge cases
Entity not found; UBO declines; partial chain; trust structures TODO

## Acceptance criteria
- [ ] ABN/ACN path creates business order
- [ ] UBO links issued as `/u/{code}`
- [ ] Chain status visible to party

## Out of scope
- Full trust/SMSF edge cases until specified

## Analytics (no PII)
- kyb_started, ubo_link_sent, ubo_complete, kyb_complete — entity type only, no ABN in analytics if sensitive TODO
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-01, CLI-03, FLOW business; C-029, C-030
