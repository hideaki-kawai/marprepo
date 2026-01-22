# Calm Earth テーマ

落ち着いたアースカラーで、真面目で誠実な印象を与えるテーマです。学術発表、研究報告、フォーマルな場面に最適。

## カラーパレット

| 役割 | 色名 | カラーコード | 用途 |
|------|------|-------------|------|
| 背景色 | オフホワイト | `#FAFAF9` | スライド背景 |
| 文字色 | ダークブラウン | `#44403C` | 本文テキスト |
| メインカラー | フォレストグリーン | `#365314` | 見出し、ボックス背景 |
| メインカラー（薄） | ライトグリーン | `#ECFCCB` | 背景ハイライト |
| アクセントカラー | テラコッタ | `#B45309` | 強調、重要ポイント |
| サブカラー | ウォームグレー | `#78716C` | 補助テキスト |

## 推奨フォント

- **見出し**: Noto Serif JP Bold / Merriweather Bold
- **本文**: Noto Sans JP Regular / Source Sans Pro Regular

## プロンプト（コピー用）

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* Google Fonts インポート */
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&family=Noto+Serif+JP:wght@400;600;700&family=Merriweather:wght@400;700&display=swap');
  
  /* ============================================
     Calm Earth テーマ
     落ち着いたアースカラー配色
     ============================================ */
  
  /* 基本設定 */
  section {
    font-family: 'Noto Sans JP', sans-serif;
    background-color: #FAFAF9;
    color: #44403C;
    font-size: 26px;
    line-height: 1.7;
    padding: 50px 60px;
  }
  
  /* 見出しスタイル */
  h1 {
    font-family: 'Noto Serif JP', 'Merriweather', serif;
    color: #365314;
    font-size: 44px;
    font-weight: 700;
    border-bottom: 3px solid #365314;
    padding-bottom: 10px;
    margin-bottom: 28px;
  }
  
  h2 {
    font-family: 'Noto Serif JP', 'Merriweather', serif;
    color: #365314;
    font-size: 34px;
    font-weight: 600;
    margin-top: 20px;
  }
  
  h3 {
    color: #4D7C0F;
    font-size: 26px;
    font-weight: 600;
  }
  
  /* 強調テキスト */
  strong {
    color: #B45309;
    font-weight: 700;
  }
  
  em {
    color: #365314;
    font-style: normal;
    font-weight: 600;
  }
  
  /* リンク */
  a {
    color: #4D7C0F;
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
    color: #365314;
  }
  
  /* コードブロック */
  code {
    background-color: #ECFCCB;
    color: #365314;
    border-radius: 4px;
    padding: 2px 8px;
  }
  
  pre {
    background-color: #292524;
    color: #E7E5E4;
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
    background-color: #365314;
    color: #FFFFFF;
    padding: 12px 16px;
    text-align: left;
    font-weight: 600;
  }
  
  td {
    border-bottom: 1px solid #D6D3D1;
    padding: 12px 16px;
  }
  
  tr:nth-child(even) {
    background-color: #F5F5F4;
  }
  
  /* 引用 */
  blockquote {
    border-left: 4px solid #365314;
    background-color: #ECFCCB;
    padding: 16px 24px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
    font-style: italic;
  }
  
  /* ページ番号 */
  section::after {
    color: #78716C;
    font-size: 18px;
  }
  
  /* タイトルスライド用クラス */
  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(135deg, #365314 0%, #4D7C0F 100%);
    color: #FFFFFF;
  }
  
  section.lead h1 {
    color: #FFFFFF;
    border-bottom: none;
    font-size: 52px;
  }
  
  section.lead h2 {
    color: #ECFCCB;
    font-size: 28px;
    font-weight: 400;
  }
  
  /* 注釈スタイル */
  .footnote {
    color: #78716C;
    font-size: 18px;
    margin-top: 30px;
    padding-top: 10px;
    border-top: 1px solid #D6D3D1;
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

# 環境影響評価報告

令和8年度 研究発表会

---

# 研究背景

## 問題意識

- 地球温暖化による生態系への影響
- 持続可能な開発目標（SDGs）との関連
- **CO2排出量削減** の必要性

> 本研究では、森林保全活動の効果を定量的に分析しました

---

# 調査結果

| 項目 | 2024年 | 2025年 | 変化率 |
|------|--------|--------|--------|
| 森林面積 | 1,200ha | 1,350ha | +12.5% |
| 生物多様性指数 | 3.2 | 3.8 | +18.8% |
| CO2吸収量 | 450t | 520t | +15.6% |
```

## 配色のバリエーション

### より暖かみのある印象にしたい場合

```css
/* メインカラーをブラウン系に変更 */
h1, h2 { color: #78350F; }
th { background-color: #78350F; }
```

### よりクールな印象にしたい場合

```css
/* メインカラーをティール系に変更 */
h1, h2 { color: #134E4A; }
th { background-color: #134E4A; }
```
