# Checkout URL Receipt

商品URLができた瞬間に、購入ボタンへ接続するための非機密メモ。
アカウントID、銀行口座、本人確認情報、管理画面URL、購入者情報は書かない。

## 入力欄

| Product | Platform | Public product URL | Tax-included price | Status |
| --- | --- | --- | ---: | --- |
| listing-template-pack |  |  | 1500 | pending |
| first-sale-checklist |  |  | 1500 | pending |
| ai-worklog-template |  |  | 1500 | pending |

## index.html patch

`index.html` の `checkoutLinks` に公開商品URLだけを貼る。

```js
const checkoutLinks = {
  listing: "https://販売先の商品URL",
  checklist: "https://販売先の商品URL",
  worklog: "https://販売先の商品URL"
};
```

## post-deploy verification

- [ ] Vercel公開URLを開ける
- [ ] 各商品の購入ボタンがリンク先の商品ページを開く
- [ ] リンク先で税込価格、支払方法、提供時期、返金可否、販売者情報、問い合わせ先を確認できる
- [ ] 無料ツールの入力内容が外部送信されない

## purchase_confirmed にしてよい条件

次のいずれかを確認できるまで、入金済みや売上達成とは記録しない。

- 販売プラットフォーム上の購入完了/売上管理画面で、対象商品の購入が確認できる
- 決済サービス上で対象商品の支払い完了が確認できる
- 振込または売上金反映を本人が確認した

未入金、未購入、クリックのみ、商品公開のみの場合は `purchase_confirmed` ではなく `checkout_connected` または `checkout_click` として扱う。
