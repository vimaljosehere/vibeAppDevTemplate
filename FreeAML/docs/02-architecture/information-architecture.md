# Information architecture

```
PUBLIC SITE          APP (party/firm)           CLIENT
marketing/SEO   →    dashboard / results   →    /v/{code}
toolkit docs         new check / orders         pay (if client-pays)
pricing              firm settings (later)      ID provider (Personr)
```

Money path: create order → Stripe pay → mint Personr only when paid → client completes → webhook updates status → report/export.
