# ThousandYen PDCA Board

## North Star

- Target: confirmed revenue >= 1000 JPY
- Current confirmed revenue: 0 JPY
- Current blocker: payment account / checkout URL is not connected
- Revenue ledger: `operations/revenue-ops-ledger.md`

## Product Lanes

| Product | Price | Stage | Primary metric | Next action |
| --- | ---: | --- | --- | --- |
| 商品ページ即貼りテンプレ50 | 税込1500 | product-ready / checkout-blocked | tool_run, sample_open, checkout_click | ココナラ/BOOTH/note URLを接続 |
| 初回販売チェックリスト | 税込1500 | product-ready / checkout-blocked | tool_run, sample_open, checkout_click | ココナラ/BOOTH/note URLを接続 |
| AI作業ログ・振り返りテンプレ集 | 税込1500 | product-ready / checkout-blocked | tool_run, sample_open, checkout_click | ココナラ/BOOTH/note URLを接続 |

## Event Taxonomy

- `tool_open`: 商品ツールを開いた
- `tool_run`: 無料生成ツールを使った
- `sample_open`: サンプルを開いた
- `checkout_click`: 購入ボタンを押した
- `purchase_confirmed`: 入金/購入事実を確認した

## PDCA Loop

### Plan

3商品を税込1500円に設定し、無料ツールで価値を先出しして有料bundleへ誘導する。

### Do

公開サイトで3商品を並行表示し、サンプル閲覧と決済クリックを記録する。

### Check

クリックがない場合は商品名と無料ツールの入力項目を変更する。クリックがあるのに購入がない場合は価格、返金可否の見せ方、サンプル内容を変更する。

### Act

最も `sample_download -> checkout_click` 率が高い商品に先に決済導線と投稿導線を集中させる。

## Revenue Confirmation Rule

`purchase_confirmed` は、販売プラットフォームまたは決済サービスで対象商品の購入完了を確認した場合だけ記録する。クリック、商品公開、問い合わせ、サンプル閲覧は売上として扱わない。
