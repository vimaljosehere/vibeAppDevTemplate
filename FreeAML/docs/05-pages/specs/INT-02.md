# INT-02 — Internal

- **Name:** Internal
- **URL (freeze):** `/internal`
- **Audience:** internal
- **Purpose:** Internal utilities hub.

## Entry points
- Eng bookmark

## Actions
- **Primary:** TODO: clarify live purpose from complyin30
- **Secondary:** n/a

## Data shown
- TODO

## Components used
- TODO

## Empty / loading / error / success
- TODO

## Analytics
- Dev-only
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] **TODO:** document purpose from live codebase
- [ ] Not marketed

## Security
- Restrict access TODO

## Related features / pages
- INT-01


## Purpose
- **TODO:** Confirm what `/internal` does in live `complyin30` (ops tools, flags, etc.).

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
