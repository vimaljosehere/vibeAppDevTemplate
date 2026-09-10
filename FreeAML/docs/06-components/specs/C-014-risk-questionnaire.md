# C-014 — RiskQuestionnaire

## Purpose
Guided business risk assessment questionnaire (toolkit).

## Where used
- Risk assessment destination; compliance hub

## Props (conceptual)
- Questions[], answers, progress

## States
- In progress, complete, review

## Accessibility
- Fieldsets/legends; progress announced

## Do-nots
- Results educational — not a regulated determination claim TODO
- **Never** render raw Personr provider URLs (use gated `/continue` when live).
- Do not put OTPs, ID images, or Personr payloads into analytics hooks.

## Related pages / features
F-009; PUB-39
## Behaviour
- Multi-step questions for business risk assessment toolkit.
- Saves progress locally or to party account when authed TODO.

## Edge cases
- Refresh mid-flow restores TODO; abandon OK.

## Acceptance criteria
- [ ] Completing fires `training`/`toolkit` completion-style event without answers PII dump
- [ ] Works from redirect target of `/risk-assessment`

## Analytics
- `risk_questionnaire_step`, `risk_questionnaire_complete` — step index only.

## Implementation notes
- Prefer existing design tokens (`docs/07-design/`).
- Keep file focused; compose rather than duplicate PayCTA/StatusBadge logic.
