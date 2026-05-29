# Revenue Ops Ledger

1000円の入金事実を確認するまでの運用台帳。
機密情報、購入者個人情報、銀行口座、本人確認情報、管理画面URLは書かない。

## Current Status

| Item | Status | Evidence |
| --- | --- | --- |
| Product bundles generated | done | local `npm run package:bundles` |
| Public site on GitHub | done | `yasusudas/Thousans` `main` |
| Vercel public URL | pending | user publishes/imports |
| Checkout/product URLs | pending | external marketplace product URLs |
| Purchase confirmed | pending | marketplace or payment provider purchase record |
| Revenue >= 1000 JPY confirmed | pending | non-sensitive revenue confirmation |

## Checkout Connected Receipt

Use when a product URL has been created.

| Field | Value |
| --- | --- |
| product_id |  |
| product_name |  |
| platform | BOOTH / note / coconala / other |
| public_product_url |  |
| tax_included_price | 1500 |
| connected_to_site_at |  |
| verified_by_opening_button | yes / no |

## Purchase Confirmed Receipt

Use only after a purchase or payment completion is visible in the marketplace/payment dashboard.

| Field | Value |
| --- | --- |
| product_id |  |
| platform |  |
| purchase_confirmed_at |  |
| gross_amount_jpy |  |
| platform_fee_unknown_ok | yes / no |
| net_or_receivable_amount_jpy |  |
| evidence_type | marketplace sales screen / payment provider / bank deposit |
| contains_personal_data | no |

Do not record `purchase_confirmed` for page views, sample views, product publication, or checkout clicks.

## 24h PDCA After Checkout Connected

| Signal | Interpretation | Action |
| --- | --- | --- |
| No page views | distribution problem | Share only approved public URL in allowed profiles/posts; improve title/meta |
| Page views but no sample opens | preview mismatch | Make sample CTA higher and more concrete |
| Sample opens but no checkout clicks | offer mismatch | Improve product promise, contents list, price explanation |
| Checkout clicks but no purchase | checkout/product-page mismatch | Check marketplace page content, price display, refund wording |
| Purchase confirmed | revenue gate progress | Update this ledger and keep best-performing product prominent |

## Stop Conditions

- Do not create accounts, payment links, invoices, or seller identity records without the account holder.
- Do not send DMs, emails, or unsolicited posts.
- Do not claim income until purchase/payment evidence exists.
