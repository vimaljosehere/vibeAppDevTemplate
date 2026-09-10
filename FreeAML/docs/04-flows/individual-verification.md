# FLOW-001 — Individual verification (business pays or client pays)

1. Party creates order (type = individual)
2. Stripe Checkout (payer = business or client per order)
3. On paid: create/mint Personr session (never before paid)
4. Client opens `/v/{code}` → continues via **gated** server redirect
5. Personr webhook → update verification_status
6. Party sees results; optional notifications

Edge: unpaid → no Personr; expired JWT → anonymous public status + re-login UX (not hard brick).
