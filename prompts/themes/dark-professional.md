# Dark Professional テーマ

ダークな背景で大人っぽく高級感のある印象を与えるテーマです。学会発表、エグゼクティブ向けプレゼン、夜のイベントに最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | ダークネイビー | `#0F172A` | スライド背景 |
| 文字色 | ライトグレー | `#E2E8F0` | 本文テキスト |
| メインカラー | ゴールド | `#F59E0B` | 見出し、アクセント |
| メインカラー（薄） | ダークゴールド | `#78350F` | ボックス背景 |
| アクセントカラー | シアン | `#06B6D4` | 強調、リンク |
| サブカラー | シルバー | `#94A3B8` | 補助テキスト |

## 推奨フォント

- **見出し**: Noto Sans JP Bold / Montserrat Bold
- **本文**: Noto Sans JP Regular / Montserrat Regular

## プロンプト（コピー用）

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&family=Montserrat:wght@400;500;600;700;800&display=swap');
  
  /* ============================================
     Dark Professional テーマ
     大人っぽいダーク配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', 'Montserrat', sans-serif;
    background-color: #0F172A;
    color: #E2E8F0;
    font-size: 26px;
    line-height: 1.6;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #F59E0B;
    font-size: 48px;
    font-weight: 700;
    border-bottom: 3px solid #F59E0B;
    padding-bottom: 12px;
    margin-bottom: 30px;
    letter-spacing: 1px;
  }
  
  h2 {
    color: #FBBF24;
    font-size: 36px;
    font-weight: 700;
    margin-top: 20px;
  }
  
  h3 {
    color: #FCD34D;
    font-size: 28px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #06B6D4;
    font-weight: 700;
  }
  
  em {
    color: #F59E0B;
    font-style: normal;
    font-weight: 600;
  }
  
  /* リンク */
  a {
    color: #06B6D4;
    text-decoration: none;
    border-bottom: 1px solid #06B6D4;
  }
  
  a:hover {
    color: #22D3EE;
  }
  
  /* リスト */
  ul, ol {
    margin-left: 20px;
  }
  
  li {
    margin-bottom: 10px;
  }
  
  li::marker {
    color: #F59E0B;
  }
  
  /* コードブロック */
  code {
    background-color: #1E293B;
    color: #06B6D4;
    border: 1px solid #334155;
    border-radius: 4px;
    padding: 2px 8px;
  }
  
  pre {
    background-color: #020617;
    color: #E2E8F0;
    border: 1px solid #334155;
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
    background-color: #78350F;
    color: #FEF3C7;
    padding: 14px 16px;
    text-align: left;
    font-weight: 600;
    border-bottom: 2px solid #F59E0B;
  }
  
  td {
    border-bottom: 1px solid #334155;
    padding: 14px 16px;
  }
  
  tr:nth-child(even) {
    background-color: #1E293B;
  }
  
  /* 引用 */
  blockquote {
    border-left: 4px solid #F59E0B;
    background-color: #1E293B;
    padding: 16px 24px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
    color: #CBD5E1;
  }
  
  /* ページ番号 */
  section::after {
    color: #64748B;
    font-size: 18px;
  }
  
  /* タイトルスライド用クラス */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #0F172A 0%, #1E293B 50%, #0F172A 100%);
    color: #E2E8F0;
  }
  
  section.lead h1 {
    color: #F59E0B;
    border-bottom: none;
    font-size: 56px;
    text-shadow: 0 0 30px rgba(245, 158, 11, 0.3);
  }
  
  section.lead h2 {
    color: #94A3B8;
    font-size: 28px;
    font-weight: 400;
  }
  
  /* グロー効果のあるボックス */
  .glow-box {
    background-color: #1E293B;
    border: 1px solid #F59E0B;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 0 20px rgba(245, 158, 11, 0.2);
  }
  
  /* 数字の強調 */
  .big-number {
    font-size: 72px;
    font-weight: 800;
    color: #F59E0B;
    line-height: 1;
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

# ANNUAL REPORT 2025

経営戦略発表会

---

# 業績ハイライト

## 主要指標

- 売上高 **¥150億円**（前年比+25%）
- 営業利益率 *15.2%*
- 新規事業売上比率 **30%**

> "最高の年を更新し続ける" - CEO メッセージ

---

# 事業別売上構成

| 事業部門 | 売上高 | 前年比 | 構成比 |
|----------|--------|--------|--------|
| デジタル | ¥60億 | +40% | 40% |
| コンサル | ¥45億 | +20% | 30% |
| 製造 | ¥45億 | +10% | 30% |
```

## バリエーション

### ブルー系（テック系向け）

```css
/* メインカラーをブルーに変更 */
h1 { color: #3B82F6; border-bottom-color: #3B82F6; }
h2 { color: #60A5FA; }
th { background-color: #1E40AF; }
```

### グリーン系（サステナビリティ向け）

```css
/* メインカラーをグリーンに変更 */
h1 { color: #10B981; border-bottom-color: #10B981; }
h2 { color: #34D399; }
th { background-color: #065F46; }
```
