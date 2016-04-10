# Git Flowの練習

## ブランチの作成
developの作成

```
git branch develop
git push -u origin develop
```

pushした時パスワードを求められるのでgithubアカウントのパスワードを入力する。


同様にrelease、hotfix、featureを作成する。←明示的に作成しなくてもいい

```
git branch ブランチ名
git push -u origin ブランチ名
```


## featureの開始

1.featureブランチを作成する

```
git checkout -b featureブランチ名 develop
```

git checkoutはリモートからブランチをチェックアウトしてくる。
-bをつけるとブランチがない場合に新規作成してチェックアウトする。


2.featureを空コミットする

```
git commit --allow-empty
```

3.プルリクエストを作成する

```
git push -u origin featureブランチ名
```

## 変更を追加・コミットする

1.git statusで変更を確認、git addでステージにファイルを追加、そしてコミットする。

```
git status
git add <some-file>
git commit
```

2.リモートへpushする。

```
git push
```

または

```
git push -u origin featureブランチ名
```

## リモートの変更をローカルに同期する

```
git fetch origin
```

## リモートの変更を取り込む

リモートからpullします。

```
git pull
```

カレントがfeatureの時に別のブランチの変更をfeatureにマージします。

```
git merge ブランチ名
```
