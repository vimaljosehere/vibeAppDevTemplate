# Page inventory

Full live inventory aligned to FreeAML / complyin30 routes. **URLs frozen** during strangler.

Canonical specs: [`specs/`](./specs/). Template: [`PAGE-TEMPLATE.md`](./PAGE-TEMPLATE.md).

| ID | Name | URL | Spec |
|---|---|---|---|
| PUB-01 | Homepage | `/` | specs/PUB-01.md |
| PUB-02 | Pricing | `/pricing` | specs/PUB-02.md |
| PUB-03 | Pro marketing | `/pro` | specs/PUB-03.md |
| PUB-04 | Pro signup | `/pro/signup` | specs/PUB-04.md |
| PUB-05 | Pro welcome | `/pro/welcome` | specs/PUB-05.md |
| PUB-06 | Compare | `/compare` | specs/PUB-06.md |
| PUB-07 | Blog index | `/blog` | specs/PUB-07.md |
| PUB-08 | AML check | `/aml-check` | specs/PUB-08.md |
| PUB-09 | AML check cost | `/aml-check-cost` | specs/PUB-09.md |
| PUB-10 | KYC check | `/kyc-check` | specs/PUB-10.md |
| PUB-11 | KYC check cost | `/kyc-check-cost` | specs/PUB-11.md |
| PUB-12 | Free AML check | `/free-aml-check` | specs/PUB-12.md |
| PUB-13 | Free KYC check | `/free-kyc-check` | specs/PUB-13.md |
| PUB-14 | Free identity verification | `/free-identity-verification` | specs/PUB-14.md |
| PUB-15 | Identity verification | `/identity-verification` | specs/PUB-15.md |
| PUB-16 | Entity verification | `/entity-verification` | specs/PUB-16.md |
| PUB-17 | UBO verification | `/ubo-verification` | specs/PUB-17.md |
| PUB-18 | Customer due diligence | `/customer-due-diligence` | specs/PUB-18.md |
| PUB-19 | CDD report | `/cdd-report` | specs/PUB-19.md |
| PUB-20 | AUSTRAC compliance | `/austrac-compliance` | specs/PUB-20.md |
| PUB-21 | AML/CTF compliance | `/aml-ctf-compliance` | specs/PUB-21.md |
| PUB-22 | AML software Australia | `/aml-software-australia` | specs/PUB-22.md |
| PUB-23 | Tranche 2 | `/tranche-2` | specs/PUB-23.md |
| PUB-24 | Tranche 2 compliance | `/tranche-2-compliance` | specs/PUB-24.md |
| PUB-25 | Conveyancer | `/conveyancer` | specs/PUB-25.md |
| PUB-26 | Accountants | `/accountants` | specs/PUB-26.md |
| PUB-27 | Lawyers | `/lawyers` | specs/PUB-27.md |
| PUB-28 | Real estate | `/real-estate` | specs/PUB-28.md |
| PUB-29 | Jewellers | `/jewellers` | specs/PUB-29.md |
| PUB-30 | Vs EasyAML | `/vs/easyaml` | specs/PUB-30.md |
| PUB-31 | Vs FirstAML | `/vs/firstaml` | specs/PUB-31.md |
| PUB-32 | Sixstep | `/sixstep` | specs/PUB-32.md |
| PUB-33 | Compliance hub | `/compliance` | specs/PUB-33.md |
| PUB-34 | Compliance docs | `/compliance-docs` | specs/PUB-34.md |
| PUB-35 | Reports | `/reports` | specs/PUB-35.md |
| PUB-36 | Training index | `/training` | specs/PUB-36.md |
| PUB-37 | Training module | `/training/[moduleId]` | specs/PUB-37.md |
| PUB-38 | Program (redirect) | `/program` | specs/PUB-38.md |
| PUB-39 | Risk assessment (redirect) | `/risk-assessment` | specs/PUB-39.md |
| PUB-40 | Components kitchen sink | `/components` | specs/PUB-40.md |
| CLI-01 | Client verification/pay hub | `/v/[code]` | specs/CLI-01.md |
| CLI-02 | Gated Personr continue (PLANNED) | `/continue` | specs/CLI-02.md |
| CLI-03 | UBO capture | `/u/[code]` | specs/CLI-03.md |
| CLI-04 | Short-code results entry | `/r/[code]` | specs/CLI-04.md |
| PAR-01 | Results by id | `/results/[id]` | specs/PAR-01.md |
| PAR-02 | OTP login (/my) | `/my` | specs/PAR-02.md |
| PAR-03 | My dashboard | `/my/dashboard` | specs/PAR-03.md |
| PAR-04 | My verifications | `/my/verifications` | specs/PAR-04.md |
| PAR-05 | My compliance | `/my/compliance` | specs/PAR-05.md |
| PAR-06 | My references | `/my/references` | specs/PAR-06.md |
| PAR-07 | My settings | `/my/settings` | specs/PAR-07.md |
| PAR-08 | My team | `/my/team` | specs/PAR-08.md |
| ORG-01 | Create org | `/org/create` | specs/ORG-01.md |
| ORG-02 | Org home | `/org/[code]` | specs/ORG-02.md |
| INT-01 | Test PDFs | `/testpdfs` | specs/INT-01.md |
| INT-02 | Internal | `/internal` | specs/INT-02.md |

## Notes
- PUB-07: child blog posts exist under `/blog/...` (freeze; not each inventoried).
- PUB-38 `/program` and PUB-39 `/risk-assessment` are redirects — confirm targets in live app.
- CLI-02 `/continue` is **planned** (Module 1b).
- CLI-04 `/r/[code]`: confirm live existence or alias to `/results/[id]`.
- Firm Clerk auth is separate; `/v` stays login-free.
- Delete obsolete thin `CLI-01-verification.md` at pages root — use `specs/CLI-01.md`.
