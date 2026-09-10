# Permissions (target)

| Action | Client `/v` | Party JWT | Staff | Admin | Owner |
|---|---|---|---|---|---|
| Complete own verification | ✓ | — | — | — | — |
| See short_code / Personr continue | via gated server | party only | firm scope | firm scope | firm scope |
| Create order | — | ✓ | ✓ | ✓ | ✓ |
| View all firm orders | — | — | ✓ | ✓ | ✓ |
| CSV export | — | — | — | ✓ | ✓ |
| Billing / Connect markup | — | — | — | — | ✓ |
| Manage members | — | — | — | ✓ | ✓ |

**Rule:** ungated `order-status` returns public fields only (no `short_code`, PII, Personr link).
