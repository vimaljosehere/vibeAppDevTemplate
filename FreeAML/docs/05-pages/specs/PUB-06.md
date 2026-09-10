# PUB-06 — Compare

- **Name:** Compare
- **URL (freeze):** `/compare`
- **Audience:** public
- **Purpose:** Comparison content vs alternatives; convert to FreeAML.

## Entry points
- SEO, nav, vs pages

## Actions
- **Primary:** Start verification / see pricing
- **Secondary:** Read vs/easyaml, vs/firstaml

## Data shown
- Public comparison tables

## Components used
- C-005, C-009, C-016, C-001/002

## Empty / loading / error / success
- Marketing states only

## Analytics
- `compare_view`, `compare_cta`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] URL frozen
- [ ] CTA to VerificationForm or pricing

## Security
- Fair claims; no scraped competitor PII

## Related features / pages
- PUB-30, PUB-31, F-018

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
