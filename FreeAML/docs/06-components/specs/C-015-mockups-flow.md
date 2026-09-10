# C-015 — Mockups / VerificationFlowMockup / ComplianceMockups

## Purpose
Marketing mockups illustrating verification/compliance UI.

## Where used
- Home, Pro, SEO landings

## Props (conceptual)
- Variant: verification | compliance

## States
- Static decorative

## Accessibility
- alt text summarizing mock; aria-hidden if pure decoration with adjacent text

## Do-nots
- Mock must not show real PII or real Personr URLs
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-01, PUB-03
## Behaviour
- Static illustrations of `/v` hub, results, or compliance UI for marketing.
- Variants switch artwork.

## Edge cases
- Reduced-motion: static frame only.

## Acceptance criteria
- [ ] No real customer names/codes in artwork
- [ ] No Personr URL strings in mock UI chrome

## Analytics
- None.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
