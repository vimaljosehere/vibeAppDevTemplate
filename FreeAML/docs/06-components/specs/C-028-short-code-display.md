# C-028 — ShortCodeDisplay (party-only)

## Purpose
Shows capability short code / link to the **party** only.

## Where used
- PAR-01 auth results; party dashboards — **never** ungated public

## Props (conceptual)
- code, copy button

## States
- Visible, copied toast

## Accessibility
- Read-only text; copy button labelled

## Do-nots
- **Do not** render on ungated order-status payloads (R-006)
- New codes ≥12 chars (R-005)
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-003, F-007; PAR-01
## Behaviour
- Displays short code + copy-to-clipboard for **authenticated party** only.
- May show full `/v/{code}` link for sharing.

## Edge cases
- Copy fail → manual select message.
- Legacy short codes (<12) still display if historical (R-005).

## Acceptance criteria
- [ ] Not mounted on ungated public status views
- [ ] Copy control labelled
- [ ] New codes documented ≥12 chars

## Analytics
- `short_code_copied` — never the code value.
