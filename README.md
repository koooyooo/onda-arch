# おんだ建築事務所 ホームページ

一級建築士 恩田耕爾によるおんだ建築事務所のウェブサイト（プロトタイプ）。
ビルド不要の静的サイト（HTML / CSS / JS）として構成しており、GitHub Pagesでそのまま公開できます。

## ディレクトリ構成

```
.
├── index.html          # サイト本体（1ページ構成）
├── assets/
│   ├── css/style.css   # スタイル
│   ├── js/main.js      # ナビゲーション・スクロールアニメーション
│   └── img/
│       └── profile.jpg # プロフィール写真
└── docs/                # 元の資料画像など
```

## ローカルでの確認方法

```
cd onda-arch
python3 -m http.server 8000
```

ブラウザで `http://localhost:8000` を開いて確認できます。

## GitHub Pagesでの公開手順

1. このディレクトリをGitHubリポジトリにする
   ```
   git init
   git add .
   git commit -m "Initial website prototype"
   git branch -M main
   git remote add origin <あなたのリポジトリURL>
   git push -u origin main
   ```
2. GitHubのリポジトリ画面で **Settings > Pages** を開く
3. **Source** を `Deploy from a branch` にし、ブランチを `main` / フォルダを `/ (root)` に設定
4. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される

独自ドメインを使う場合は、リポジトリ直下に `CNAME` ファイルを追加し、ドメインを1行記載してください。

## 未着手・要対応の項目（プロトタイプにつき）

- `works` セクションの実績写真・詳細（現在はプレースホルダー）
- プロフィールの経歴・沿革の詳細
- お問い合わせフォームの送信先設定（Formspreeなど外部フォームサービス、またはメーラー連携が必要。GitHub Pagesは静的ホスティングのためサーバー側処理ができません）

## 反映済みの基本情報

事務所名・所在地・電話/FAX・営業時間・定休日・アクセス・メールアドレス・主要業務内容は、以下の情報をもとに反映済みです。
- https://www.navida.ne.jp/snavi/5375_1.html （事務所情報）
- メールアドレスはユーザー指定の `koji@onda-arch.com`
