# F-001 — Individual KYC (Personr)

- **Status:** live
- **Module:** Core / Personr
- **Priority:** see feature-inventory.md

## Problem
SMEs need fast individual identity verification for AUSTRAC CDD without buying enterprise caseware.

## Users
- Party (firm staff or DIY customer); client completing IDV

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- **R-001:** Never mint Personr until order paid (402 if unpaid).
- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
Order paid → Personr mint → client `/v` → (planned `/continue`) → webhook complete → party results

## Edge cases
Unpaid mint attempt → 402; Personr downtime → retryable error; duplicate webhook idempotent

## Acceptance criteria
- [ ] Pay-before-mint enforced server-side
- [ ] Webhook updates status idempotently
- [ ] Party can view outcome when auth

## Out of scope
- Enterprise case management; reminting competitor KYCs (R-009)

## Analytics (no PII)
- verification_started, personr_session_minted (server), personr_outcome, verification_complete — no PII/OTP/docs
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- CLI-01, PAR-01, FLOW-001; C-003, C-025, C-027
