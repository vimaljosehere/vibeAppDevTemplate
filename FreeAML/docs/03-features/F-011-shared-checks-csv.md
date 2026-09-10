# F-011 — Shared checks + CSV export

- **Status:** planned
- **Module:** Orgs
- **Priority:** see feature-inventory.md

## Problem
Teams need shared order lists and CSV for audits/pilots.

## Users
- Firm staff

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Staff opens shared verifications → filter → CSV export without PII in analytics

## Edge cases
Large CSV; permission denied for non-members; PII in file but not analytics

## Acceptance criteria
- [ ] Shared verification list for org members
- [ ] CSV export downloads
- [ ] Pilot gate documented

## Out of scope
- Realtime collaboration

## Analytics (no PII)
- shared_list_viewed, csv_exported — row counts, not names
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PAR-03/04
