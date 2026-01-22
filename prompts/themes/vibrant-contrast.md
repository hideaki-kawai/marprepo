# Vibrant Contrast テーマ

ビビッドな色のコントラストで、元気でインパクトのある印象を与えるテーマです。イベント、マーケティング、活気のあるプレゼンに最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | ピュアホワイト | `#FFFFFF` | スライド背景 |
| 文字色 | チャコール | `#1F2937` | 本文テキスト |
| メインカラー | ビビッドオレンジ | `#EA580C` | 見出し、メイン要素 |
| メインカラー（薄） | ライトオレンジ | `#FED7AA` | 背景ハイライト |
| アクセントカラー | ディープパープル | `#7C3AED` | 強調、コントラスト |
| サブカラー | ターコイズ | `#0D9488` | 補助的なアクセント |

## 推奨フォント

- **見出し**: Noto Sans JP Black / Poppins Bold
- **本文**: Noto Sans JP Medium / Poppins Regular

## プロンプト（コピー用）

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&family=Poppins:wght@400;500;600;700;800;900&display=swap');
  
  /* ============================================
     Vibrant Contrast テーマ
     元気でインパクトのある配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', 'Poppins', sans-serif;
    background-color: #FFFFFF;
    color: #1F2937;
    font-size: 26px;
    line-height: 1.6;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    color: #EA580C;
    font-size: 52px;
    font-weight: 900;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 30px;
    position: relative;
  }
  
  h1::after {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 0;
    width: 100px;
    height: 6px;
    background: linear-gradient(90deg, #EA580C 0%, #7C3AED 100%);
    border-radius: 3px;
  }
  
  h2 {
    color: #C2410C;
    font-size: 38px;
    font-weight: 700;
    margin-top: 20px;
  }
  
  h3 {
    color: #7C3AED;
    font-size: 28px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #7C3AED;
    font-weight: 700;
  }
  
  em {
    color: #0D9488;
    font-style: normal;
    font-weight: 600;
  }
  
  /* リンク */
  a {
    color: #EA580C;
    text-decoration: none;
    font-weight: 600;
    border-bottom: 2px solid #FED7AA;
    transition: border-color 0.3s;
  }
  
  /* リスト */
  ul, ol {
    margin-left: 20px;
  }
  
  li {
    margin-bottom: 12px;
  }
  
  li::marker {
    color: #EA580C;
    font-weight: bold;
  }
  
  /* コードブロック */
  code {
    background-color: #FED7AA;
    color: #9A3412;
    border-radius: 6px;
    padding: 3px 10px;
    font-weight: 500;
  }
  
  pre {
    background: linear-gradient(135deg, #1F2937 0%, #374151 100%);
    color: #F9FAFB;
    border-radius: 12px;
    padding: 24px;
    border-left: 6px solid #EA580C;
  }
  
  /* テーブル */
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 20px 0;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  th {
    background: linear-gradient(135deg, #EA580C 0%, #C2410C 100%);
    color: #FFFFFF;
    padding: 16px 20px;
    text-align: left;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  td {
    border-bottom: 2px solid #FED7AA;
    padding: 16px 20px;
  }
  
  tr:nth-child(even) {
    background-color: #FFF7ED;
  }
  
  /* 引用 */
  blockquote {
    border-left: 6px solid #7C3AED;
    background: linear-gradient(90deg, #F3E8FF 0%, #FFFFFF 100%);
    padding: 20px 28px;
    margin: 24px 0;
    border-radius: 0 12px 12px 0;
    font-size: 28px;
    font-weight: 500;
  }
  
  /* ページ番号 */
  section::after {
    color: #9CA3AF;
    font-size: 18px;
    font-weight: 600;
  }
  
  /* タイトルスライド用クラス */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #EA580C 0%, #DC2626 50%, #7C3AED 100%);
    color: #FFFFFF;
  }
  
  section.lead h1 {
    color: #FFFFFF;
    font-size: 64px;
    text-shadow: 4px 4px 8px rgba(0, 0, 0, 0.3);
  }
  
  section.lead h1::after {
    display: none;
  }
  
  section.lead h2 {
    color: #FED7AA;
    font-size: 32px;
    font-weight: 500;
  }
  
  /* インパクトボックス */
  .impact-box {
    background: linear-gradient(135deg, #EA580C 0%, #7C3AED 100%);
    color: #FFFFFF;
    padding: 30px;
    border-radius: 16px;
    text-align: center;
    font-size: 32px;
    font-weight: 700;
  }
  
  /* 大きな数字 */
  .big-stat {
    font-size: 80px;
    font-weight: 900;
    background: linear-gradient(135deg, #EA580C 0%, #7C3AED 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
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

# 🚀 LAUNCH EVENT

新サービス発表会 2026

---

# 驚きの成果

## ベータテスト結果

- ユーザー満足度 **98%**
- 作業効率 *3倍* アップ
- 導入コスト **50%** 削減

> "これは革命だ" - テストユーザーの声

---

# 導入事例

| 企業名 | 業種 | 効果 |
|--------|------|------|
| A社 | IT | 売上200%増 |
| B社 | 製造 | コスト40%減 |
| C社 | 小売 | 顧客満足度150%増 |
```

## バリエーション

### イエロー × ブルー（エネルギッシュ）

```css
/* カラーパレットの変更 */
h1 { color: #EAB308; }
strong { color: #2563EB; }
h3 { color: #2563EB; }
th { background: linear-gradient(135deg, #EAB308 0%, #CA8A04 100%); }
```

### ピンク × グリーン（ポップ）

```css
/* カラーパレットの変更 */
h1 { color: #EC4899; }
strong { color: #059669; }
h3 { color: #059669; }
th { background: linear-gradient(135deg, #EC4899 0%, #DB2777 100%); }
```
