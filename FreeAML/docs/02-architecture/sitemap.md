# Sitemap (freeze during strangler)

## Public
- `/` home
- Toolkit / guide routes (existing SEO URLs — do not rename)
- Pricing / for-firms (add when firm mode ships)

## App / party
- `/results/[id]` or `/r/{code}` status
- `/my` or OTP login surfaces
- Future: `/app` firm dashboard, `/app/orders`, `/app/settings`

## Client
- `/v/{code}` verification hub
- `/continue` (planned) server redirect to Personr — never show raw provider URL in UI/JSON

## Webhooks (keep paths)
- Stripe webhook
- Personr webhook

TODO: paste exact production path list from `complyin30` when reviewing.
