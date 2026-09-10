# ORG-02 — Org home

- **Name:** Org home
- **URL (freeze):** `/org/[code]`
- **Audience:** org members
- **Purpose:** Organisation landing / context switch for firm code.

## Entry points
- After create, invites, bookmarks

## Actions
- **Primary:** Open team / verifications
- **Secondary:** Settings

## Data shown
- Org-scoped summary only for members

## Components used
- C-025, cards, C-001

## Empty / loading / error / success
- 404/forbidden for outsiders; loading

## Analytics
- `org_home_view`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Members only
- [ ] Isolation enforced
- [ ] Firm auth separate from public `/v`

## Security
- R-008

## Related features / pages
- F-010; PAR-08

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
