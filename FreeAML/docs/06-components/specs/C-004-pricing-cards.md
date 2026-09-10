# C-004 — PricingCards / SimplePricingSection

## Purpose
Display price tiers / simple pricing section.

## Where used
- PUB-02, PUB-03, home sections

## Props (conceptual)
- Plans, amounts AUD, CTA targets

## States
- Default, highlighted plan

## Accessibility
- Clear price text; CTA accessible names

## Do-nots
- Do not imply URL-based markup fees
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-004, F-005, F-019
## Behaviour
- Shows AUD amounts and who pays (firm vs client).
- Pro card mentions Connect markup stored on order.

## Edge cases
- Missing price config → TODO fallback copy, no blank card.

## Acceptance criteria
- [ ] Client-pays explained
- [ ] Markup not described as URL parameter

## Analytics
- `pricing_card_cta` with plan id.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
