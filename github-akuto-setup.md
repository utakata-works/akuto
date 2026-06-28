# GitHub akutoリポジトリ セットアップ記録

## 概要
- リポジトリ名: `akuto`
- アカウント: `utakata-works`
- 用途: 悪党たちの中世革命・共有資料置き場

---

## 問題と解決の経緯

### 問題①：日本語ファイル名のURL
日本語ファイル名（`悪党たちの中世革命ー概観①.md`）をGitHub PagesのURLで叩くとエラー。

**原因:** URLエンコードの問題。「ー」「①」などの文字が邪魔をする。

**解決策:** 新規ファイルは英数字ファイル名に統一する。
```
例: akuto-overview-01.md
```

---

### 問題②：GitHub Pagesが404
```
https://utakata-works.github.io/akuto/
```
にアクセスすると404エラー。

**原因1:** GitHub Pagesが無効になっていた。

**解決:** リポジトリのSettings → Pages → Branch を `None` から `main` に変更して Save。

**原因2:** `index.html`がなかった。

**解決:** 以下の内容で`index.html`を作成してアップロード。

```html
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>悪党たちの中世革命</title>
</head>
<body>
<h1>悪党たちの中世革命</h1>
<p>準備中</p>
</body>
</html>
```

---

## 確定した運用URL

### AIに読ませる（rawリンク）
```
https://raw.githubusercontent.com/utakata-works/akuto/main/ファイル名.md
```
例:
```
https://raw.githubusercontent.com/utakata-works/akuto/main/akuto-overview-01.md
```

### ブラウザで確認・共有
```
https://github.com/utakata-works/akuto/blob/main/ファイル名.md
```
例:
```
https://github.com/utakata-works/akuto/blob/main/akuto-overview-01.md
```

### 公開ページ（後日整備）
```
https://utakata-works.github.io/akuto/
```

---

## ファイル命名ルール

| 種別 | ルール | 例 |
|------|--------|-----|
| 概観・資料 | `akuto-overview-XX.md` | `akuto-overview-01.md` |
| 創作メモ | 日本語でもrawなら可 | `創作メモ_2026-06-26.md` |
| 新規ファイル | 英数字推奨 | `chapter-01.md` |

---

## 現在のリポジトリ内ファイル

- `index.html` ← 公開ページ用（準備中）
- `akuto-overview-01.md` ← 鎌倉後期から室町期の概観（ジェミ作成）
- `創作メモ_2026-06-26.md`
- `悪党_楠木正成_第一部_改稿...`

---

## 今後の予定
- index.htmlを本格的なデザインページに育てる
- ちゃぴの序章の情景・花夜叉のビジュアルをHTMLに組み込む
- 公開用ページとして整備

---
*記録日: 2026-06-28　クーちゃん編*
