# F-005 — Connect markup on order (Pro)

- **Status:** partial
- **Module:** Pro / Connect
- **Priority:** see feature-inventory.md

## Problem
Firms want optional service markup; fee must live on order, not /v URL.

## Users
- Pro firms with Connect

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-002/R-003:** Single Connect payout; markup on order at creation, never in `/v` URL.
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Pro firm sets markup on order create → client pays total → Connect single payout of net+markup to firm

## Edge cases
Markup without Connect onboarding; fee change after create forbidden; double transfer blocked (R-002)

## Acceptance criteria
- [ ] Markup stored on order at creation
- [ ] Not present in `/v` query
- [ ] Single Connect payout path

## Out of scope
- Multiple payout rails; URL-encoded fees

## Analytics (no PII)
- markup_configured, connect_payout_recorded — fee cents OK; no account numbers
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-03–05; ORG; C-004, C-005
