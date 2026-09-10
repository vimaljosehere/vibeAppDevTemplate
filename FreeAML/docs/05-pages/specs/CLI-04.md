# CLI-04 — Short-code results entry

- **Name:** Short-code results entry
- **URL (freeze):** `/r/[code]`
- **Audience:** party / recipient
- **Purpose:** Short-code results entry. **If route missing in live app, treat as alias note to `/results/[id]`.**

## Entry points
- Notifications, shared links

## Actions
- **Primary:** Open results (auth may upgrade payload)
- **Secondary:** OTP login to unlock full detail

## Data shown
- Ungated: redacted status only (R-006)
- Auth: fuller results

## Components used
- C-025, C-026; C-028 party-only when auth

## Empty / loading / error / success
- Unknown code generic; expired JWT → anonymous not 401 brick (R-007)

## Analytics
- `results_shortcode_open`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] **TODO:** confirm `/r/[code]` exists in complyin30; if not, document alias/redirect to PAR-01
- [ ] Ungated redaction rules hold
- [ ] New codes ≥12 chars

## Security
- R-006, R-007

## Related features / pages
- F-007; PAR-01, PAR-02


## Alias note
- If `/r/[code]` is not a live route, keep this ID as the documented short-code entry and map behaviour to `/results/[id]` + OTP.
