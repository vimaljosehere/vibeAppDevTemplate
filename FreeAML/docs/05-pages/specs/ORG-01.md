# ORG-01 — Create org

- **Name:** Create org
- **URL (freeze):** `/org/create`
- **Audience:** party / future firm owner
- **Purpose:** Create firm organisation workspace (Clerk later; lightweight today).

## Entry points
- Pro welcome, settings, CTA

## Actions
- **Primary:** Create organisation
- **Secondary:** Cancel

## Data shown
- Form fields for org profile; no other orgs listed

## Components used
- C-020, C-017, C-001/002

## Empty / loading / error / success
- Validation errors; success → /org/[code]

## Analytics
- `org_created`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Creates org record
- [ ] Redirects to ORG-02
- [ ] Does not affect `/v` auth model

## Security
- Auth required; R-008

## Related features / pages
- F-010; ORG-02, PUB-05

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
