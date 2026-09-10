# PUB-36 — Training index

- **Name:** Training index
- **URL (freeze):** `/training`
- **Audience:** public
- **Purpose:** AML training modules index (SEO + toolkit).

## Entry points
- Hub, SEO

## Actions
- **Primary:** Open module
- **Secondary:** Start verification CTA

## Data shown
- Public module list

## Components used
- C-001/002, cards, C-016

## Empty / loading / error / success
- Empty: no modules; loading skeletons

## Analytics
- `training_index_view`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Lists modules linking to `/training/[moduleId]`
- [ ] URL frozen

## Security
- Public

## Related features / pages
- F-009; PUB-37

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
