# Monochrome テーマ

シンプルなモノクロ配色で、どんな場面でも使える万能テーマです。印刷用、フォーマルな場面、シンプルさを求める場面に最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | ホワイト | `#FFFFFF` | スライド背景 |
| 文字色 | ダークグレー | `#374151` | 本文テキスト |
| メインカラー | ブラック | `#111827` | 見出し |
| メインカラー（薄） | ライトグレー | `#F3F4F6` | 背景ハイライト |
| アクセントカラー | ミディアムグレー | `#6B7280` | 補助要素 |
| 境界線 | グレー | `#D1D5DB` | 区切り線、ボーダー |

## 推奨フォント

- **見出し**: Noto Sans JP Bold / Inter Bold
- **本文**: Noto Sans JP Regular / Inter Regular

## プロンプト（コピー用）

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&family=Inter:wght@400;500;600;700&display=swap');
  
  /* ============================================
     Monochrome テーマ
     シンプルなモノクロ配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', 'Inter', sans-serif;
    background-color: #FFFFFF;
    color: #374151;
    font-size: 26px;
    line-height: 1.7;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #111827;
    font-size: 46px;
    font-weight: 700;
    border-bottom: 2px solid #111827;
    padding-bottom: 12px;
    margin-bottom: 28px;
  }
  
  h2 {
    color: #1F2937;
    font-size: 34px;
    font-weight: 700;
    margin-top: 20px;
  }
  
  h3 {
    color: #374151;
    font-size: 26px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #111827;
    font-weight: 700;
  }
  
  em {
    font-style: italic;
  }
  
  /* リンク */
  a {
    color: #374151;
    text-decoration: underline;
  }
  
  /* リスト */
  ul, ol {
    margin-left: 20px;
  }
  
  li {
    margin-bottom: 10px;
  }
  
  li::marker {
    color: #374151;
  }
  
  /* コードブロック */
  code {
    background-color: #F3F4F6;
    color: #1F2937;
    border: 1px solid #E5E7EB;
    border-radius: 4px;
    padding: 2px 8px;
    font-family: 'SF Mono', 'Monaco', monospace;
  }
  
  pre {
    background-color: #1F2937;
    color: #F9FAFB;
    border-radius: 8px;
    padding: 20px;
  }
  
  /* テーブル */
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 20px 0;
  }
  
  th {
    background-color: #111827;
    color: #FFFFFF;
    padding: 12px 16px;
    text-align: left;
    font-weight: 600;
  }
  
  td {
    border-bottom: 1px solid #E5E7EB;
    padding: 12px 16px;
  }
  
  tr:nth-child(even) {
    background-color: #F9FAFB;
  }
  
  /* 引用 */
  blockquote {
    border-left: 4px solid #6B7280;
    background-color: #F3F4F6;
    padding: 16px 24px;
    margin: 20px 0;
    font-style: italic;
    color: #4B5563;
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
    background-color: #111827;
    color: #F9FAFB;
  }
  
  section.lead h1 {
    color: #FFFFFF;
    border-bottom: none;
    font-size: 52px;
  }
  
  section.lead h2 {
    color: #9CA3AF;
    font-size: 28px;
    font-weight: 400;
  }
  
  /* 白背景のタイトルスライド */
  section.lead-white {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background-color: #FFFFFF;
  }
  
  section.lead-white h1 {
    border-bottom: none;
    font-size: 52px;
  }
  
  /* 区切り線 */
  hr {
    border: none;
    border-top: 1px solid #D1D5DB;
    margin: 30px 0;
  }
  
  /* 印刷最適化 */
  @media print {
    section {
      background-color: #FFFFFF !important;
      color: #000000 !important;
    }
    
    h1, h2, h3 {
      color: #000000 !important;
    }
    
    a {
      color: #000000 !important;
      text-decoration: underline !important;
    }
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

# 年次報告書

2025年度 事業報告

---

# 目次

1. 事業概要
2. 財務報告
3. 今後の展望

---

# 事業概要

## 主な取り組み

- 新規事業の立ち上げ
- 既存事業の効率化
- 人材育成プログラムの拡充

> 「継続は力なり」を信条に、着実な成長を遂げました

---

# 財務報告

| 項目 | 2024年度 | 2025年度 | 増減 |
|------|----------|----------|------|
| 売上高 | 100億円 | 120億円 | +20% |
| 営業利益 | 10億円 | 15億円 | +50% |
| 純利益 | 7億円 | 11億円 | +57% |
```

## 印刷時の注意点

このテーマは印刷に最適化されています：

1. **背景色**: 白を基調としているため、インク消費を抑えられます
2. **コントラスト**: 黒とグレーのコントラストで読みやすさを確保
3. **@media print**: 印刷時に最適な色に自動調整されます

### モノクロ印刷向けの追加設定

```css
/* 完全なモノクロ印刷用 */
@media print {
  th {
    background-color: #000000 !important;
    color: #FFFFFF !important;
  }
  
  code {
    border: 1px solid #000000 !important;
    background-color: #FFFFFF !important;
  }
  
  blockquote {
    border-left: 4px solid #000000 !important;
    background-color: #FFFFFF !important;
  }
}
```

## バリエーション

### ウォームグレー系

```css
/* よりあたたかみのあるグレー */
section { color: #44403C; }
h1, h2 { color: #1C1917; }
th { background-color: #292524; }
```

### クールグレー系

```css
/* よりクールな印象 */
section { color: #334155; }
h1, h2 { color: #0F172A; }
th { background-color: #1E293B; }
```
