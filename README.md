# AI開発迷子リセット LP

このrepoは、AIで作り散らかった開発プロジェクトを棚卸しし、進められる状態に戻す診断サービス「AI開発迷子リセット」の静的LPです。

内部的には `RTS Project Audit Offer` として位置づけています。

HTML/CSSのみで動作し、ビルド不要・依存追加なしで GitHub Pages の `/root` 公開に対応します。

## LP改善メモ

- スマホ初見で対象者が伝わるように、Heroに「GitHub repoが増えすぎて、何が本体かわからなくなった人へ。」という悩み直撃コピーを追加しています。
- ライト診断 9,800円を最初の選択肢として見つけやすくするため、料金カードに「まずはこれ」ラベルを付けています。
- 診断イメージをBefore / Afterより前に置き、納品される整理結果を早めに伝える構成にしています。

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
mailto:ultimaterisingson@proton.me?subject=AI%E9%96%8B%E7%99%BA%E8%BF%B7%E5%AD%90%E3%83%AA%E3%82%BB%E3%83%83%E3%83%88%E7%9B%B8%E8%AB%87
```

差し替える場合は、`index.html` 内の `CTA_LINK` コメント付近にあるCTAリンクの `href` を変更してください。Hero CTA、最終CTA、Footerのお問い合わせリンクは同じ申し込み先に揃えてください。

## 共有時の注意

- APIキー、パスワード、秘密鍵、個人情報は送らないでください。
- private repoを共有する場合は、必要な範囲だけ共有する運用です。
- 共有が難しい場合は、repo一覧、README、画面スクショ、構成メモ、困っていることの箇条書きでも確認できます。
- このLPはRTSの再構成・実行履歴・意思決定整理の考え方を使った外向き診断サービスであり、RTS Coreそのものを販売するものではありません。

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
