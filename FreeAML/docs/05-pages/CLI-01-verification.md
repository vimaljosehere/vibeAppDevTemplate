# CLI-01 — `/v/{code}`

Purpose: client completes verification without firm login.

Must:
- Resolve legacy short codes and new ≥12-char codes
- Show plain-language status and next step
- Never display raw Personr URL (use `/continue`)
- Support client-pays CTA when unpaid

Must not: leak other customers’ data via code enumeration (rate-limit / generic errors).
