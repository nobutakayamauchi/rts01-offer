# risingson Sales / Offer Hub

このrepoは、risingson が外部向けに販売する商品・サービスの静的な営業・法定表記ハブです。

元の「AI開発迷子リセット / RTS Project Audit Offer」のLPは維持しつつ、今後は複数商品を扱うため、商品実装と販売情報を分離して管理します。

このrepoは商品本体・delivery runtime・commercial coreではありません。各商品の機能事実は、その商品の実装repoを正本とします。

## GitHub Pages

GitHub Pages の `/root` 公開を前提にしています。

```text
https://nobutakayamauchi.github.io/rts01-offer/
```

`.nojekyll` を配置しているため、Jekyll変換なしで静的ファイルを公開します。

## 主要導線

```text
/                              既存メインLP
/products/index.html           商品一覧
/products/catalog.json         商品レジストリ
/legal/index.html              販売者共通の法定表記入口
/legal/products/<slug>.html    商品別の特定商取引法に基づく表記
/offer/<slug>.html             このrepoでLPを持つ商品の販売ページ
```

既存の `/legal/tokushoho.html` と `/offer/initial-flow.html` は互換維持します。

## 新商品を追加するとき

1. `products/catalog.json` に商品を1件追加する。
2. `legal/products/<slug>.html` を追加する。
3. `products/index.html` に商品カードを追加する。
4. LPをこのrepoに置く場合は `offer/<slug>.html` を追加する。Brain / note 等で売る場合は外部URLを登録する。
5. LP / 販売記事から、その商品の特商法ページへリンクする。
6. 商品仕様は販売repoの記憶で書かず、実装repoを確認してから表記する。

詳細は `docs/MULTI_PRODUCT_SALES_LEGAL.md` を参照してください。

## WebAI-Bridge の正本境界

- `nobutakayamauchi/WebAI-Bridge`: public product/runtime surface
- `nobutakayamauchi/WebAI-Bridge-Core`: private commercial/runtime core
- `rts01-offer`: sales copy / product catalog / legal disclosure

WebAI-Bridgeの実装仕様が販売文と食い違う場合は、実装repo側を確認して販売文を修正します。

## 共有時の注意

- APIキー、パスワード、秘密鍵をsales/legal repoへ置かない
- private coreの内容をそのまま公開しない
- 売上・利益・成果を保証する表現をしない
- 価格、提供時期、返品条件、追加料金は商品ごとに確認する

## ローカル確認

```bash
python3 -m http.server 8000
```

その後 `http://localhost:8000/` を開きます。
