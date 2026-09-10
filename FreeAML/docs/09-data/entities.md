# Entities

| Entity | Key fields (conceptual) |
|---|---|
| Order | id, short_code, type, status, payer, amount, markup, contacts, stripe_*, personr_* (private) |
| Subject | person or company fields on/related to order |
| OtpAttempt | contact, window, count (durable) |
| Org | id, name, connect account (future) |
| Membership | org, user, role (future) |

TODO: align names 1:1 with Supabase tables during review.
