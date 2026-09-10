# C-005 — PricingFeatureComparison

## Purpose
Feature comparison table across plans / competitors.

## Where used
- PUB-02, PUB-06, PUB-30/31

## Props (conceptual)
- Rows/columns of features; checkmarks

## States
- Default; responsive stacked TODO

## Accessibility
- Table headers; scope attributes

## Do-nots
- No false claims; R-009 no remint promises
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-02, PUB-06
## Behaviour
- Matrix of features vs plans or vs competitor claims.
- Responsive: table → stacked definition lists on small screens TODO.

## Edge cases
- Unequal column counts; long feature names wrap.

## Acceptance criteria
- [ ] Accessible table or equivalent
- [ ] No R-009 remint claims

## Analytics
- `compare_table_view` (page id).

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
