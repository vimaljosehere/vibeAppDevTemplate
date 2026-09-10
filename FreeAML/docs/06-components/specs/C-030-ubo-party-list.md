# C-030 — UboPartyList

## Purpose
Lists directors/UBOs and invite/capture state for KYB chain.

## Where used
- Business results; CLI-03 context; party KYB detail

## Props (conceptual)
- parties[], statuses, invite actions

## States
- Empty, partial, complete

## Accessibility
- Table or list with row headers

## Do-nots
- Invite links are `/u/{code}` not Personr URLs
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-002, F-017; CLI-03
## Behaviour
- Lists directors/UBOs with capture status; actions issue `/u/{code}` invites.
- Parent KYB completeness derives from list state.

## Edge cases
- Empty list on new company; invite resend cooldown.

## Acceptance criteria
- [ ] Invite hrefs are `/u/...` not Personr
- [ ] Status via C-025 or inline
- [ ] Accessible table/list

## Analytics
- `ubo_invite_sent` count only; `ubo_list_view`.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
