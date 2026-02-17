# 🚀 GitHub Pagesデプロイ手順

画像9分割アプリをGitHub Pagesで公開する手順です。

## 📋 前提条件

- GitHubアカウントを持っていること
- Gitがインストールされていること

## 🔧 手順

### 1. GitHubで新しいリポジトリを作成

1. [GitHub](https://github.com)にログイン
2. 右上の「+」→「New repository」をクリック
3. 以下を入力:
   - **Repository name**: `image-splitter` (または好きな名前)
   - **Description**: `画像を3×3グリッドで9分割するWebアプリ`
   - **Public** を選択(GitHub Pages無料利用のため)
   - **Initialize this repository with** のチェックは**すべて外す**
4. 「Create repository」をクリック

### 2. ローカルリポジトリをGitHubにプッシュ

ターミナルで以下を実行:

```bash
cd /Users/kino/Developer/image-splitter

# 初回コミット
git commit -m "Initial commit: 画像9分割アプリ"

# GitHubリポジトリを追加(URLは自分のものに置き換え)
git remote add origin https://github.com/あなたのユーザー名/image-splitter.git

# プッシュ
git branch -M main
git push -u origin main
```

### 3. GitHub Pagesを有効化

1. GitHubのリポジトリページを開く
2. 「Settings」タブをクリック
3. 左サイドバーの「Pages」をクリック
4. **Source**セクションで:
   - Branch: `main` を選択
   - Folder: `/ (root)` を選択
5. 「Save」をクリック

### 4. デプロイ完了を確認

- 数分待つと、GitHub Pagesのセクションに以下のメッセージが表示されます:
  ```
  Your site is live at https://あなたのユーザー名.github.io/image-splitter/
  ```

- このURLをクリックしてアプリが動作することを確認!

## 🎉 完了!

これで世界中の人があなたのアプリを使えるようになりました!

## 📝 更新方法

アプリを更新したい場合:

```bash
cd /Users/kino/Developer/image-splitter

# ファイルを編集後
git add .
git commit -m "更新内容の説明"
git push

# 数分後に自動的にデプロイされます
```

## 🔗 シェア方法

### URLをシェア

```
https://あなたのユーザー名.github.io/image-splitter/
```

### SNSでシェア

**Twitter/X**:
```
画像を3×3グリッドで9分割できる無料Webアプリを作りました!
✨ ドラッグ&ドロップで簡単
🔒 完全にプライベート(サーバー送信なし)
💾 PNG最高品質

https://あなたのユーザー名.github.io/image-splitter/

#WebApp #画像編集 #無料ツール
```

**Note/Qiita**:
記事を書いてアプリの使い方や技術解説を投稿!

## 🌟 カスタムドメイン(オプション)

独自ドメインを使いたい場合:

1. ドメインを取得(例: `image-splitter.com`)
2. GitHub Pages設定で「Custom domain」に入力
3. DNSレコードを設定

詳細: [GitHub Pagesカスタムドメイン設定](https://docs.github.com/ja/pages/configuring-a-custom-domain-for-your-github-pages-site)

## 🐛 トラブルシューティング

### デプロイされない

- GitHub Pagesの設定を確認
- リポジトリがPublicになっているか確認
- 数分待ってから再度アクセス

### 404エラー

- `index.html`がリポジトリのルートにあるか確認
- ブランチ名が`main`になっているか確認

### 画像が分割されない

- ブラウザのコンソールでエラーを確認
- JSZipのCDNが読み込めているか確認

## 📚 参考リンク

- [GitHub Pages公式ドキュメント](https://docs.github.com/ja/pages)
- [Git基本コマンド](https://git-scm.com/docs)
