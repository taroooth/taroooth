# ひらがじゃん デプロイ手順

ひらがじゃんを GitHub Pages にデプロイする手順です。

## 公開 URL

```
https://taroooth.github.io/hirajan/
```

---

## 初回セットアップ

### 1. リポジトリを作成する

1. https://github.com/new を開く
2. 以下の設定で作成する
   - Repository name: `hirajan`
   - Visibility: **Public**
   - README は追加しない
3. 「Create repository」をクリック

### 2. ファイルをアップロードする

1. 作成したリポジトリを開く
2. 「Add file」→「Upload files」をクリック
3. `index.html` をドラッグ＆ドロップ
4. 「Commit changes」をクリック

### 3. GitHub Pages を有効化する

1. リポジトリの「Settings」タブを開く
2. 左メニューの「Pages」をクリック
3. Source を **Deploy from a branch** に設定
4. Branch: **main** / フォルダ: **/ (root)**
5. 「Save」をクリック

数分後に https://taroooth.github.io/hirajan/ で公開されます。

---

## 更新時の手順

`index.html` を変更したら以下のいずれかでデプロイします。

### GitHub の Web UI から更新する場合

1. リポジトリの `index.html` を開く
2. 鉛筆アイコン（Edit）をクリック
3. 内容を編集して「Commit changes」

### ローカルから git push する場合

```bash
git add index.html
git commit -m "更新内容のメモ"
git push origin main
```

push すると GitHub Pages が自動で再デプロイします（通常 1〜2 分）。

---

## デプロイ状況の確認

リポジトリの「Actions」タブを開くと、デプロイの進捗と成否を確認できます。

- `pages build and deployment` が **success** になれば公開完了

---

## バージョン管理

`index.html` 内の以下の箇所でバージョン番号を管理しています。

```html
<div style="...">v1.2.0</div>
```

更新時はバージョン番号も合わせて更新してください（例: v1.2.0 → v1.3.0）。
