# PUB-32 — Sixstep

- **Name:** Sixstep
- **URL (freeze):** `/sixstep`
- **Audience:** public
- **Purpose:** Educational six-step AML journey content + convert.

## Entry points
- SEO, toolkit

## Actions
- **Primary:** Start verification / open toolkit
- **Secondary:** Related compliance pages

## Data shown
- Public educational content

## Components used
- C-008 HowItWorks, C-009, C-023 FAQ, C-001/002

## Empty / loading / error / success
- Marketing states

## Analytics
- `sixstep_view`, `sixstep_cta`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] URL frozen
- [ ] Clear next step into product

## Security
- Public

## Related features / pages
- F-009, F-018

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
