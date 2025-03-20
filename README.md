# Git コマンド一覧

## 初期化
```
git init
```

## コミット
```
git add .
git commit -m "コミットメッセージ"
```
ファイル名を指定。"."は全変更ファイル。

## 変更状況を確認
```
git diff
```
リポジトリとワークツリーの差分をチェック。
```
git diff --staged
```
リポジトリとステージの差分をチェック。
```
git status
```
変更ファイルを確認。

## 変更履歴の確認
```
git log
```

## 変更を元に戻す
```
git restore "ファイル名"
```
ワークツリーの変更を取り消す。
```
git restore --staged "ファイル名"
```
ステージに挙げた変更をワークツリーに戻す。
```
git checkout "ファイル名"
```
指定したファイルの変更を破棄する。

## ブランチの操作
### ブランチの作成
```
git branch "ブランチ名"
```
### ブランチの一覧を表示
```
git branch
git branch -a
```
### ブランチを切り替える
```
git switch "ブランチ名"
git switch -c "ブランチ名"
```
-cはブランチを新規作成して切り替える。

### ブランチをマージ
```
git merge "ブランチ名"
git merge  origin/"ブランチ名"
```

## リモートリポジトリの操作
### リモートリポジトリを追加
```
git remote add origin URL
```

### リモートリポジトリにプッシュ
```
git push origin "ブランチ名"
```

### リモートリポジトリから情報取得
```
git pull origin "ブランチ名"
git pull
```
※省略可能
```
git fetch origin
```

## 直前のコミットの状態に戻す
```
git reset --hard HEAD^
```
