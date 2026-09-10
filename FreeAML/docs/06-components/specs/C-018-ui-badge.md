# C-018 — UI Badge

## Purpose
Small categorical badge (plan, tag).

## Where used
- Pricing, lists

## Props (conceptual)
- tone, children

## States
- Default

## Accessibility
- Not only color — text included

## Do-nots
- Distinct from StatusBadge (C-025)
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-02; C-025
## Behaviour
- Compact label chip for plan names, tags — not order status (use C-025).

## Edge cases
- Long text truncates with title tooltip TODO.

## Acceptance criteria
- [ ] Text + tone (not color alone)
- [ ] Distinct from StatusBadge

## Analytics
- None.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
