# C-010 — TrustBadges

## Purpose
Trust/credibility badges (AUSTRAC context, security, payments).

## Where used
- Home, pricing, landings

## Props (conceptual)
- Badge list

## States
- Default

## Accessibility
- Decorative images alt="" or labelled

## Do-nots
- No fake certifications
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-01
## Behaviour
- Displays trust cues (payments via Stripe, AU focus, security).
- Icons decorative when adjacent text present.

## Edge cases
- Image fail → text fallback.

## Acceptance criteria
- [ ] No fabricated regulator endorsement
- [ ] Contrast OK on dark/light

## Analytics
- None.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
