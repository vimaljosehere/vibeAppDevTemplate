# INT-01 — Test PDFs

- **Name:** Test PDFs
- **URL (freeze):** `/testpdfs`
- **Audience:** internal
- **Purpose:** Internal PDF generation / CDD PDF test harness.

## Entry points
- Eng only

## Actions
- **Primary:** Generate/test PDF
- **Secondary:** n/a

## Data shown
- Sample/fixture data only

## Components used
- PDF viewer/download

## Empty / loading / error / success
- Error on generate fail

## Analytics
- Optional dev-only analytics
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Not in public nav
- [ ] Supports F-014 bring-up
- [ ] No production customer PII in fixtures

## Security
- Lock down in production TODO (auth or non-index)

## Related features / pages
- F-014

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
