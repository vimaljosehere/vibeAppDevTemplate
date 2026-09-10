# C-008 — HowItWorks

## Purpose
3–6 step explainer of FreeAML flow.

## Where used
- Home, SEO landings, sixstep-related

## Props (conceptual)
- Steps[] title/body/icon

## States
- Default

## Accessibility
- Ordered list semantics

## Do-nots
- Keep copy aligned to pay-before-Personr
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-01, PUB-32; F-020
## Behaviour
- Steps include: start → pay → verify (Personr) → results — emphasizing pay before IDV.

## Edge cases
- Customize step count per landing without breaking a11y list.

## Acceptance criteria
- [ ] Ordered list semantics
- [ ] Copy mentions client-pays optionally

## Analytics
- None required (content).

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
