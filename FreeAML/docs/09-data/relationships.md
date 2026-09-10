# Relationships

- Org 1—* Orders (future); today orders may be party-scoped
- Order 1—* verification legs / UBO children (KYB)
- Order 1—1 Stripe payment intent/session (preferred)
- Order 0—1 Personr session (after paid)
