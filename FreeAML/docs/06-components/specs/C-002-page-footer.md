# C-002 — PageFooter

## Purpose
Site footer with legal, toolkit, and SEO internal links.

## Where used
- Public layouts

## Props (conceptual)
- Link groups; locale note AU

## States
- Default

## Accessibility
- Footer landmark; link lists

## Do-nots
- No capability codes or PII
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-*; C-016
## Behaviour
- Groups: Product, Toolkit, Industries, Legal.
- Includes AU jurisdiction cue; optional NZ note later (see locale docs).

## Edge cases
- Long link lists wrap without overflow on mobile.

## Acceptance criteria
- [ ] All hrefs are frozen public paths or legal pages
- [ ] No capability codes or Personr links

## Analytics
- Optional `footer_link_click` (path only).

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
