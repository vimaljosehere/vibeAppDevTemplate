# C-006 — ClientPaysCallout

## Purpose
Explains client-pays option and optional Pro markup (on order).

## Where used
- Pricing, Pro, /v unpaid states

## Props (conceptual)
- `amount`, `markupCents?`, `payer`

## States
- Visible, dismissed TODO

## Accessibility
- Aside/note semantics

## Do-nots
- Markup never encoded in `/v` URL (R-003)
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-004, F-005; CLI-01
## Behaviour
- Callout copy: client can pay; Pro firms may add service fee on the **order**.
- May show computed total = base + markup when provided by server.

## Edge cases
- markupCents=0 → hide markup line; Connect not onboarded → soft message.

## Acceptance criteria
- [ ] Never writes fee into `/v` query
- [ ] Aligns with R-002/R-003

## Analytics
- `client_pays_callout_view`.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
