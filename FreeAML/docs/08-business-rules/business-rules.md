# Business rules

| ID | Rule |
|---|---|
| R-001 | Do not mint Personr until order is paid (402 otherwise) |
| R-002 | Single Connect payout path — no double transfer |
| R-003 | Markup/Connect fee stored on order at creation; not in `/v` URL |
| R-004 | OTP = 4 digits via secure RNG; durable attempt limits |
| R-005 | New short codes ≥12 chars; old short codes still resolve |
| R-006 | Ungated order-status: no short_code, PII, or Personr link |
| R-007 | Expired JWT → anonymous public payload (not hard 401 brick) |
| R-008 | Org data isolation when firm accounts exist |
| R-009 | Never remint competitor historical KYCs as FreeAML results |
| R-010 | Migration = parallel run + new-matters-only + async concierge |
| R-011 | New Supabase changes = **new** migration files only |
| R-012 | No OTPs / ID docs / Personr payloads in analytics |
