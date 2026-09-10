# C-009 — CTASection

## Purpose
Reusable bottom/mid-page call-to-action block.

## Where used
- Most marketing pages

## Props (conceptual)
- Headline, body, primary/secondary buttons

## States
- Default

## Accessibility
- Heading level correct in page outline

## Do-nots
- CTA must not deep-link Personr
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-*
## Behaviour
- Primary button → VerificationForm anchor or `/` start; secondary → pricing/pro.

## Edge cases
- Missing secondary CTA allowed.

## Acceptance criteria
- [ ] Heading level fits page outline
- [ ] Buttons keyboard operable

## Analytics
- `cta_section_click` with location.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
