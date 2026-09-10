# PUB-38 — Program (redirect)

- **Name:** Program (redirect)
- **URL (freeze):** `/program`
- **Audience:** public
- **Purpose:** Legacy/SEO path — **redirect** to current program target (document target).

## Entry points
- Old links, SEO

## Actions
- **Primary:** Follow redirect to live program content
- **Secondary:** n/a

## Data shown
- None (redirect)

## Components used
- Server redirect only

## Empty / loading / error / success
- Ensure 301/308 as intended; no interstitial leak

## Analytics
- `redirect_hit` path=/program (optional)
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Redirects to live toolkit program destination
- [ ] **TODO:** confirm exact target path in complyin30 (likely compliance program page)
- [ ] Keep `/program` frozen as alias

## Security
- Open redirect safe: fixed target only

## Related features / pages
- F-009; PUB-33


## Redirect target
- **TODO:** Document exact production redirect target from live `complyin30` routes (do not invent).

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
