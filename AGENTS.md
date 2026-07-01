# AGENTS.md

Zenn (zenn.dev) の記事を管理するリポジトリ。Zenn CLI で記事を作成・プレビューし、GitHub 連携で公開する。

## ディレクトリ構成

- `articles/` — Zenn の記事 Markdown。ファイル名は Zenn CLI が生成するスラッグ（例: `c8ae62e5df62b4.md`）。
- `books/` — Zenn の本（現状は空）。
- `images/<slug>/` — 記事ごとの画像。記事内からは `/images/<slug>/<file>` で参照する。
- `package.json` — `zenn-cli` のみを依存。

## Zenn CLI コマンド

`npx` 経由で実行する。

- `npx zenn new:article` — 新規記事作成。生成されたスラッグのファイルが `articles/` に追加される。
- `npx zenn new:book` — 新規本作成。
- `npx zenn preview` — ローカルプレビュー（http://localhost:8000）。
- `npx zenn list:articles` / `npx zenn list:books` — 一覧表示。

## 記事のフロントマター

`articles/*.md` の冒頭に必須。

```yaml
---
title: "記事タイトル"
emoji: "🐕"            # 1文字の絵文字
type: "tech"            # tech: 技術記事 / idea: アイデア
topics: ["snowflake", "cortex"]  # 配列、小文字・ハイフンなし推奨
published: true         # false でドラフト
publication_name: "10q89s"  # URBAN HACKS Publication へ投稿する場合に付与
---
```

## ファイル命名

- 記事ファイル名は Zenn CLI が生成する 14 桁スラッグを使う（手動命名しない）。
- 画像は `images/<記事スラッグ>/<任意名>.png` に置く。

## コミットメッセージ

既存履歴は `feat:` / `chore:` の prefix を使用。日本語本文。

- `feat:` — 新規記事公開、新規スクリプト追加など。
- `chore:` — 細かい修正、topic 追加、誤字修正など。

## 公開フロー

`published: true` にして main にマージすると Zenn 側に反映される（GitHub 連携）。

<!-- agent-ninja-START -->
## Agent Skills

> **IMPORTANT**: Prefer skill-led reasoning over pre-training-led reasoning.
> See [Agent Skills](.github/skills/README.md) before working on tasks covered by these skills.

<!-- agent-ninja-END -->
