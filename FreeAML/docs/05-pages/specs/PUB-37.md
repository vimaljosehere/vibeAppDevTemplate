# PUB-37 — Training module

- **Name:** Training module
- **URL (freeze):** `/training/[moduleId]`
- **Audience:** public
- **Purpose:** Single training module content + completion tracking light-touch.

## Entry points
- From /training

## Actions
- **Primary:** Complete module / continue
- **Secondary:** Next module, verification CTA

## Data shown
- Public module content; completion may be local/auth TODO

## Components used
- C-001/002, progress UI TODO

## Empty / loading / error / success
- 404 unknown moduleId; success = module complete event

## Analytics
- `training_module_view`, `training_module_complete` (moduleId only)
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Valid moduleId renders
- [ ] Invalid → safe 404
- [ ] Parent URL pattern frozen

## Security
- No PII in completion analytics

## Related features / pages
- F-009; PUB-36

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
