# Marp 基本設定ガイド

Marpスライドを作成する際の基本的な設定と使い方をまとめたガイドです。

## 基本構造

```markdown
---
marp: true
theme: default
paginate: true
header: 'ヘッダーテキスト'
footer: 'フッターテキスト'
---

# スライドタイトル

スライドの内容

---

# 次のスライド

`---` で区切ると新しいスライドになります
```

## フロントマター設定

| 設定項目 | 説明 | 例 |
|---------|------|-----|
| `marp` | Marpを有効化 | `true` |
| `theme` | テーマ指定 | `default`, `gaia`, `uncover` |
| `paginate` | ページ番号表示 | `true` / `false` |
| `header` | 全スライドのヘッダー | `'ヘッダーテキスト'` |
| `footer` | 全スライドのフッター | `'フッターテキスト'` |
| `size` | スライドサイズ | `16:9`, `4:3`, `A4` |
| `style` | カスタムCSS | （下記参照） |

## スタイルの基本テンプレート

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&display=swap');
  
  /* 全体設定 */
  section {
    font-family: 'Noto Sans JP', sans-serif;
    background-color: #ffffff;
    color: #333333;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #2563eb;
    font-weight: 700;
  }
  
  h2 {
    color: #1e40af;
    font-weight: 700;
  }
  
  /* リンクスタイル */
  a {
    color: #3b82f6;
  }
  
  /* コードブロック */
  code {
    background-color: #f3f4f6;
    border-radius: 4px;
    padding: 2px 6px;
  }
---
```

## 色の基本原則

### 3色ルール

| 役割 | 比率 | 用途 |
|------|------|------|
| 背景色 | 70% | スライドの背景 |
| メインカラー | 25% | 見出し、強調ボックス |
| アクセントカラー | 5% | 特に強調したい箇所 |

### 文字色の推奨

```css
/* ❌ 真っ黒は避ける */
color: #000000;

/* ✅ 少し薄い黒を使う */
color: #333333;  /* 推奨 */
color: #444444;  /* やや明るめ */
```

## よく使うディレクティブ

### スライド単位の設定

```markdown
<!-- _class: lead -->
# 中央寄せのタイトルスライド

<!-- _backgroundColor: #1e3a5f -->
<!-- _color: white -->
# 背景色を変更したスライド

<!-- _paginate: false -->
# ページ番号を非表示
```

### 画像の配置

```markdown
<!-- 背景画像 -->
![bg](image.jpg)

<!-- 右側に配置 -->
![bg right](image.jpg)

<!-- 左側に40%幅で配置 -->
![bg left:40%](image.jpg)

<!-- 透明度を設定 -->
![bg opacity:0.5](image.jpg)
```

## フォントサイズの目安

| 要素 | 推奨サイズ | CSS例 |
|------|-----------|-------|
| メインタイトル | 48-64px | `font-size: 56px;` |
| セクション見出し | 36-48px | `font-size: 40px;` |
| サブ見出し | 28-36px | `font-size: 32px;` |
| 本文 | 24-28px | `font-size: 26px;` |
| 注釈 | 18-22px | `font-size: 20px;` |

## 参考リンク

- [Marp 公式ドキュメント](https://marp.app/)
- [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
- [Marpit Framework](https://marpit.marp.app/)
