# F-003 — Client capability links /v/{code}

- **Status:** live
- **Module:** Core
- **Priority:** see feature-inventory.md

## Problem
Clients must complete verification without firm login or accounts.

## Users
- End clients receiving capability links

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-005:** New short codes ≥12 chars; legacy codes still resolve.
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Client opens `/v/{code}` → sees status + next step → pay or continue IDV → done

## Edge cases
Invalid/expired code → generic error; enumeration rate-limited; legacy short codes still work

## Acceptance criteria
- [ ] Resolves ≥12-char and legacy codes
- [ ] Login-free
- [ ] No raw Personr URL in page/JSON

## Out of scope
- Firm Clerk auth on `/v`

## Analytics (no PII)
- capability_link_opened, capability_next_step_clicked — code length class only, not raw code
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-01; C-026, C-027, C-028 (party-only)
