# C-027 — PayCTA

## Purpose
Primary pay button launching Stripe Checkout for client-pays orders.

## Where used
- CLI-01, unpaid banners

## Props (conceptual)
- orderId, amount, disabledReason

## States
- Ready, loading, disabled (already paid)

## Accessibility
- Button name includes amount

## Do-nots
- Never enable mint path before paid
- No markup in URL
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-004; CLI-01
## Behaviour
- Starts Stripe Checkout for unpaid client-pays orders.
- Disabled when paid, loading, or missing session.

## Edge cases
- Popup blockers → full-page redirect fallback TODO.
- 402/unpaid mint still blocked server-side regardless of CTA.

## Acceptance criteria
- [ ] Label includes amount
- [ ] No Personr navigation from this button
- [ ] Idempotent checkout session create

## Analytics
- `pay_cta_click` orderType only.
