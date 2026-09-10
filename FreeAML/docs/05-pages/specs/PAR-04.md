# PAR-04 — My verifications

- **Name:** My verifications
- **URL (freeze):** `/my/verifications`
- **Audience:** party (OTP session)
- **Purpose:** List party's verifications; future shared/CSV (F-011).

## Entry points
- After /my OTP; nav within /my/*

## Actions
- **Primary:** Open verification / export CSV when live
- **Secondary:** Back to dashboard / logout TODO

## Data shown
- Auth party data only; org-scoped when org exists (R-008)

## Components used
- C-001 app nav variant, C-025, tables/cards, C-021 Skeleton

## Empty / loading / error / success
- Empty lists; loading skeletons; error toasts; success saves

## Analytics
- `my_section_view` section=/my/verifications
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Requires OTP session
- [ ] URL `/my/verifications`
- [ ] No data bleed across parties/orgs

## Security
- Session auth; R-008 isolation on team/org views

## Related features / pages
- F-006, F-010, F-011; PAR-02

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
