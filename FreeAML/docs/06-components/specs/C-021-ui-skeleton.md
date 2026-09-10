# C-021 — UI Skeleton

## Purpose
Loading placeholder shapes.

## Where used
- Lists, results, /my

## Props (conceptual)
- width/height variants

## States
- Visible while loading

## Accessibility
- aria-busy on container; decorative skeletons aria-hidden

## Do-nots
- N/A
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PAR-01, PAR-04
## Behaviour
- Pulse/shimmer placeholders matching card/list layouts.

## Edge cases
- Prefer `prefers-reduced-motion: reduce` → static gray.

## Acceptance criteria
- [ ] Parent sets aria-busy
- [ ] Skeletons aria-hidden

## Analytics
- None.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
