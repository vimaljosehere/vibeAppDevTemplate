# C-012 — BrandProvider

## Purpose
Theme/brand context for white-label-lite / partner skins.

## Where used
- Root layout; partner embed later

## Props (conceptual)
- Brand tokens, logo URL

## States
- Default FreeAML brand

## Accessibility
- Contrast of tokens must meet WCAG

## Do-nots
- Do not load remote CSS from untrusted hosts unchecked
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-015; design tokens
## Behaviour
- Provides CSS variables / theme context from brand config.
- Default = FreeAML; partner override for F-015 later.

## Edge cases
- Missing logo → text wordmark.

## Acceptance criteria
- [ ] Token contrast meets WCAG AA for body text
- [ ] No untrusted remote script injection

## Analytics
- `brand_theme_applied` brandId only.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
