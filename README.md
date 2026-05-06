# AI開発迷子リセット LP

このrepoは、AIで作り散らかった開発プロジェクトを棚卸しし、進められる状態に戻す診断サービス「AI開発迷子リセット」の静的LPです。

内部的には `RTS Project Audit Offer` として位置づけています。

HTML/CSSのみで動作し、ビルド不要・依存追加なしで GitHub Pages の `/root` 公開に対応します。

## GitHub Pages公開手順

1. GitHubで `nobutakayamauchi/rts01-offer` を開く
2. `Settings` → `Pages` を開く
3. `Build and deployment` の `Source` を `Deploy from a branch` にする
4. `Branch` を公開したいブランチにする
5. 公開フォルダを `/root` にする
6. `Save` を押す
7. 数分後、以下のURLで公開を確認する

```text
https://nobutakayamauchi.github.io/rts01-offer/
```

`.nojekyll` を配置しているため、Jekyll変換なしで静的ファイルをそのまま公開できます。

## CTAリンク

CTAリンクは、現在 `ultimaterisingson@proton.me` 宛て（件名: `AI開発迷子リセット相談`）です。

```text
mailto:ultimaterisingson@proton.me?subject=AI開発迷子リセット相談
```

差し替える場合は、`index.html` 内の `CTA_LINK` コメント付近にあるCTAリンクの `href` を変更してください。Hero CTA、最終CTA、Footerのお問い合わせリンクは同じ申し込み先に揃えてください。

## 決済について

現時点ではLP上に直接決済リンクは置きません。

申し込み後すぐに決済は発生せず、まずはメールで内容を確認し、対応可否・納期・支払い方法を個別に案内します。

支払い方法は、銀行振込 / Stripe決済リンク / Square請求書に対応予定です。

## ローカル確認方法

ブラウザで直接 `index.html` を開けば確認できます。

簡易サーバーで確認する場合は、repo rootで次のコマンドを実行してください。

```bash
python3 -m http.server 8000
```

その後、ブラウザで以下を開きます。

```text
http://localhost:8000/
```

## ファイル構成

```text
.
├── index.html
├── assets/
│   └── style.css
├── .nojekyll
└── README.md
```
