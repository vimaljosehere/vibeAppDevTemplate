# C-026 — OrderSummaryCard

## Purpose
Summary of order type, amount, payer, status for client/party views.

## Where used
- CLI-01, PAR-01

## Props (conceptual)
- orderType, amount, payer, status; redactMode

## States
- Loading via skeleton; redacted vs full

## Accessibility
- Heading + definition list

## Do-nots
- In redactMode: no short_code, PII, Personr link (R-006)
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-007; C-025
## Behaviour
- Shows order type, amount, payer, status.
- `redactMode=true` for ungated/anonymous: strip short_code, PII, Personr link (R-006).

## Edge cases
- Expired JWT parent passes redactMode (R-007).

## Acceptance criteria
- [ ] Redacted vs full modes differ as specified
- [ ] Pay CTA slot optional via children

## Analytics
- Parent page events only.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
