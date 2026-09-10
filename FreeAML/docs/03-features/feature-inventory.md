# Feature inventory

Tagline: **make AML dead simple**. Specs are filled per row under this folder.

| ID | Feature | Status | Spec | Module |
|---|---|---|---|---|
| F-001 | Individual KYC (Personr) | live | `F-001-individual-kyc-personr.md` | Core / Personr |
| F-002 | Business KYB + UBO chain | live | `F-002-business-kyb-ubo.md` | Core / Personr |
| F-003 | Client capability links /v/{code} | live | `F-003-client-capability-links.md` | Core |
| F-004 | Client-pays Stripe | live | `F-004-client-pays-stripe.md` | Payments |
| F-005 | Connect markup on order (Pro) | partial | `F-005-connect-markup-on-order.md` | Pro / Connect |
| F-006 | OTP auth 4-digit | live | `F-006-otp-auth-4-digit.md` | Auth |
| F-007 | Order status / results (/results, /r) | live | `F-007-order-status-results.md` | Core |
| F-008 | Notifications email/SMS | partial | `F-008-notifications-email-sms.md` | Notifications |
| F-009 | Compliance toolkit | live | `F-009-compliance-toolkit.md` | Toolkit / SEO |
| F-010 | Firm orgs (Clerk planned; today /org, /my/team) | partial | `F-010-firm-orgs.md` | Orgs |
| F-011 | Shared checks + CSV export | planned | `F-011-shared-checks-csv.md` | Orgs |
| F-012 | Prepaid packs / invoice | planned | `F-012-prepaid-packs-invoice.md` | Payments |
| F-013 | Gated Personr /continue | planned | `F-013-gated-personr-continue.md` | Personr / M1b |
| F-014 | PDF CDD report | planned | `F-014-pdf-cdd-report.md` | Reporting |
| F-015 | Partner embed / API | planned | `F-015-partner-embed-api.md` | Partner |
| F-016 | Ongoing monitoring | planned | `F-016-ongoing-monitoring.md` | Monitoring |
| F-017 | UBO capture via /u/{code} | live | `F-017-ubo-capture-u-code.md` | Core |
| F-018 | Industry/SEO landing conversion | live | `F-018-industry-seo-landing.md` | Marketing/SEO |
| F-019 | Pro marketing + signup (/pro) | partial | `F-019-pro-marketing-signup.md` | Pro |
| F-020 | Home instant verification start (/) | live | `F-020-home-instant-verification.md` | Marketing/Core |

## Locked rules (apply across features)
- 4-digit OTP + durable rate limits (R-004)
- New short codes ≥12 chars; legacy still resolve (R-005)
- Pay before Personr mint (R-001)
- Connect markup on **order**, not `/v` URL; single Connect payout path (R-002, R-003)
- Ungated order-status: no short_code / PII / Personr link; expired JWT → anonymous not hard 401 (R-006, R-007)
- Planned `/continue` gated Personr redirect (F-013 / Module 1b)
- Public `/v/{code}` login-free; firm auth separate (Clerk later); freeze SEO URLs
