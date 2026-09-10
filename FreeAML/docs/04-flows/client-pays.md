# FLOW-002 — Client pays (+ optional markup)

1. Firm sets payer = client; optional Connect markup stored **on order**
2. Client pays on Stripe hosted checkout
3. Same post-pay Personr rules as FLOW-001
4. Firm receives net + markup via Connect (single payout path — no double transfer)

Markup inactive as a marketed product until Pro module ships; data model must already support fee on order.
