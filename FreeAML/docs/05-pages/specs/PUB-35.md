# PUB-35 — Reports

- **Name:** Reports
- **URL (freeze):** `/reports`
- **Audience:** public / party
- **Purpose:** Reporting entry for toolkit / CDD report education (PDF feature F-014 planned).

## Entry points
- Hub, SEO, results CTA later

## Actions
- **Primary:** Learn / request report path
- **Secondary:** Start verification

## Data shown
- Public explanatory; auth reports TODO when F-014 ships

## Components used
- C-001/002, C-009

## Empty / loading / error / success
- TODO auth-gated list when live

## Analytics
- `reports_page_view`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] URL frozen
- [ ] Does not leak other orgs' reports

## Security
- Auth boundaries when reports list exists

## Related features / pages
- F-014, F-009

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
