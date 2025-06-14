# JXC 公開記事アーカイブ

Japan X College（JXC）が **note** に公開している記事を自動でミラーリングしたリポジトリです。  
`note-japan_x_college-*.xml` をもとに、**公開（publish）済み** の記事だけを Markdown に変換して格納しています。

---

## ディレクトリ構成

articles/
└── data/
├── markdown/ # 記事本文（Markdown）
│ └── YYYY/MM/DD/ # 投稿日でフォルダ分け
│ └── タイトル.md
└── metadata/
├── index.csv # 記事メタ一覧（自動生成）
└── authors.yaml # 著者情報（任意）

- **ファイル名**: タイトルをそのまま slug 化。重複時は `-2` などを付与  
- **front-matter**: 各 Markdown 冒頭に `title / slug / date / link` を記録  
- **画像** を追加したい場合は `data/images/slug/` フォルダを作って配置してください（`.gitattributes` で LFS 対応）