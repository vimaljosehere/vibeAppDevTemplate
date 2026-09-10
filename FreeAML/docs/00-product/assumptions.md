# Assumptions & open questions

## Locked (treat as true)

- Next.js + Vercel + Supabase + Stripe + Personr + Twilio/Resend
- SEO URLs and content paths stay frozen during strangler
- 4-digit OTP + durable `otp_attempts`; new short codes ≥12 chars
- Markup fee lives on **order**, not `/v/{code}`
- Personr URL must not leak to ungated JSON/UI (gated `/continue` planned)
- Institutional sell only after: Module 1 money path + firm login + shared checks + CSV + DPA

## TODO (fill when editing)

- [ ] Exact public price list vs Connect markup tiers (site vs code drift)
- [ ] Which toolkit pages are MVP vs later
- [ ] NZ provider equivalents (see `14-locale`)
- [ ] White-label / API priority vs packs
