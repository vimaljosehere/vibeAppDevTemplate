# User roles

| Role | Context |
|---|---|
| Anonymous client | `/v/{code}` only |
| Party (email/OTP JWT) | Own orders / results |
| Account owner | Firm billing + settings (future Clerk org) |
| Admin / compliance | Shared checks, export, staff invites |
| Staff | Create/monitor checks for the firm |
| Viewer | Read-only (optional later) |

Public client path stays **login-free**. Firm staff auth is separate (Clerk Organizations planned).
