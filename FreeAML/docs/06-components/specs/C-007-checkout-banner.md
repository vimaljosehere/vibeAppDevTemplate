# C-007 — CheckoutBanner

## Purpose
Banner prompting incomplete checkout / return to pay.

## Where used
- CLI-01 unpaid; results unpaid

## Props (conceptual)
- `orderId`, `amountDue`, CTA

## States
- Info / urgent

## Accessibility
- role=status if live updates

## Do-nots
- Do not expose card data
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-004; C-027
## Behaviour
- Sticky or inline banner when checkout abandoned / unpaid.
- CTA resumes Stripe Checkout session or creates new idempotently TODO.

## Edge cases
- Already paid race → banner hides after refresh/webhook.

## Acceptance criteria
- [ ] Only shows when unpaid client-pays
- [ ] CTA disabled while redirecting

## Analytics
- `checkout_banner_cta`.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
