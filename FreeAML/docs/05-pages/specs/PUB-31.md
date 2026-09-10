# PUB-31 — Vs FirstAML

- **Name:** Vs FirstAML
- **URL (freeze):** `/vs/firstaml`
- **Audience:** public
- **Purpose:** Competitive comparison vs FirstAML; convert to FreeAML (no remint competitor KYCs — R-009).

## Entry points
- SEO, /compare, sales enablement

## Actions
- **Primary:** Start FreeAML verification
- **Secondary:** Pricing, Pro

## Data shown
- Public comparison claims only

## Components used
- C-005, C-009, C-016, C-001/002

## Empty / loading / error / success
- Marketing states

## Analytics
- `vs_page_view` competitor=firstaml
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Frozen `/vs/firstaml`
- [ ] CTA to start check
- [ ] Does not promise reminting FirstAML history

## Security
- Honest comparison; R-009

## Related features / pages
- PUB-06, F-018

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
