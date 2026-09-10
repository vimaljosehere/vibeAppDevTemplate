# C-003 — VerificationForm

## Purpose
Primary conversion form to start individual/business verification — make AML dead simple.

## Where used
- PUB-01 home; SEO landings PUB-08–29; CTAs

## Props (conceptual)
- `entityType`, contact fields, submit handler
- Optional `landingSlug` for analytics

## States
- Idle, validating, submitting, error, success→redirect

## Accessibility
- Labelled inputs; error announced; keyboard submit

## Do-nots
- Do not mint Personr from form alone — pay-before-mint server-side
- Do not stash markup in query string
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-018, F-020; PUB-01
## Behaviour
- Collects enough to create an order draft (individual vs business).
- On submit: server creates order → client-pays or party-pays checkout path.
- `landingSlug` stamped for funnel analytics only.

## Edge cases
- Double-submit guarded; network error keeps values; bot honeypot TODO.

## Acceptance criteria
- [ ] Works on `/` and SEO landings without account
- [ ] Does not call Personr mint
- [ ] Validation messages are field-linked

## Analytics
- `verification_form_submit` + `landing_slug` — no raw form PII in event props.
