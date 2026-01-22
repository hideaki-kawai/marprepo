# Cute Pastel テーマ

やわらかいパステルカラーで、親しみやすく温かみのある印象を与えるテーマです。女性向け、子供向け、カジュアルなプレゼンに最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | クリームホワイト | `#FFFBF5` | スライド背景 |
| 文字色 | ソフトブラウン | `#5D534A` | 本文テキスト |
| メインカラー | ローズピンク | `#DB2777` | 見出し、ボックス背景 |
| メインカラー（薄） | ライトピンク | `#FCE7F3` | 背景ハイライト |
| アクセントカラー | ミントグリーン | `#10B981` | 強調、ポイント |
| サブカラー | ラベンダー | `#A78BFA` | 補助的な装飾 |

## 推奨フォント

- **見出し**: Noto Sans JP Bold / Quicksand Bold
- **本文**: Noto Sans JP Regular / Quicksand Regular

## プロンプト（コピー用）

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=Quicksand:wght@400;500;600;700&display=swap');
  
  /* ============================================
     Cute Pastel テーマ
     やわらかいパステルカラー配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', 'Quicksand', sans-serif;
    background-color: #FFFBF5;
    color: #5D534A;
    font-size: 26px;
    line-height: 1.7;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #DB2777;
    font-size: 44px;
    font-weight: 700;
    border-bottom: 3px dashed #F9A8D4;
    padding-bottom: 12px;
    margin-bottom: 28px;
  }
  
  h2 {
    color: #DB2777;
    font-size: 34px;
    font-weight: 700;
    margin-top: 20px;
  }
  
  h3 {
    color: #EC4899;
    font-size: 26px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #10B981;
    font-weight: 700;
  }
  
  em {
    color: #A78BFA;
    font-style: normal;
    font-weight: 600;
  }
  
  /* リンク */
  a {
    color: #DB2777;
    text-decoration: none;
    border-bottom: 2px dotted #F9A8D4;
  }
  
  /* リスト */
  ul, ol {
    margin-left: 20px;
  }
  
  li {
    margin-bottom: 10px;
  }
  
  li::marker {
    color: #DB2777;
  }
  
  /* コードブロック */
  code {
    background-color: #FCE7F3;
    color: #BE185D;
    border-radius: 6px;
    padding: 2px 8px;
  }
  
  pre {
    background-color: #FDF4FF;
    color: #86198F;
    border: 2px solid #F5D0FE;
    border-radius: 12px;
    padding: 20px;
  }
  
  /* テーブル */
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 20px 0;
    border-radius: 12px;
    overflow: hidden;
  }
  
  th {
    background-color: #DB2777;
    color: #FFFFFF;
    padding: 14px 16px;
    text-align: left;
    font-weight: 600;
  }
  
  td {
    border-bottom: 1px solid #FBCFE8;
    padding: 14px 16px;
  }
  
  tr:nth-child(even) {
    background-color: #FDF2F8;
  }
  
  /* 引用 */
  blockquote {
    border-left: 4px solid #10B981;
    background-color: #ECFDF5;
    padding: 16px 24px;
    margin: 20px 0;
    border-radius: 0 12px 12px 0;
  }
  
  /* ページ番号 */
  section::after {
    color: #9CA3AF;
    font-size: 18px;
  }
  
  /* タイトルスライド用クラス */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #FCE7F3 0%, #FDF4FF 50%, #EDE9FE 100%);
    color: #5D534A;
  }
  
  section.lead h1 {
    color: #DB2777;
    border-bottom: none;
    font-size: 52px;
    text-shadow: 2px 2px 4px rgba(219, 39, 119, 0.1);
  }
  
  section.lead h2 {
    color: #A78BFA;
    font-size: 28px;
    font-weight: 500;
  }
  
  /* かわいいボックス */
  .cute-box {
    background: linear-gradient(135deg, #FCE7F3 0%, #FDF4FF 100%);
    border: 2px solid #F9A8D4;
    border-radius: 16px;
    padding: 20px;
    margin: 20px 0;
  }
  
  /* ハイライトテキスト */
  mark {
    background-color: #FEF3C7;
    padding: 2px 6px;
    border-radius: 4px;
  }
---
```

## 使用例

```markdown
---
marp: true
<!-- 上記のstyleをここに貼り付け -->
---

<!-- _class: lead -->

# 🌸 新商品のご紹介

〜春の新作コレクション〜

---

# 商品ラインナップ

## 今シーズンのテーマ

- **ナチュラル＆オーガニック**
- *やさしい色合い*
- 肌にやさしい素材

> 💕 すべての商品が敏感肌の方にもおすすめです

---

# お客様の声

| 年代 | 満足度 | コメント |
|------|--------|----------|
| 20代 | ⭐⭐⭐⭐⭐ | とってもかわいい！ |
| 30代 | ⭐⭐⭐⭐ | 使いやすいです |
| 40代 | ⭐⭐⭐⭐⭐ | 品質が良い |
```

## バリエーション

### ラベンダー系にしたい場合

```css
/* メインカラーをラベンダーに変更 */
h1, h2 { color: #7C3AED; }
th { background-color: #7C3AED; }
section { background-color: #FAF5FF; }
```

### ミント系にしたい場合

```css
/* メインカラーをミントグリーンに変更 */
h1, h2 { color: #059669; }
th { background-color: #059669; }
section { background-color: #F0FDF4; }
```
