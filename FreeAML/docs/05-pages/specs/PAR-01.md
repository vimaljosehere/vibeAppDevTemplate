# PAR-01 — Results by id

- **Name:** Results by id
- **URL (freeze):** `/results/[id]`
- **Audience:** party (auth preferred)
- **Purpose:** Order/verification results detail for the initiating party.

## Entry points
- Post-checkout, notifications, /my/verifications, /r upgrade

## Actions
- **Primary:** View status / download report (when F-014)
- **Secondary:** Share client link, retry notify

## Data shown
- **Auth:** status, outcomes allowed, short_code display (C-028), links
- **Anonymous/expired JWT:** public redacted payload only — no short_code, PII, Personr link (R-006/R-007)

## Components used
- C-025, C-026, C-028 (party-only), C-027 if unpaid

## Empty / loading / error / success
- Loading skeleton; 404; soft anonymous on expired JWT; success complete badge

## Analytics
- `results_viewed_auth`, `results_viewed_anonymous`, `jwt_expired_soft`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Auth vs anonymous payloads differ correctly
- [ ] Expired JWT does not hard-401 brick
- [ ] No Personr URL in ungated JSON

## Security
- R-006, R-007, R-012

## Related features / pages
- F-007, F-001, F-014

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
