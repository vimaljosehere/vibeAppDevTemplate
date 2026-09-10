# C-024 — OTP input (4-digit)

## Purpose
Four separate digit inputs for OTP auth on /my.

## Where used
- PAR-02 `/my` (may be page-local; still required component)

## Props (conceptual)
- length=4 fixed; onComplete; error

## States
- Empty, partial, complete, error, rate-limited

## Accessibility
- One field per digit or single with masking — announce errors; autocomplete one-time-code

## Do-nots
- **Do not** analytics the OTP value (R-012)
- Enforce durable rate limits server-side (R-004)
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-006; PAR-02
## Behaviour
- Exactly **4** digit cells; auto-advance; paste full code supported.
- onComplete fires once when 4 digits present; server verifies.

## Edge cases
- Rate-limited: show wait message; wrong code clears last digit or all TODO.
- Resend cooldown separate control on page.

## Acceptance criteria
- [ ] Length fixed at 4 (R-004)
- [ ] `autocomplete="one-time-code"` where supported
- [ ] OTP value never sent to analytics (R-012)
- [ ] Works inside `/my` OTP gate

## Analytics
- Parent fires `otp_verified` / `otp_rate_limited` only.
