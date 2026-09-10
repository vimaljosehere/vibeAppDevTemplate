# Component library inventory

Filled specs live in [`specs/`](./specs/). Template: [`COMPONENT-TEMPLATE.md`](./COMPONENT-TEMPLATE.md).

| ID | Component | Spec |
|---|---|---|
| C-001 | Navbar | specs/C-001-navbar.md |
| C-002 | PageFooter | specs/C-002-page-footer.md |
| C-003 | VerificationForm | specs/C-003-verification-form.md |
| C-004 | PricingCards / SimplePricingSection | specs/C-004-pricing-cards.md |
| C-005 | PricingFeatureComparison | specs/C-005-pricing-feature-comparison.md |
| C-006 | ClientPaysCallout | specs/C-006-client-pays-callout.md |
| C-007 | CheckoutBanner | specs/C-007-checkout-banner.md |
| C-008 | HowItWorks | specs/C-008-how-it-works.md |
| C-009 | CTASection | specs/C-009-cta-section.md |
| C-010 | TrustBadges | specs/C-010-trust-badges.md |
| C-011 | StructuredData / SEO helpers | specs/C-011-structured-data-seo.md |
| C-012 | BrandProvider | specs/C-012-brand-provider.md |
| C-013 | PillInput | specs/C-013-pill-input.md |
| C-014 | RiskQuestionnaire | specs/C-014-risk-questionnaire.md |
| C-015 | Mockups / VerificationFlowMockup / ComplianceMockups | specs/C-015-mockups-flow.md |
| C-016 | InternalLinks | specs/C-016-internal-links.md |
| C-017 | UI Button | specs/C-017-ui-button.md |
| C-018 | UI Badge | specs/C-018-ui-badge.md |
| C-019 | UI Card | specs/C-019-ui-card.md |
| C-020 | UI Input | specs/C-020-ui-input.md |
| C-021 | UI Skeleton | specs/C-021-ui-skeleton.md |
| C-022 | UI TooltipIcon | specs/C-022-ui-tooltip-icon.md |
| C-023 | Landing FAQ / EntityTypePills / FreeToolsCard | specs/C-023-landing-primitives.md |
| C-024 | OTP input (4-digit) | specs/C-024-otp-input.md |
| C-025 | StatusBadge (order/verification) | specs/C-025-status-badge.md |
| C-026 | OrderSummaryCard | specs/C-026-order-summary-card.md |
| C-027 | PayCTA | specs/C-027-pay-cta.md |
| C-028 | ShortCodeDisplay (party-only) | specs/C-028-short-code-display.md |
| C-029 | EntitySearchResults | specs/C-029-entity-search-results.md |
| C-030 | UboPartyList | specs/C-030-ubo-party-list.md |

## Cross-cutting rules
- No raw Personr URLs in any component (F-013 / `/continue`).
- ShortCodeDisplay is **party-only**.
- OTP is exactly **4 digits** with durable rate limits.
- Analytics hooks must never receive OTP/PII/Personr payloads.
