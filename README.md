# Slides

Marpを使用してMarkdownからスライドをcreateするリポジトリ

## 📝 使い方

### 1. セットアップ

#### VSCode拡張機能（推奨）
1. VSCodeで「Marp for VS Code」拡張機能をインストール
2. `.md`ファイルでMarpプレビューがすぐに使える
3. npmインストール不要！

#### CLI版
```bash
# mise 利用者
mise use -g marp-cli
```

### 2. スライドのcreate
```bash
# HTMLでexport
marp slides.md

# PDFでexport
# --allow-local-files 付与で画像動画表示
marp --allow-local-files --html ./personal/ttsubasa/20250731_vibe_coding/slide.md
```

### 3. リアルタイムpreview

#### VSCode拡張機能
- `Ctrl/Cmd + Shift + P` → "Marp: Open Preview"
- またはファイル上で右クリック → "Open Preview"

## 📁 ディレクトリ構成

```
slide-deck/
├── 20250731_vibe_coding/    # Vibe Codingプレゼン資料
│   ├── slide.md            # Markdownファイル
│   ├── slide.html          # 出力されたHTML
│   └── images/             # 画像・動画素材
├── CLAUDE.md               # Claudeプロジェクト仕様書
├── README.md               # このファイル
└── YYYYMMDD_内容/          # 今後作成される資料（例）
```

### 命名規則
- **ディレクトリ名**: `YYYYMMDD_内容` 形式（例: 20250731_vibe_coding）
- **スライドファイル**: `slide.md`（各ディレクトリ内）
- **画像ディレクトリ**: `images/`（必要に応じて）

## ✍️ Markdownの基本構文

```markdown
---
marp: true
theme: default
paginate: true
header: 'ヘッダーtext'
footer: 'フッターtext'
---

# タイトルslide

---

# slide 1

- bullet point 1
- bullet point 2

---

# slide 2

## サブタイトル

内容...
```

## 🎨 themeとstyle

- `theme: default` - 基本theme
- カスタムCSSでstyleを調整可能
- Notion風デザインなどを実装済み


## 🔗 参考link

- [Marp公式ドキュメント](https://marp.app/)
- [Marp for VS Code拡張機能](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
- [Marp CLI](https://github.com/marp-team/marp-cli)
