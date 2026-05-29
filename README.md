# ThousandYen Digital Kits

3つの低価格デジタル商品を並行運用し、1000円の初回売上を狙うためのVercel向け静的サイトです。

## Products

- 商品ページ即貼りテンプレ50
- 初回販売チェックリスト
- AI作業ログ・振り返りテンプレ集

## Commands

```bash
npm install
npm run check
npm run dev
```

## Revenue Gate

このリポジトリだけでは入金先を作れません。ココナラ、BOOTH、noteなどの本人アカウントで商品URLを作成し、`src/config.js` の `checkoutLinks` に貼ると購入ボタンとして動作します。
