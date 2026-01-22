# Marp スライド プロンプト集

Marpでスライドを作成する際に使えるプロンプト（スタイル指定）のコレクションです。

## 📁 ディレクトリ構成

```
marprepo/
├── README.md                    # このファイル
├── prompts/                     # プロンプト集
│   ├── themes/                  # テーマ別プロンプト
│   │   ├── business-blue.md     # ビジネス向け青系
│   │   ├── calm-earth.md        # 落ち着いたアースカラー
│   │   ├── cute-pastel.md       # かわいらしいパステル
│   │   ├── dark-professional.md # 大人っぽいダーク
│   │   ├── vibrant-contrast.md  # インパクトのあるコントラスト
│   │   └── monochrome.md        # モノクロ（印刷向け）
│   └── base/                    # 基本設定プロンプト
│       └── marp-basics.md       # Marp基本設定ガイド
├── examples/                    # サンプルスライド
└── assets/                      # 画像などのリソース
```

## 🎨 配色の基本原則

このリポジトリのプロンプトは以下の原則に基づいて設計されています：

### 使用する色は3色が目安

| 色の役割 | 用途 | 比率 |
|---------|------|------|
| 背景色 | スライドの背景 | 約70% |
| メインカラー | 見出し、強調ボックスなど | 約25% |
| アクセントカラー | 特に強調したい箇所 | 約5% |

### 文字色について

- **テキストの色**: 真っ黒（#000000）ではなく、少し薄い黒（#333333〜#444444）を推奨
- 黒すぎるとデザイン性が下がり、目が疲れやすくなります

## 🚀 クイックスタート：スライド作成の流れ

### Step 1: テーマを選ぶ

まず、プレゼンのシーンや与えたい印象からテーマを選びましょう。

#### 📋 シーン別おすすめテーマ

| こんなとき | おすすめテーマ |
|-----------|---------------|
| 社内会議・報告会 | [Business Blue](prompts/themes/business-blue.md) / [Monochrome](prompts/themes/monochrome.md) |
| 学会発表・研究報告 | [Calm Earth](prompts/themes/calm-earth.md) / [Dark Professional](prompts/themes/dark-professional.md) |
| 顧客への提案 | [Business Blue](prompts/themes/business-blue.md) / [Dark Professional](prompts/themes/dark-professional.md) |
| イベント・発表会 | [Vibrant Contrast](prompts/themes/vibrant-contrast.md) |
| 女性向け・子供向け | [Cute Pastel](prompts/themes/cute-pastel.md) |
| 印刷して配布 | [Monochrome](prompts/themes/monochrome.md) |

#### 🎭 印象別おすすめテーマ

| 与えたい印象 | おすすめテーマ |
|-------------|---------------|
| 信頼感・誠実さ | [Business Blue](prompts/themes/business-blue.md) |
| 落ち着き・真面目 | [Calm Earth](prompts/themes/calm-earth.md) |
| 親しみやすさ・やわらかさ | [Cute Pastel](prompts/themes/cute-pastel.md) |
| 高級感・プロフェッショナル | [Dark Professional](prompts/themes/dark-professional.md) |
| 元気・インパクト | [Vibrant Contrast](prompts/themes/vibrant-contrast.md) |
| シンプル・万能 | [Monochrome](prompts/themes/monochrome.md) |

> 💡 **迷ったら**: ビジネスシーンなら **Business Blue**、学術系なら **Calm Earth** がおすすめです。

### Step 2: Markdownファイルを作成

```markdown
---
marp: true
theme: default
paginate: true
style: |
  /* ここにテーマのスタイルを貼り付け */
---

# プレゼンタイトル

サブタイトル・日付など

---

# セクション1

- ポイント1
- ポイント2
- ポイント3

---

# セクション2

内容を記述...
```

### Step 3: テーマのスタイルを貼り付け

1. 選んだテーマファイル（例: `prompts/themes/business-blue.md`）を開く
2. 「プロンプト（コピー用）」セクションの `style: |` 以下をコピー
3. 作成したMarkdownファイルに貼り付け

### Step 4: プレビュー & 出力

```bash
# プレビュー
marp -p your-slide.md

# PPTX出力（編集可能）
npx @marp-team/marp-cli your-slide.md --pptx --pptx-editable

# PDF出力
marp your-slide.md --pdf
```

---

## 📝 基本的な使い方（まとめ）

1. `prompts/themes/` から好みのテーマを選択
2. プロンプト内容をコピー
3. Marpスライドの先頭（フロントマター）に貼り付け
4. 必要に応じてカスタマイズ

### 例：最小構成

```markdown
---
marp: true
theme: default
style: |
  /* ここにプロンプトからコピーしたスタイルを貼り付け */
---

# スライドタイトル

内容をここに記述
```

## 🔧 Marp CLI のインストールと使い方

Marp CLIを使うと、コマンドラインからMarkdownファイルをPDF/HTML/PPTXなどに変換できます。

### インストール方法

Marp CLIは**Node.js環境**で動作します。

```bash
# グローバルインストール（推奨）
npm install -g @marp-team/marp-cli

# プロジェクトローカルにインストールする場合
npm install --save-dev @marp-team/marp-cli
```

### PPTX（PowerPoint）への変換

```bash
# 基本的な変換
marp presentation.md --pptx

# 出力ファイル名を指定
marp presentation.md -o output.pptx

# 出力ディレクトリを指定
marp presentation.md --pptx -o ./output/

# ⭐ 編集可能なPPTXを生成（おすすめ）
npx @marp-team/marp-cli presentation.md --pptx --pptx-editable
```

> 💡 **`--pptx-editable` オプション**: 通常のPPTX出力はスライドが画像として埋め込まれますが、このオプションを付けると**PowerPoint上でテキストや図形を編集可能な状態**で出力されます。後から微調整したい場合に便利です。

### その他の出力形式

```bash
# PDF出力
marp presentation.md --pdf

# HTML出力
marp presentation.md --html

# 複数形式を同時出力
marp presentation.md --pdf --html --pptx
```

### プレビューモード

```bash
# ブラウザでプレビュー（ファイル変更時に自動リロード）
marp -p presentation.md

# サーバーモード（複数ファイルを監視）
marp -s ./slides/
```

### よく使うオプション

| オプション | 説明 |
|-----------|------|
| `--pptx` | PowerPoint形式で出力 |
| `--pptx-editable` | 編集可能なPPTXを出力（⭐おすすめ） |
| `--pdf` | PDF形式で出力 |
| `--html` | HTML形式で出力 |
| `-o <path>` | 出力先を指定 |
| `-p` / `--preview` | プレビューモード |
| `-s` / `--server` | サーバーモード |
| `--allow-local-files` | ローカル画像ファイルを許可 |
| `--theme <name>` | テーマを指定 |

### VS Code拡張を使う方法（CLI不要）

CLIをインストールせずに、VS Codeの拡張機能でも変換できます：

1. VS Code拡張「[Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)」をインストール
2. Markdownファイルを開く
3. 右上のMarpアイコン（Mのロゴ）をクリック
4. 「Export slide deck...」を選択
5. 保存形式で `.pptx` / `.pdf` / `.html` を選択

> 💡 初心者にはVS Code拡張がおすすめです。CLIは自動化やCI/CDでの利用に向いています。

---

## 📚 テーマ一覧

| テーマ | 説明 | おすすめシーン |
|-------|------|---------------|
| [Business Blue](prompts/themes/business-blue.md) | 信頼感のある青系配色 | ビジネス提案、報告会 |
| [Calm Earth](prompts/themes/calm-earth.md) | 落ち着いたアースカラー | 学術発表、真面目な報告 |
| [Cute Pastel](prompts/themes/cute-pastel.md) | やわらかいパステル調 | 女性向け、子供向け |
| [Dark Professional](prompts/themes/dark-professional.md) | 大人っぽいダーク | 学会発表、高級感のある提案 |
| [Vibrant Contrast](prompts/themes/vibrant-contrast.md) | インパクトのあるコントラスト | イベント、活気のあるプレゼン |
| [Monochrome](prompts/themes/monochrome.md) | シンプルなモノクロ | 印刷用、フォーマルな場面 |

## 🔤 フォントについて

各テーマでは以下のフォントを推奨しています：

### 日本語フォント
- **見出し**: Noto Sans JP (Bold/Black)
- **本文**: Noto Sans JP (Regular/Medium)

### 英数字フォント
- **見出し**: Inter, Roboto, Source Sans Pro
- **本文**: Inter, Roboto

> 💡 Google Fontsからインポートする設定を各プロンプトに含めています

## 📖 参考資料

### Marp関連
- [Marp 公式ドキュメント](https://marp.app/)
- [Marp CLI (GitHub)](https://github.com/marp-team/marp-cli)
- [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
- [Markdown でスライドを作れる Marp はいいぞ - Qiita](https://qiita.com/tomoasleep/items/604107787d92dec4868e)

### 配色・デザイン
- [パワポ資料の配色はこれで決まり！](https://studio.virtual-planner.com/powerpoint-color/)
- [パワポで使う色はパクれ！](https://toukeidesign.sozaiya-san.com/pp_design_basic04_color-copypaste)

## ライセンス

MIT License
