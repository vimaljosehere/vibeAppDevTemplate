# PUB-02 — Pricing

- **Name:** Pricing
- **URL (freeze):** `/pricing`
- **Audience:** public
- **Purpose:** Show check pricing and Pro markup story at high level.

## Entry points
- Nav, homepage CTA, SEO

## Actions
- **Primary:** Start check / go Pro
- **Secondary:** Compare, FAQ

## Data shown
- Public price cards; no account-specific fees in URL

## Components used
- C-004 PricingCards, C-005 FeatureComparison, C-006 ClientPaysCallout, C-001/002

## Empty / loading / error / success
- Standard marketing states; CTA success → form or /pro

## Analytics
- `pricing_view`, `pricing_cta_click`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Client-pays explained
- [ ] Markup described as on-order (not URL)
- [ ] CTAs work

## Security
- Public; no PII

## Related features / pages
- F-004, F-005, F-012, F-019

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
