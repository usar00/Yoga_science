# ヨガサイエンス (Yoga Science)

科学的根拠に基づくヨガの理論解説サイト。理系的アプローチで「なぜ効くのか」を体系的に届ける。

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

- **静的サイトジェネレーター**: [Hugo](https://gohugo.io/)
- **ホスティング**: GitHub Pages
- **CI/CD**: GitHub Actions（`main` ブランチへの push で自動デプロイ）

## 記事の追加方法

新しい記事を追加するには、対応するカテゴリのディレクトリに Markdown ファイルを作成します。

```bash
# 例: 解剖学カテゴリに新しい記事を追加
# content/anatomy/new-article-slug.md を作成

cat <<'EOF' > content/anatomy/new-article-slug.md
---
title: "記事タイトル"
date: 2026-02-26
description: "記事の概要説明"
tags: ["タグ1", "タグ2"]
---

記事の本文をここに書く。
EOF
```

`main` ブランチに push すると、GitHub Actions が自動的にビルド・デプロイします。

## ローカルでの開発

```bash
# Hugo をインストール（macOS の場合）
brew install hugo

# 開発サーバーを起動
hugo server -D

# http://localhost:1313/ でプレビュー
```
