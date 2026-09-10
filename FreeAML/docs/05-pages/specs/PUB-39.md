# PUB-39 — Risk assessment (redirect)

- **Name:** Risk assessment (redirect)
- **URL (freeze):** `/risk-assessment`
- **Audience:** public
- **Purpose:** Legacy/SEO path — **redirect** to live risk assessment experience.

## Entry points
- Old links, SEO

## Actions
- **Primary:** Follow redirect
- **Secondary:** n/a

## Data shown
- None (redirect)

## Components used
- Server redirect; destination may use C-014 RiskQuestionnaire

## Empty / loading / error / success
- Fixed redirect only

## Analytics
- `redirect_hit` path=/risk-assessment
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Redirects to live risk UI
- [ ] **TODO:** confirm exact target
- [ ] URL `/risk-assessment` frozen as alias

## Security
- Fixed target only

## Related features / pages
- F-009; C-014


## Redirect target
- **TODO:** Confirm exact production redirect target from live routes.

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
