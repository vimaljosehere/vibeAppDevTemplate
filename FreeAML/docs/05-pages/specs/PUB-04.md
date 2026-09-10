# PUB-04 — Pro signup

- **Name:** Pro signup
- **URL (freeze):** `/pro/signup`
- **Audience:** public / prospective Pro firm
- **Purpose:** Capture Pro firm signup

## Entry points
- From /pro funnel, pricing, nav
- Unique intent: Capture Pro firm signup

## Actions
- **Primary:** Submit signup
- **Secondary:** Back to pricing / home

## Data shown
- Public marketing; signup fields only on PUB-04
- Welcome may show soft auth state TODO

## Components used
- C-001/002, C-004/005, C-009; signup form on PUB-04

## Empty / loading / error / success
- Loading/error on signup; success → /pro/welcome

## Analytics
- `pro_funnel` with step=PUB-04
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] URL frozen `/pro/signup`
- [ ] Explains markup on **order** not `/v`
- [ ] Single Connect payout messaging
- [ ] Keywords/intent: pro signup

## Security
- No Personr URLs; protect signup against spam

## Related features / pages
- F-005, F-019; PUB-02

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
