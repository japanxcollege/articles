# JXC Articles Archive

Japan X College（JXC）のnote記事をGitHubで管理するリポジトリです。

## 概要

このリポジトリは、JXCがnoteに公開している記事を自動でミラーリングしたものです。
`note-japan_x_college-*.xml`をもとに、**公開（publish）済み**の記事だけをMarkdownに変換して格納しています。

## ディレクトリ構成

```
articles/
├── README.md          # このファイル
└── data/             # 記事データ
    ├── markdown/     # 記事本文（Markdown）
    │   └── YYYY/MM/DD/  # 投稿日でフォルダ分け
    │   └── タイトル.md
    └── metadata/     # メタデータ
        ├── index.csv    # 記事メタ一覧（自動生成）
        └── authors.yaml # 著者情報（任意）
```

## ファイル命名規則

- **ファイル名**: タイトルをそのままslug化。重複時は `-2` などを付与
- **front-matter**: 各Markdown冒頭に `title / slug / date / link` を記録
- **画像**: `data/images/slug/` フォルダに配置（`.gitattributes` でLFS対応）

## 更新方法

1. noteのXMLエクスポートファイルを取得
2. 変換スクリプトを実行してMarkdownに変換
3. 変更をコミットしてプッシュ

## ライセンス

© Japan X College 