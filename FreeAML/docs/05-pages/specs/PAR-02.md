# PAR-02 — OTP login (/my)

- **Name:** OTP login (/my)
- **URL (freeze):** `/my`
- **Audience:** party
- **Purpose:** Passwordless OTP gate into party area (4-digit, durable rate limits).

## Entry points
- Direct, results unlock, emails

## Actions
- **Primary:** Request + submit 4-digit OTP
- **Secondary:** Resend OTP

## Data shown
- Email/phone input only; never show previous OTPs

## Components used
- C-024 OTP input, C-020 Input, C-017 Button

## Empty / loading / error / success
- Rate limited state; wrong code; success → /my/dashboard

## Analytics
- `otp_requested`, `otp_verified`, `otp_rate_limited` — never OTP value
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] OTP length = 4
- [ ] Durable rate limits across instances
- [ ] Secure RNG server-side (R-004)

## Security
- R-004; lockout messaging without account enumeration detail

## Related features / pages
- F-006; PAR-03+

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
