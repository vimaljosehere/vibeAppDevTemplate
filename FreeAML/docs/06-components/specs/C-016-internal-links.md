# C-016 — InternalLinks

## Purpose
SEO internal linking cluster between toolkit/industry pages.

## Where used
- SEO landings, footer, hub

## Props (conceptual)
- links[] href+label

## States
- Default

## Accessibility
- List of links with clear names

## Do-nots
- Only frozen FreeAML paths
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PUB-08–29, PUB-33
## Behaviour
- Renders related-link clusters (industries, topics) for SEO equity.

## Edge cases
- Empty list → render nothing.

## Acceptance criteria
- [ ] Only frozen FreeAML paths
- [ ] Descriptive link text (not “click here”)

## Analytics
- `internal_link_click` href path.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
