# PUB-07 — Blog index

- **Name:** Blog index
- **URL (freeze):** `/blog`
- **Audience:** public
- **Purpose:** Content hub; child post routes exist under /blog/* (inventory note).

## Entry points
- SEO, nav, internal links

## Actions
- **Primary:** Open a post
- **Secondary:** CTA to toolkit / verification

## Data shown
- Public post list; child posts are separate routes (do not rename)

## Components used
- C-001/002, C-016, cards

## Empty / loading / error / success
- Empty: no posts message; loading skeletons

## Analytics
- `blog_index_view`, `blog_post_click`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Lists posts
- [ ] Note: child posts exist — freeze those URLs too
- [ ] CTA present

## Security
- Public CMS content

## Related features / pages
- F-018; toolkit pages


## Child routes
- Blog posts under `/blog/...` exist in production — treat as frozen SEO URLs; not individually inventoried here.

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
