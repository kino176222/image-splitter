# 🎓 中学生でも分かる!GitHub CLIで画像9分割アプリを公開する方法

このドキュメントでは、GitHub CLIを使って画像9分割アプリを世界中に公開する方法を、中学生でも分かるように解説します!

## 🤔 そもそもGitHub CLIって何?

**GitHub CLI (gh)** は、ターミナル(黒い画面)からGitHubを操作できる便利なツールです。

### 普通の方法 vs GitHub CLI

**普通の方法:**
1. ブラウザでGitHubを開く
2. 「New repository」をクリック
3. 名前を入力
4. 「Create」をクリック
5. コマンドをコピペ
6. Settings → Pagesを開く
7. 設定を変更...

**GitHub CLIを使う方法:**
```bash
gh repo create image-splitter --public --push
gh api repos/あなたの名前/image-splitter/pages -X POST ...
```

たった2行で完了!✨

## 📚 用語解説

### Git(ギット)
- **何?**: ファイルの変更履歴を記録するツール
- **例え**: タイムマシン付きのUSBメモリ
- **できること**: 「昨日のバージョンに戻す」「誰がいつ変更したか見る」

### GitHub(ギットハブ)
- **何?**: Gitで管理したファイルをインターネット上に保存するサービス
- **例え**: Googleドライブのプログラマー版
- **できること**: コードを公開、共同作業、無料でWebサイト公開

### GitHub Pages(ギットハブ ページズ)
- **何?**: GitHubで無料でWebサイトを公開できる機能
- **例え**: 無料のレンタルサーバー
- **できること**: HTMLファイルを置くだけで世界中からアクセス可能に

### CLI(シーエルアイ)
- **何?**: Command Line Interface(コマンドライン インターフェース)の略
- **例え**: マウスを使わず、キーボードだけで操作する方法
- **なぜ使う?**: 慣れると超速い!自動化もできる!

## 🚀 実際にやったこと(ステップバイステップ)

### ステップ1: GitHub CLIをインストール

```bash
brew install gh
```

**何が起こった?**
- Homebrew(ホームブリュー)というアプリ管理ツールを使って、GitHub CLIをインストール
- Homebrewは「App Storeのターミナル版」みたいなもの

**時間**: 約1〜2分

### ステップ2: GitHubにログイン

```bash
gh auth login
```

**何が起こった?**
1. 「どこのGitHubを使う?」→ GitHub.com を選択
2. 「HTTPSとSSH、どっち?」→ HTTPS を選択(簡単な方)
3. 「Gitの認証もする?」→ Yes
4. 「どうやってログインする?」→ ブラウザでログイン
5. ワンタイムコード(9A29-2D35みたいなやつ)が表示される
6. ブラウザが開いて、コードを入力
7. 「Authorize(許可する)」をクリック
8. ログイン完了!✨

**時間**: 約30秒

### ステップ3: ファイルをコミット

```bash
git commit -m "Initial commit: 画像9分割アプリ"
```

**何が起こった?**
- 作ったファイル(index.html, README.md, LICENSE)を「セーブポイント」として記録
- `-m "メッセージ"` は「このセーブポイントの説明」

**例え**: ゲームのセーブデータに「ボス倒した後」みたいな名前をつける感じ

### ステップ4: GitHubにリポジトリを作成してプッシュ

```bash
gh repo create image-splitter --public --source=. --remote=origin --push
```

**何が起こった?**
- `gh repo create`: GitHubに新しいリポジトリ(プロジェクトの保管場所)を作成
- `image-splitter`: リポジトリの名前
- `--public`: 誰でも見られる公開設定
- `--source=.`: 今いるフォルダの中身を使う
- `--remote=origin`: GitHubのリポジトリを「origin」という名前で登録
- `--push`: ファイルをGitHubにアップロード

**結果**: https://github.com/kino176222/image-splitter が作成された!

### ステップ5: GitHub Pagesを有効化

```bash
gh api repos/kino176222/image-splitter/pages -X POST -F 'source[branch]=main' -F 'source[path]=/'
```

**何が起こった?**
- `gh api`: GitHub APIを直接叩く(高度な操作)
- `repos/.../pages`: GitHub Pagesの設定を変更
- `-X POST`: 「新しく作る」という命令
- `source[branch]=main`: mainブランチ(メインの作業場所)を使う
- `source[path]=/`: ルートフォルダ(一番上のフォルダ)を公開

**結果**: https://kino176222.github.io/image-splitter/ で公開開始!

## 🎉 完成!

数分待つと、以下のURLでアプリが使えるようになります:

**https://kino176222.github.io/image-splitter/**

## 🔄 更新する方法

アプリを改良したら、以下のコマンドで更新できます:

```bash
# 1. 変更をステージング(準備)
git add .

# 2. コミット(セーブ)
git commit -m "更新内容の説明"

# 3. プッシュ(アップロード)
git push

# 数分後に自動的に反映されます!
```

## 💡 よくある質問

### Q1: GitHub CLIを使わないとダメ?

**A**: いいえ!ブラウザでも同じことができます。でもGitHub CLIの方が:
- 速い(クリック不要)
- 自動化できる
- かっこいい😎

### Q2: お金かかる?

**A**: 完全無料!GitHub Pagesは無料で使えます。

### Q3: 独自ドメイン(example.comみたいなやつ)使える?

**A**: 使えます!ドメインを買って、GitHub Pagesの設定で追加するだけ。

### Q4: アクセス数に制限ある?

**A**: あります。月100GBまで。でも個人のアプリなら全然余裕!

### Q5: HTTPSになる?

**A**: 自動的にHTTPSになります!安全!🔒

## 🎓 もっと学びたい人へ

### おすすめリンク

- [GitHub公式ドキュメント(日本語)](https://docs.github.com/ja)
- [GitHub CLI公式サイト](https://cli.github.com/)
- [Git入門(サル先生)](https://backlog.com/ja/git-tutorial/)

### 次のステップ

1. **カスタムドメインを設定**: 自分だけのURLを使う
2. **GitHub Actionsを学ぶ**: 自動テスト、自動デプロイ
3. **オープンソースに貢献**: 他の人のプロジェクトを手伝う

## 🌟 まとめ

GitHub CLIを使えば、たった5つのコマンドで:
1. ✅ インストール
2. ✅ ログイン
3. ✅ コミット
4. ✅ リポジトリ作成&プッシュ
5. ✅ GitHub Pages有効化

世界中に自分のWebアプリを公開できます!

**所要時間**: 約5分
**難易度**: ⭐⭐☆☆☆ (慣れれば簡単!)
**かっこよさ**: ⭐⭐⭐⭐⭐

---

作成日: 2025年12月20日  
作成者: Antigravity AI Assistant
