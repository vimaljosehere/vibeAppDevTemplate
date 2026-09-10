# Technical architecture

- **App:** Next.js App Router on Vercel
- **Data:** Supabase Postgres
- **Payments:** Stripe Checkout + Connect
- **IDV:** Personr adapter module
- **Pattern:** Strangler — replace modules behind same public/webhook URLs

Modules (rebuild map): Core verification · Personr adapter · Payments · Pro/markup · Auth · Notifications · Reporting/PDF (P2) · Toolkit · Orgs · Marketing/SEO · Shared platform
