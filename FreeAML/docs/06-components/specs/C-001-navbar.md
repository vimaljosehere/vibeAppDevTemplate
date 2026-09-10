# C-001 — Navbar

## Purpose
Global top navigation for marketing and light app chrome.

## Where used
- Most PUB pages; /my may use variant

## Props (conceptual)
- Links, logo, optional CTA (`Start check`, `Pro`)
- `variant`: marketing | app

## States
- Default, mobile menu open, active route

## Accessibility
- Landmark `<nav>`; mobile button aria-expanded; focus trap in drawer TODO

## Do-nots
- Do not require firm auth on public pages
- Do not link to Personr
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-*; PAR-*
## Behaviour
- Renders FreeAML logo + primary nav (Pricing, Pro, Compliance, Blog as applicable).
- Mobile: hamburger opens panel; closes on route change / Escape.
- App variant may show `/my` links when OTP session exists — never gate public `/v`.

## Edge cases
- Unknown active route: no crash; no false “active”.
- Reduced-motion: skip heavy menu transitions.

## Acceptance criteria
- [ ] Present on marketing layouts without layout shift
- [ ] Keyboard-accessible mobile menu
- [ ] CTAs go to frozen FreeAML routes only

## Analytics
- `nav_cta_click` with target path — no PII.
