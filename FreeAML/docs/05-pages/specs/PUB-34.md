# PUB-34 — Compliance docs

- **Name:** Compliance docs
- **URL (freeze):** `/compliance-docs`
- **Audience:** public
- **Purpose:** Document templates / compliance document library wedge.

## Entry points
- Compliance hub, SEO

## Actions
- **Primary:** View/download doc (as offered)
- **Secondary:** Start verification

## Data shown
- Public docs list/metadata

## Components used
- C-001/002, cards, C-016

## Empty / loading / error / success
- Empty library message; download errors

## Analytics
- `compliance_docs_view`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Reachable from hub
- [ ] URL frozen

## Security
- Public files only; no customer PII in samples

## Related features / pages
- F-009

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
