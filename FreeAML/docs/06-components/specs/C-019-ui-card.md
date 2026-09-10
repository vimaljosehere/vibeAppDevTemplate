# C-019 — UI Card

## Purpose
Surface container for content groups.

## Where used
- Dashboards, landings, /my

## Props (conceptual)
- title, children, footer

## States
- Default, interactive/hover if link card

## Accessibility
- If clickable, keyboard activatable

## Do-nots
- N/A
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PAR-03+
## Behaviour
- Container with optional header/footer slots; link-card variant navigates.

## Edge cases
- Nested interactive elements forbidden in link-card.

## Acceptance criteria
- [ ] Padding/spacing matches design tokens
- [ ] Keyboard activation if clickable

## Analytics
- Call site.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
