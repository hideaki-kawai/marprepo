# Business Blue テーマ

信頼感・誠実さを表現する青系の配色テーマです。ビジネス提案、報告会、社内プレゼンなどに最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | ホワイト | `#FFFFFF` | スライド背景 |
| 文字色 | ダークグレー | `#333333` | 本文テキスト |
| メインカラー | ディープブルー | `#1E40AF` | 見出し、ボックス背景 |
| メインカラー（薄） | ライトブルー | `#DBEAFE` | 背景ハイライト |
| アクセントカラー | コーラルレッド | `#DC2626` | 強調、重要ポイント |
| サブアクセント | オレンジ | `#EA580C` | 補助的な強調 |

## 推奨フォント

- **見出し**: Noto Sans JP Bold / Inter Bold
- **本文**: Noto Sans JP Regular / Inter Regular

## プロンプト（コピー用）

以下をMarpスライドのフロントマターに貼り付けてください：

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&family=Inter:wght@400;500;600;700&display=swap');
  
  /* ============================================
     Business Blue テーマ
     信頼感・誠実さを表現する青系配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', 'Inter', sans-serif;
    background-color: #FFFFFF;
    color: #333333;
    font-size: 26px;
    line-height: 1.6;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #1E40AF;
    font-size: 48px;
    font-weight: 700;
    border-bottom: 4px solid #1E40AF;
    padding-bottom: 12px;
    margin-bottom: 30px;
  }
  
  h2 {
    color: #1E40AF;
    font-size: 36px;
    font-weight: 700;
    margin-top: 20px;
  }
  
  h3 {
    color: #2563EB;
    font-size: 28px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #DC2626;
    font-weight: 700;
  }
  
  em {
    color: #1E40AF;
    font-style: normal;
    font-weight: 600;
  }
  
  /* リンク */
  a {
    color: #2563EB;
    text-decoration: underline;
  }
  
  /* リスト */
  ul, ol {
    margin-left: 20px;
  }
  
  li {
    margin-bottom: 8px;
  }
  
  li::marker {
    color: #1E40AF;
  }
  
  /* コードブロック */
  code {
    background-color: #DBEAFE;
    color: #1E40AF;
    border-radius: 4px;
    padding: 2px 8px;
    font-family: 'Source Code Pro', monospace;
  }
  
  pre {
    background-color: #1E293B;
    color: #E2E8F0;
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
    background-color: #1E40AF;
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
    background-color: #F8FAFC;
  }
  
  /* 引用 */
  blockquote {
    border-left: 4px solid #1E40AF;
    background-color: #DBEAFE;
    padding: 16px 24px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
  }
  
  /* ページ番号 */
  section::after {
    color: #6B7280;
    font-size: 18px;
  }
  
  /* タイトルスライド用クラス */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #1E40AF 0%, #3B82F6 100%);
    color: #FFFFFF;
  }
  
  section.lead h1 {
    color: #FFFFFF;
    border-bottom: none;
    font-size: 56px;
  }
  
  section.lead h2 {
    color: #DBEAFE;
    font-size: 32px;
    font-weight: 400;
  }
  
  /* 強調ボックス用クラス */
  section.highlight {
    background-color: #DBEAFE;
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

# プロジェクト報告書

2026年1月 営業部

---

# 今期の成果

## 売上実績

- 前年比 **120%** の売上達成
- 新規顧客獲得数 *50社*
- 顧客満足度 **4.5/5.0**

> 💡 特に新規顧客開拓が好調でした

---

# 今後の計画

| 四半期 | 目標 | 施策 |
|--------|------|------|
| Q1 | 売上10%増 | 新商品投入 |
| Q2 | 顧客基盤拡大 | キャンペーン実施 |
```

## おすすめの組み合わせ

- **フォーマルな提案書**: このテーマのまま使用
- **カジュアルな報告**: アクセントカラーを `#F97316`（オレンジ）に変更
- **技術発表**: コードブロックを多用する場合に最適
