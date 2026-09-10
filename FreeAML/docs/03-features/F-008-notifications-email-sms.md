# F-008 — Notifications email/SMS

- **Status:** partial
- **Module:** Notifications
- **Priority:** see feature-inventory.md

## Problem
Users need reliable email/SMS for links, OTP, and completion.

## Users
- Party + client

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Trigger event → Resend/Twilio send → delivery logged; retry on transient fail

## Edge cases
Provider outage; bounce/complaint; do not put OTP in analytics

## Acceptance criteria
- [ ] Email and SMS paths exist for OTP/links
- [ ] Failures logged without message body PII in analytics

## Out of scope
- Push/WhatsApp until specified

## Analytics (no PII)
- notify_email_queued, notify_sms_queued, notify_delivered/failed (provider ids only)
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- All client/party flows
