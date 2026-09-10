# Agent instructions (FreeAML)

Before writing code:
1. Read `docs/00-product/goals-non-goals.md` and `docs/08-business-rules/business-rules.md`
2. Match the **module** in `docs/13-roadmap/milestones.md` — do not widen scope
3. Freeze public SEO URLs and webhook paths unless the task says otherwise
4. Prefer strangler replacements behind existing routes over greenfield rewrites

Must not:
- Expose Personr raw URLs, OTPs, ID docs, or short codes on ungated APIs
- Hand-edit applied Supabase baseline migrations — add a **new** migration
- Remint historical competitor KYCs as FreeAML/Personr results
- Add outbound phone/SDR assumptions into product copy

Tagline constraint: **make AML dead simple** → 4-digit OTP (rate-limited); new short codes ≥12 chars.
