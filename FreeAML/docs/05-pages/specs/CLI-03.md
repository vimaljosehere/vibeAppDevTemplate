# CLI-03 — UBO capture

- **Name:** UBO capture
- **URL (freeze):** `/u/[code]`
- **Audience:** UBO individual (login-free)
- **Purpose:** Beneficial owner completes capture on dedicated capability link.

## Entry points
- Email/SMS from KYB chain

## Actions
- **Primary:** Submit UBO details / continue IDV if required
- **Secondary:** View parent entity context (minimal)

## Data shown
- Minimal entity label + UBO form; no other customers' data

## Components used
- C-030 UboPartyList (context), C-025, form inputs C-020, C-027 if pay needed TODO

## Empty / loading / error / success
- Invalid code generic error; success updates parent KYB

## Analytics
- `ubo_page_opened`, `ubo_submitted`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Login-free
- [ ] Codes ≥12 for new links
- [ ] No Personr URL in page
- [ ] Rate-limit enumeration

## Security
- Same capability security as /v

## Related features / pages
- F-017, F-002

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
