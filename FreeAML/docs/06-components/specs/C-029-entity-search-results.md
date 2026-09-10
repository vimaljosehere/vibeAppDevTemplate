# C-029 — EntitySearchResults

## Purpose
List ABN/ACN/name search hits for KYB start.

## Where used
- Business verification flow; entity landings

## Props (conceptual)
- results[], onSelect, loading, empty

## States
- Loading, empty, error, populated

## Accessibility
- Listbox/option pattern or links

## Do-nots
- Do not leak unrelated org customer data
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-002; PUB-16
## Behaviour
- Renders ABR-style search hits; selecting continues KYB order create.

## Edge cases
- Zero hits → empty state + manual entry TODO.
- Provider timeout → retry.

## Acceptance criteria
- [ ] Keyboard list navigation
- [ ] Selection returns stable entity id
- [ ] No cross-tenant data

## Analytics
- `entity_search_performed` (hit_count only), `entity_selected`.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
