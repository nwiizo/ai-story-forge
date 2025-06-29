# ワークスペースガイド - 作品の管理方法

## 推奨ディレクトリ構造

AI Story Forgeを使って作成した作品は、以下のような構造で管理することをお勧めします。これらのディレクトリは`.gitignore`で除外されているため、誤ってコミットされることはありません。

```
ai-story-forge/
├── my-characters/              # 作成したキャラクター
│   ├── 2025-06-protagonist/    # 日付-役割で整理
│   │   ├── tanaka-misaki.character.md
│   │   └── notes.md
│   └── 2025-06-supporting/
│       ├── yamada-taro.character.md
│       └── suzuki-hanako.character.md
│
├── my-stories/                 # 作成した物語
│   ├── last-letter/           # 作品ごとにフォルダ
│   │   ├── story.md           # メインストーリー
│   │   ├── outline.md         # プロット
│   │   ├── scenes/            # 個別シーン
│   │   │   ├── scene-01-meeting.md
│   │   │   └── scene-02-revelation.md
│   │   └── quality-checks/    # 品質評価記録
│   └── digital-ghost/
│       ├── story.md
│       ├── chapters/
│       │   ├── chapter-01.md
│       │   └── chapter-02.md
│       └── character-refs/    # この物語用のキャラ設定
│
├── drafts/                    # 作業中・下書き
│   ├── ideas.md
│   ├── experimental-scene.md
│   └── dialogue-practice.md
│
└── personal-notes/            # 個人的なメモ
    ├── writing-tips.md
    ├── favorite-prompts.md
    └── my-motivation-list.md
```

## ファイル命名規則

### キャラクターファイル
- `[名前].character.md` - 例: `tanaka-misaki.character.md`
- `[名前]-[バージョン].character.md` - 例: `tanaka-misaki-v2.character.md`

### 物語ファイル
- `[タイトル].story.md` - 例: `last-letter.story.md`
- `scene-[番号]-[内容].md` - 例: `scene-03-confession.md`
- `chapter-[番号].md` - 例: `chapter-01.md`

### 作業ファイル
- `[日付]-[内容].draft.md` - 例: `2025-06-15-opening.draft.md`
- `[内容].wip.md` - 例: `climax-scene.wip.md`

## 作品の整理のコツ

### 1. 日付での管理
```
my-characters/
├── 2025-06/     # 月ごとに整理
├── 2024-02/
└── archive/      # 古い作品
```

### 2. プロジェクトごとの管理
```
my-stories/
├── project-mystery-novel/    # プロジェクト名
│   ├── characters/
│   ├── plot/
│   └── scenes/
└── project-short-stories/
    ├── story-01/
    └── story-02/
```

### 3. バージョン管理
重要な作品は個別のGitリポジトリで管理することも検討してください：
```bash
cd my-stories/important-novel
git init
git add .
git commit -m "Initial draft"
```

## セキュリティとバックアップ

### 重要な作品のバックアップ
1. **クラウドストレージ**: Google Drive、Dropbox等に定期的にバックアップ
2. **個別リポジトリ**: 重要な作品は別のプライベートリポジトリで管理
3. **エクスポート**: 定期的にPDFやWord形式でエクスポート

### プライバシーの確保
- 個人的な設定や実在の人物をモデルにしたキャラクターは、特に注意して管理
- 必要に応じて暗号化ツールの使用を検討

## コマンド使用時の保存先

Claudeコマンドを使用する際の推奨保存先：

```bash
# キャラクター作成時
/character new
# → 保存先: my-characters/2025-06/[character-name].character.md

# 物語作成時
/story new
# → 保存先: my-stories/[story-title]/story.md

# シーン作成時
/scene dialogue
# → 保存先: my-stories/[story-title]/scenes/scene-XX.md
```

## テンプレートからの作業開始

```bash
# キャラクターテンプレートをコピーして開始
cp character-template/CHARACTER.md my-characters/new-character.character.md

# 物語テンプレートをコピーして開始
cp story-template/STORY.md my-stories/new-story/story.md
```

---

💡 **ヒント**: 
- 作品フォルダは定期的に整理しましょう
- 完成した作品は`archive`フォルダに移動
- お気に入りのプロンプトは`personal-notes`に保存して再利用