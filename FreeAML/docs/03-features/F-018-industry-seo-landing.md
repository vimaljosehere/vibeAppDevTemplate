# F-018 — Industry/SEO landing conversion

- **Status:** live
- **Module:** Marketing/SEO
- **Priority:** see feature-inventory.md

## Problem
SEO landings must convert via VerificationForm without renaming frozen URLs.

## Users
- Public visitors from search

## Behaviour
- Aligns to tagline: **make AML dead simple**.
- Stack touchpoints: Next.js / Vercel / Supabase / Stripe+Connect / Personr / Resend / Twilio as relevant.

- Firm auth (Clerk) is separate from public `/v` — never require firm login for capability links.

## Happy path
SEO landing → VerificationForm → order/checkout path without URL rename

## Edge cases
Form validation; bot spam; freeze URL if content changes

## Acceptance criteria
- [ ] Each SEO landing hosts VerificationForm or CTA
- [ ] Unique intent/keywords preserved
- [ ] URLs not renamed

## Out of scope
- URL renames during strangler

## Analytics (no PII)
- seo_landing_view, verification_form_submit (landing_slug)
- Never: OTPs, ID docs, Personr payloads, raw capability URLs (R-012).

## Security notes
- Enforce server-side; do not trust client for paid/mint/OTP.
- Rate-limit enumeration on codes and OTP.
- Org isolation when firm accounts exist (R-008).

## Related pages / flows
- PUB-08–29; C-003, C-023
