# C-011 — StructuredData / SEO helpers

## Purpose
JSON-LD / meta helpers for frozen SEO URLs.

## Where used
- PUB landings, home, blog

## Props (conceptual)
- Schema type, title, description canonical

## States
- Server-rendered

## Accessibility
- N/A visual; ensure valid JSON-LD

## Do-nots
- Do not put PII in structured data
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-018; PUB-08–29
## Behaviour
- Emits JSON-LD (Organization, WebPage, FAQPage as relevant) + canonical.
- Uses frozen URL as `@id` / canonical.

## Edge cases
- Invalid JSON must not break page (build-time validate).

## Acceptance criteria
- [ ] Canonical matches freeze list
- [ ] No PII in schema

## Analytics
- N/A (SEO).

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
