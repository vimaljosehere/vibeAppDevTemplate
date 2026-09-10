# Tech decisions

| Decision | Choice | Why |
|---|---|---|
| Framework | Stay Next.js | SEO + speed; no Go rewrite |
| Firm auth | Clerk Organizations | teams/roles/invites; not on `/v` |
| OTP length | 4 digits | “dead simple”; compensate with rate limits |
| Short codes | ≥12 new | capability-URL safety |
| Markup | on order | stable links |
| Analytics | PostHog + GA4 | product + acquisition; server events on webhooks |
| Rebuild | strangler modules | protect SEO + live money path |
