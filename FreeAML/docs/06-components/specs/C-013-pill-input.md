# C-013 — PillInput

## Purpose
Pill-styled text/chip input for filters or entity type entry.

## Where used
- Landings, entity search UI

## Props (conceptual)
- value, onChange, placeholder

## States
- Focus, error, disabled

## Accessibility
- Associated label; focus ring

## Do-nots
- N/A Personr
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
C-029; PUB-16
## Behaviour
- Pill chrome around input; Enter commits chip if chip-mode.

## Edge cases
- Max length; paste handling.

## Acceptance criteria
- [ ] Label visible or aria-label
- [ ] Error state announced

## Analytics
- None (avoid keystroke logging).

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
