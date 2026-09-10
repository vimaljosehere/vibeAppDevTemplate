# F-010 — Firm orgs (Clerk planned; today /org, /my/team)

- **Status:** partial
- **Module:** Orgs
- **Priority:** see feature-inventory.md

## Problem
Multi-user firms need shared workspace; Clerk later, lightweight org today.

## Users
- Firm owners/admins/staff

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Owner creates `/org/create` → invite team via `/my/team` → shared context (Clerk later)

## Edge cases
Org isolation (R-008); no org data on `/v`; Clerk migration later

## Acceptance criteria
- [ ] `/org/create` and `/org/[code]` work
- [ ] `/my/team` lists members
- [ ] No firm auth required on `/v`

## Out of scope
- Full RBAC until Clerk module

## Analytics (no PII)
- org_created, team_member_invited — orgId only when Clerk lands
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- ORG-01/02, PAR-08
