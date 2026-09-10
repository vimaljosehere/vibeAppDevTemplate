# C-017 — UI Button

## Purpose
Design-system button primitive.

## Where used
- Everywhere

## Props (conceptual)
- variant, size, loading, disabled, asChild TODO

## States
- Default, hover, focus, loading, disabled

## Accessibility
- button role; loading aria-busy; disabled not focus-trapped wrongly

## Do-nots
- Destructive actions need confirm at call site
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
All pages
## Behaviour
- Variants: primary, secondary, outline, destructive, ghost; sizes sm/md/lg.
- Loading replaces label with spinner + aria-busy.

## Edge cases
- asChild/link mode keeps focus styles.

## Acceptance criteria
- [ ] Focus visible
- [ ] Disabled not submitable
- [ ] Contrast per variant

## Analytics
- Left to call sites.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
