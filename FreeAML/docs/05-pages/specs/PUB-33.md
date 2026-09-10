# PUB-33 — Compliance hub

- **Name:** Compliance hub
- **URL (freeze):** `/compliance`
- **Audience:** public (+ party deep links)
- **Purpose:** Hub for free compliance toolkit: program, risk, training, docs.

## Entry points
- Nav, SEO, my/compliance

## Actions
- **Primary:** Open toolkit section
- **Secondary:** Start verification CTA

## Data shown
- Public toolkit navigation; auth may unlock saves TODO

## Components used
- C-014 RiskQuestionnaire (linked), C-023, C-016, C-001/002

## Empty / loading / error / success
- Empty sections OK with CTA

## Analytics
- `compliance_hub_view`, `toolkit_nav_click`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Links to docs/training/reports and redirects
- [ ] URLs frozen
- [ ] CTA to VerificationForm

## Security
- Public content; no secrets

## Related features / pages
- F-009; PUB-34–39

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
