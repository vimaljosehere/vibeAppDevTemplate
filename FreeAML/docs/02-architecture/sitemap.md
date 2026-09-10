# Sitemap (freeze during strangler)

Aligned to `docs/05-pages/page-inventory.md`. Do not rename frozen public/SEO URLs.

## Public / SEO
- `/` — Homepage (PUB-01)
- `/pricing` — Pricing (PUB-02)
- `/pro`, `/pro/signup`, `/pro/welcome` — Pro funnel (PUB-03–05)
- `/compare` — Compare (PUB-06)
- `/blog` (+ child posts) — Blog (PUB-07)
- SEO landings (PUB-08–29): `/aml-check`, `/aml-check-cost`, `/kyc-check`, `/kyc-check-cost`, `/free-aml-check`, `/free-kyc-check`, `/free-identity-verification`, `/identity-verification`, `/entity-verification`, `/ubo-verification`, `/customer-due-diligence`, `/cdd-report`, `/austrac-compliance`, `/aml-ctf-compliance`, `/aml-software-australia`, `/tranche-2`, `/tranche-2-compliance`, `/conveyancer`, `/accountants`, `/lawyers`, `/real-estate`, `/jewellers`
- `/vs/easyaml`, `/vs/firstaml` — Competitor pages (PUB-30–31)
- `/sixstep` — Six-step education (PUB-32)
- Toolkit: `/compliance`, `/compliance-docs`, `/reports`, `/training`, `/training/[moduleId]` (PUB-33–37)
- Redirects (keep aliases): `/program` (PUB-38), `/risk-assessment` (PUB-39) — **TODO** confirm live targets
- `/components` — Internal kitchen sink (PUB-40, low priority)

## Client / capability
- `/v/[code]` — Client verification/pay hub (CLI-01) — login-free
- `/continue` — Planned gated Personr redirect (CLI-02, Module 1b)
- `/u/[code]` — UBO capture (CLI-03)
- `/r/[code]` — Short-code results entry (CLI-04; alias to results if absent)

## Party / my
- `/results/[id]` — Results (PAR-01)
- `/my` — OTP login (PAR-02)
- `/my/dashboard`, `/my/verifications`, `/my/compliance`, `/my/references`, `/my/settings`, `/my/team` (PAR-03–08)

## Org
- `/org/create` (ORG-01)
- `/org/[code]` (ORG-02)

## Internal
- `/testpdfs` (INT-01)
- `/internal` (INT-02) — purpose TODO

## Webhooks (keep paths)
- Stripe webhook
- Personr webhook

## Rules affecting routes
- Public `/v` stays login-free; firm auth (Clerk later) separate
- Ungated status redacts short_code / PII / Personr link; expired JWT → anonymous not hard 401
- New short codes ≥12 chars; markup on order not in `/v` URL
