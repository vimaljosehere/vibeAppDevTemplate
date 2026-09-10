# C-023 — Landing FAQ / EntityTypePills / FreeToolsCard

## Purpose
Grouped marketing primitives for SEO landings: FAQ accordion, entity-type pills, free-tools card.

## Where used
- PUB SEO landings, compliance hub, home

## Props (conceptual)
- FAQ items; entity types; tools links

## States
- FAQ collapsed/expanded; pill selected

## Accessibility
- Accordion keyboard pattern; pills radiogroup or tabs as appropriate

## Do-nots
- FAQ answers must not include Personr URLs or real customer data
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-018; PUB-08–29; C-003
## Behaviour
- **FAQ:** accordion Q&A for landings.
- **EntityTypePills:** individual vs company (etc.) selector feeding VerificationForm.
- **FreeToolsCard:** promo card linking to compliance toolkit.

## Edge cases
- Only one FAQ open vs multi TODO; pills required before submit.

## Acceptance criteria
- [ ] FAQ keyboard accordion pattern
- [ ] Pills expose selected state to AT
- [ ] Tools card uses frozen `/compliance` paths

## Analytics
- `faq_open` (question id), `entity_type_selected`, `free_tools_click`.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
