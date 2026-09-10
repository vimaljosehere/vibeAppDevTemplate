# F-016 — Ongoing monitoring

- **Status:** planned
- **Module:** Monitoring
- **Priority:** see feature-inventory.md

## Problem
Re-screen individuals/entities for sanctions/PEP/adverse media over time.

## Users
- Firm compliance owners

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Enroll completed subject → periodic rescreen → alert firm on hit

## Edge cases
False positives; alert fatigue; consent/retention TODO

## Acceptance criteria
- [ ] Enrollment API/UI stub
- [ ] Alert channel defined TODO

## Out of scope
- Transaction monitoring

## Analytics (no PII)
- monitoring_enrolled, monitoring_alert_raised
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PAR-03 future monitoring tab
