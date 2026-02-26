# ヨガサイエンス (Yoga Science)

科学的根拠に基づくヨガの理論解説サイト。解剖学・生理学・神経科学の視点から「なぜ効くのか」を体系的に届ける。

## サイト構成

| カテゴリ | パス | 内容 |
|---|---|---|
| 解剖学 | `/anatomy/` | 筋骨格系の構造と機能 |
| 生理学 | `/physiology/` | 自律神経系・内分泌系・呼吸器系 |
| 心理学・神経科学 | `/psychology/` | 脳・精神への影響 |
| アーサナ理論 | `/asana/` | ポーズの力学・生理学分析 |
| 効果・エビデンス | `/evidence/` | 論文ベースの効果レビュー |
| ヨガ指導の科学 | `/teaching/` | 指導法・安全管理 |
| ヨガ哲学 | `/philosophy/` | 原典に基づく思想解説 |

## 技術スタック

- **静的サイトジェネレーター**: [Hugo](https://gohugo.io/) (extended)
- **テーマ**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **ホスティング**: GitHub Pages (`gh-pages` ブランチ)
- **CI/CD**: GitHub Actions（`main` ブランチへの push で自動デプロイ）
- **構造化データ**: JSON-LD (Schema.org Article)

## 記事の追加方法

```bash
# Hugo CLI で新しい記事を作成（archetype テンプレートが適用される）
hugo new anatomy/hamstrings-and-forward-fold.md

# エディタで編集し、draft: false に変更

# ビルド確認
hugo server -D

# main ブランチに push → 自動デプロイ
git add .
git commit -m "Add new article: hamstrings-and-forward-fold"
git push origin main
```

## ローカルでの開発

```bash
# Hugo をインストール（macOS の場合）
brew install hugo

# サブモジュール（PaperMod テーマ）を取得
git submodule update --init --recursive

# 開発サーバーを起動
hugo server -D

# http://localhost:1313/Yoga_science/ でプレビュー
```
