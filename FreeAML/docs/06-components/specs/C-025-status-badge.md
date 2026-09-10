# C-025 — StatusBadge (order/verification)

## Purpose
Shows order/verification status: pending / paid / in progress / complete / failed (etc.).

## Where used
- CLI-01, PAR-01, /my lists

## Props (conceptual)
- status enum → tone+label

## States
- Each status tone

## Accessibility
- Text label always; not color-only

## Do-nots
- Do not embed provider URLs in title
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-007; CLI-01
## Behaviour
- Maps status enum → label + tone (pending, paid, in_progress, complete, failed, expired TODO).

## Edge cases
- Unknown status → neutral “Unknown” not crash.

## Acceptance criteria
- [ ] Text label always present
- [ ] Used consistently on CLI-01 and PAR-01

## Analytics
- Optional `status_badge_view` with status enum only.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
