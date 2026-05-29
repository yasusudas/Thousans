# ThousandYen Digital Kits

3つの低価格デジタル商品について、初回販売の準備と導線検証を行うためのVercel向け静的サイトです。

## Products

- 商品ページ即貼りテンプレ50: `/products/listing-template-pack.html`
- 初回販売チェックリスト: `/products/first-sale-checklist.html`
- AI作業ログ・振り返りテンプレ集: `/products/ai-worklog-template.html`

## Free Samples

- `/bundles/listing-template-pack-preview.md`
- `/bundles/first-sale-checklist-sample.md`
- `/bundles/ai-worklog-template-sample.md`

## Deploy

VercelではこのリポジトリをそのままImportしてください。単一の `index.html` と静的HTML/Markdownで動くため、Build Commandは空、Output Directoryも空で問題ありません。

## Revenue Gate

このリポジトリだけでは入金先を作れません。ココナラ、BOOTH、noteなどの本人アカウントで商品URLを作成し、購入ボタンのURLへ接続すると販売導線になります。

商品URLができたら `operations/checkout-url-receipt.md` に非機密のURLだけを記録し、`index.html` の `checkoutLinks` に貼ると購入ボタンとして動作します。

## Safety Notes

- 価格は税込表示を使う。
- 購入・決済・提供条件の最終確認はリンク先の販売ページで行う。
- 売上、審査通過、法的適合、特定成果は保証しない。
- 入金または購入完了が確認できるまで、売上達成とは扱わない。
