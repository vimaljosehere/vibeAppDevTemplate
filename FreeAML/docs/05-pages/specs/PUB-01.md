# PUB-01 — Homepage

- **Name:** Homepage
- **URL (freeze):** `/`
- **Audience:** public
- **Purpose:** Instant verification start + value prop: make AML dead simple.

## Entry points
- Direct nav, ads, SEO brand, internal CTAs

## Actions
- **Primary:** Start verification (VerificationForm)
- **Secondary:** Pricing, Pro, toolkit, trust

## Data shown
- Public marketing + form fields user enters (not logged)
- No firm auth required

## Components used
- C-001 Navbar, C-002 Footer, C-003 VerificationForm, C-008 HowItWorks, C-009 CTA, C-010 TrustBadges, C-011 SEO

## Empty / loading / error / success
- Loading: form idle
- Error: validation / API fail messages
- Success: navigate to pay or capability path

## Analytics
- `home_view`, `home_verification_start`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] VerificationForm is primary above-the-fold path
- [ ] Works without account
- [ ] SEO structured data present

## Security
- Public; HTTPS; no secrets in client

## Related features / pages
- F-020, F-018; PUB-02, PUB-03

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
