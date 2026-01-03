# AIメール秘書 ランディングページ

## 📁 ファイル構成

```
aimail-lp/
├── index.html          # メインHTMLファイル
├── style.css           # スタイルシート
├── script.js           # JavaScript（スクロールアニメーション等）
├── images/             # イラスト画像フォルダ
│   ├── hero-illustration.png
│   ├── problem-illustration.png
│   ├── feature-analysis.png
│   ├── feature-priority.png
│   └── feature-chatwork.png
└── README.md           # このファイル
```

## 🎨 デザイン特徴

- **カラースキーム**: 黄色系をメインに、オレンジ・ブルーをアクセントカラーとして使用
- **イラスト**: POPで親しみやすいAIロボットキャラクターを多用
- **レスポンシブ**: スマートフォン・タブレット・PCに対応
- **アニメーション**: スクロール時のフェードイン効果、ホバーエフェクト

## 🚀 デプロイ方法

### 方法1: aimail.becreative.co.jp にデプロイ

1. **DNSレコードの設定**
   - becreative.co.jp のDNS管理画面で、サブドメイン `aimail` のAレコードまたはCNAMEレコードを設定

2. **Webサーバーへのアップロード**
   - FTP/SFTP、またはGit経由で、Webサーバーの該当ディレクトリにファイルをアップロード
   - 例: `/var/www/aimail.becreative.co.jp/`

3. **Webサーバー設定**
   - Nginx/Apache等の設定ファイルで、`aimail.becreative.co.jp` のドキュメントルートを設定
   - SSL証明書（Let's Encrypt等）を設定

### 方法2: GitHub Pages でデプロイ（無料・簡単）

1. GitHubリポジトリを作成
2. このフォルダの内容をプッシュ
3. Settings > Pages で公開設定
4. カスタムドメイン `aimail.becreative.co.jp` を設定

### 方法3: Netlify/Vercel でデプロイ（無料・自動デプロイ）

1. Netlify または Vercel にサインアップ
2. このフォルダをドラッグ&ドロップでアップロード
3. カスタムドメイン `aimail.becreative.co.jp` を設定

## 🔧 カスタマイズ方法

### 色の変更

`style.css` の `:root` セクションで色変数を変更：

```css
:root {
    --primary-yellow: #FFD93D;    /* メインカラー */
    --accent-orange: #FF9F40;     /* アクセントカラー */
    --accent-blue: #4A90E2;       /* アクセントカラー2 */
}
```

### テキストの変更

`index.html` を開いて、各セクションのテキストを編集してください。

### 画像の変更

`images/` フォルダ内の画像を差し替えてください。ファイル名を変更する場合は、`index.html` 内の `<img src="images/xxx.png">` も合わせて変更してください。

## 📱 動作確認

ローカルで確認する場合：

```bash
# Pythonの簡易サーバーで確認
cd aimail-lp
python3 -m http.server 8000
# ブラウザで http://localhost:8000 を開く
```

## 🌐 リンク先の変更

現在、CTAボタンは `https://ai-auto-mailer.onrender.com` にリンクしています。
変更する場合は、`index.html` 内の以下の箇所を編集してください：

```html
<a href="https://ai-auto-mailer.onrender.com" class="cta-button-huge" target="_blank">
    無料で始める
</a>
```

## 📞 サポート

質問や問題がある場合は、開発者にお問い合わせください。
