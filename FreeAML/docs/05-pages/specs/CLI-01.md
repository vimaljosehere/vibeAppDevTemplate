# CLI-01 — Client verification/pay hub

- **Name:** Client verification/pay hub
- **URL (freeze):** `/v/[code]`
- **Audience:** client (login-free)
- **Purpose:** Capability link hub: status, pay if needed, continue IDV — no firm login.

## Entry points
- SMS/email link, firm share, QR TODO

## Actions
- **Primary:** Pay (if unpaid) or Continue verification
- **Secondary:** View plain-language status

## Data shown
- **Public capability context:** order type, status, amount due — NO short_code echo beyond path, NO PII dump, NO Personr URL
- Party-only fields never here

## Components used
- C-025 StatusBadge, C-026 OrderSummaryCard, C-027 PayCTA, C-006 ClientPaysCallout, C-007 CheckoutBanner

## Empty / loading / error / success
- Invalid code: generic error
- Loading: skeleton
- Unpaid: pay CTA
- Paid ready: continue (via gated /continue when live)
- Complete: success summary without sensitive extras

## Analytics
- `capability_link_opened`, `pay_cta_click`, `continue_click` — code length class only
- No OTPs / ID docs / Personr payloads / raw capability URLs.

## Acceptance criteria
- [ ] Resolves new ≥12-char and legacy short codes (R-005)
- [ ] Login-free
- [ ] Never displays raw Personr URL
- [ ] Pay-before-mint enforced
- [ ] Enumeration rate-limited / generic errors
- [ ] Markup not in URL query

## Security
- R-001, R-003, R-005, R-006; no firm Clerk on this route

## Related features / pages
- F-003, F-004, F-005, F-013; CLI-02

