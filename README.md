# 🎨 画像9分割アプリ

画像を3×3グリッドで9分割できる無料のWebアプリケーションです。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ 特徴

- 🎨 **美しいUI**: モダンなグラデーションデザイン
- 📸 **ドラッグ&ドロップ対応**: 簡単に画像をアップロード
- 👀 **リアルタイムプレビュー**: 分割結果を即座に確認
- 💾 **PNG最高品質**: ロスレス形式で保存
- 🔒 **完全にプライベート**: 画像はサーバーに送信されません
- 📦 **ZIP一括ダウンロード**: 9枚まとめてダウンロード
- 🌐 **インストール不要**: ブラウザだけで動作

## 🚀 使い方

1. [デモページ](https://あなたのユーザー名.github.io/image-splitter/)を開く
2. 画像をドラッグ&ドロップ、またはクリックして選択
3. 自動的に9分割されプレビュー表示
4. 「ダウンロード」ボタンでZIPファイルを取得

## 📁 出力ファイル

ダウンロードされる`split_images.zip`には以下が含まれます:

```
split_images.zip
├── panel_01.png (左上)
├── panel_02.png (上中央)
├── panel_03.png (右上)
├── panel_04.png (左中央)
├── panel_05.png (中央)
├── panel_06.png (右中央)
├── panel_07.png (左下)
├── panel_08.png (下中央)
└── panel_09.png (右下)
```

## 🔒 プライバシー

- **サーバーへの送信なし**: すべての処理はブラウザ内で完結
- **データ保存なし**: 画像データは一切保存されません
- **第三者提供なし**: 画像が外部に送信されることはありません
- **Cookie不使用**: トラッキングなし

詳細は[プライバシーポリシー](https://あなたのユーザー名.github.io/image-splitter/#privacy)をご覧ください。

## 🛠️ 技術スタック

- **HTML5 Canvas API**: 画像の分割処理
- **File API**: ローカルファイルの読み込み
- **JSZip**: ZIP形式でのダウンロード
- **Vanilla JavaScript**: フレームワーク不要

## 📦 ローカルで実行

```bash
# リポジトリをクローン
git clone https://github.com/あなたのユーザー名/image-splitter.git

# ディレクトリに移動
cd image-splitter

# ブラウザで開く
open image_splitter.html
```

または、単に`image_splitter.html`をブラウザにドラッグ&ドロップするだけでOKです!

## 🌐 デプロイ

### GitHub Pagesでデプロイ

1. このリポジトリをフォーク
2. Settings → Pages
3. Source: `main` ブランチ
4. Save

数分後、`https://あなたのユーザー名.github.io/image-splitter/`でアクセス可能になります。

### Vercelでデプロイ

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/あなたのユーザー名/image-splitter)

### Netlifyでデプロイ

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/あなたのユーザー名/image-splitter)

## 📄 ライセンス

MIT License - 詳細は[LICENSE](LICENSE)ファイルをご覧ください。

## 🤝 コントリビューション

プルリクエストを歓迎します!大きな変更の場合は、まずIssueを開いて変更内容を議論してください。

## 📮 お問い合わせ

質問や提案がある場合は、[GitHub Issues](https://github.com/あなたのユーザー名/image-splitter/issues)でお知らせください。

## 🎉 謝辞

- [JSZip](https://stuk.github.io/jszip/) - ZIP生成ライブラリ
- すべてのコントリビューターに感謝!

---

Made with ❤️ by [あなたの名前](https://github.com/あなたのユーザー名)
