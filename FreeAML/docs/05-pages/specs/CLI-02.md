# CLI-02 — Gated Personr continue (PLANNED)

- **Name:** Gated Personr continue (PLANNED)
- **URL (freeze):** `/continue`
- **Audience:** client
- **Purpose:** Module 1b: server-side gated redirect to Personr; never show provider URL in UI/JSON.

## Entry points
- From CLI-01 Continue CTA only

## Actions
- **Primary:** Server validates → 302 to Personr
- **Secondary:** Back to /v status on deny

## Data shown
- No page body required; maybe brief interstitial TODO
- Must not embed Personr URL in HTML/JSON for client to scrape casually — redirect response only

## Components used
- Minimal; no ShortCodeDisplay

## Empty / loading / error / success
- Unpaid/unauthorized → deny + message
- Success → redirect
- Already complete → status

## Analytics
- `continue_redirect_ok`, `continue_denied`
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Eligibility checked server-side (paid, not expired, correct subject)
- [ ] 302 only when allowed
- [ ] UI/API never returns raw Personr URL
- [ ] Status: **planned** (M1b)

## Security
- Critical: R-001 + no URL leak; CSRF/session binding TODO

## Related features / pages
- F-013; CLI-01

