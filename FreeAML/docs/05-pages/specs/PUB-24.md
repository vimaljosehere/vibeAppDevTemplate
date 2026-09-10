# PUB-24 — Tranche 2 compliance

- **Name:** Tranche 2 compliance
- **URL (freeze):** `/tranche-2-compliance`
- **Audience:** public (SEO)
- **Purpose:** Convert search intent («Tranche 2 how-to») into a verification start. Keywords: tranche 2 compliance.

## Shared SEO landing pattern
- Audience: public (organic search)
- Primary action: start verification via **VerificationForm** (C-003) or CTA into form
- Secondary: pricing, toolkit links, InternalLinks (C-016)
- Components: Navbar, PageFooter, HowItWorks/CTA/TrustBadges as relevant, StructuredData, FAQ primitives (C-023)
- Empty/loading/error/success: form validation + submit → checkout/order path; skeleton optional
- Analytics: `seo_landing_view` + `verification_form_submit` with `landing_slug` — no PII
- Security: public page; freeze URL; no Personr URLs; bot/rate considerations on form POST
- Data shown: marketing copy only (public); no auth data


## Entry points
- Organic search, InternalLinks, toolkit cross-links, ads TODO

## Actions
- **Primary:** Submit VerificationForm / start check CTA
- **Secondary:** Pricing, Pro, related SEO pages, compliance hub

## Unique intent / CTA
- Intent: Tranche 2 how-to
- Emphasize industry or query language in H1/copy; CTA still starts FreeAML check (individual or business as relevant).
- PUB-16/17 lean KYB/UBO; PUB-19 may tease PDF CDD (F-014 planned).

## Acceptance criteria
- [ ] URL never renamed during strangler
- [ ] VerificationForm or clear CTA to it present
- [ ] Unique title/H1 for `tranche 2 compliance`
- [ ] StructuredData where applicable (C-011)
- [ ] No Personr provider URLs

## Related features / pages
- F-018, F-020; PUB-01, PUB-33; nearby industry/topic pages via C-016

## Shared product rules (apply)
- Tagline: make AML dead simple.
- Stack: Next.js, Vercel, Supabase, Stripe+Connect, Personr, Resend, Twilio.
- Pay before Personr mint; Connect markup on order not `/v` URL; single Connect payout.
- Ungated status: no short_code/PII/Personr link; expired JWT → anonymous not hard 401.
- Public `/v` login-free; firm Clerk auth separate; freeze SEO URLs.
- New short codes ≥12 chars; OTP 4-digit + durable rate limits.
