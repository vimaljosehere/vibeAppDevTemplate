# PUB-40 — Components kitchen sink

- **Name:** Components kitchen sink
- **URL (freeze):** `/components`
- **Audience:** internal / eng
- **Purpose:** Internal design kitchen sink for UI primitives — **low priority**.

## Entry points
- Eng bookmark only; not marketed

## Actions
- **Primary:** Visual QA of UI kit
- **Secondary:** n/a

## Data shown
- Demo states of C-017–C-022 etc.

## Components used
- All UI primitives

## Empty / loading / error / success
- N/A product states

## Analytics
- Optional `dev_components_view` — disable in prod analytics if noisy
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Not linked in public nav
- [ ] Low priority; may be prod-gated TODO

## Security
- Should not expose secrets; consider non-index / auth in prod TODO

## Related features / pages
- C-017–C-022

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
