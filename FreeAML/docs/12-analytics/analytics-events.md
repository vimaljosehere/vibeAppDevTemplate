# Analytics events

Instrument funnel: landing → toolkit → start verification → checkout → paid → Personr start → Personr outcome → complete.

Server-side captures on Stripe/Personr webhooks = source of truth.

Identify/group with Clerk userId/orgId when firm auth lands.

**Never send:** OTPs, ID images, Personr payloads, raw capability URLs.

Operating scoreboard (checks/day, blended take, live firms) — **build dashboard only after** Module 1 + markup + firm basics.
