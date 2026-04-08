# dunksoft.net — Smart Life Styles®

色彩日本語・天然色漢字INDEX・歴史継承デモ。  
言語と記憶をつなぐプロジェクト群。

## ファイル構成

```
dunksoft.net/
├── index.html          ← トップページ
└── demos/
    ├── shurijo.html        ← 首里城 色彩日本語デモ
    ├── navy-bunker.html    ← 旧海軍司令部壕デモ
    └── colorful-jp.html    ← 色彩日本語プロジェクト紹介
```

## GitHub → Cloudflare Pages セットアップ手順

### Step 1: GitHubリポジトリ作成
1. https://github.com/robertohoshino にアクセス
2. 「New repository」→ 名前: `dunksoft-net`
3. Public / README追加なし → 「Create repository」

### Step 2: ファイルをpush
```bash
git init
git add .
git commit -m "初回公開 — Smart Life Styles サイト"
git remote add origin https://github.com/robertohoshino/dunksoft-net.git
git push -u origin main
```

### Step 3: Cloudflare Pagesに接続
1. https://dash.cloudflare.com にログイン
2. 「Pages」→「Create a project」→「Connect to Git」
3. GitHubアカウント連携 → `dunksoft-net` を選択
4. Build settings: フレームワーク「なし」、ビルドコマンド空欄、出力ディレクトリ `/`
5. 「Save and Deploy」

### Step 4: お名前.comのDNS設定
Cloudflare Pages のドメイン設定で表示される CNAME を
お名前.comの管理画面でdunksoft.netに設定する。

```
種別: CNAME
ホスト名: @（または dunksoft.net）
VALUE: [プロジェクト名].pages.dev
```

### 新しいデモを追加するとき
1. `demos/` フォルダに HTMLファイルを追加
2. `index.html` のデモグリッドにカードを1枚追加
3. GitHubにpush → 自動でdunksoft.netに反映

## © Dunksoft / Roberto Hoshino
色彩日本語 COLORFUL JAPANESE™ | Smart Life Styles® | Love your life, love your time®
