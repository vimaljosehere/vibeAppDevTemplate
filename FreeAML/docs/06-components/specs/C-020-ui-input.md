# C-020 — UI Input

## Purpose
Text input primitive.

## Where used
- Forms, OTP wrappers, settings

## Props (conceptual)
- type, label, error, hint

## States
- Default, error, disabled

## Accessibility
- id/label binding; aria-invalid; describedby errors

## Do-nots
- Never log input values (OTP/PII) to analytics
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
PAR-02, C-024, C-003
## Behaviour
- Text/email/tel/password types; hint + error slots.
- Forwards refs for form libs.

## Edge cases
- Autofill styles; paste into tel.

## Acceptance criteria
- [ ] Label linked via id
- [ ] aria-invalid when error
- [ ] Never analytics value

## Analytics
- Forbidden on value changes for sensitive fields.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
