# C-022 — UI TooltipIcon

## Purpose
Icon with tooltip for helper copy (fees, statuses).

## Where used
- Pricing, forms, status rows

## Props (conceptual)
- content, icon

## States
- Closed/open; focus open

## Accessibility
- Tooltip on focus+hover; Escape closes; not only title attr

## Do-nots
- Do not put secrets in tooltip
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
C-006, C-025
## Behaviour
- Icon button opens tooltip on hover/focus; closes on Escape/blur.

## Edge cases
- Touch: tap toggle; collision with viewport edges.

## Acceptance criteria
- [ ] Keyboard accessible
- [ ] Content not required for critical info-only-in-tooltip (progressive)

## Analytics
- None.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
