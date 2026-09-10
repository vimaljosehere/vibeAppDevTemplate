# Data model (logical)

Core: **Organisation** (future) · **User/Party** · **Order** · **Subject** · **Verification leg** · **Screening result** · **Payment** · **Audit/OTP attempts**

Order holds: type, payer, amounts, markup, short_code, contacts, verification_status, Personr refs (server-only), Stripe ids.
