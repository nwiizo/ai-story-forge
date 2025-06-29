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

## Claude Codeコマンド使用時の保存先

### コマンドの引数指定

Claude Code v1.0.25以降では、コマンドに引数を渡すことができます：

```bash
# キャラクター作成（引数付き）
/character new                      # 新規作成（対話形式）
/character develop 田中美咲          # 特定キャラクターの深化
/character check 佐藤明日香          # 一貫性チェック
/character dialogue 山田太郎         # 対話シミュレーション
# → 保存先: my-characters/2025-06/[character-name].character.md

# 物語作成（引数付き）
/story plot "最後の手紙"           # タイトル指定で構築
/story structure "デジタルの亡霊"   # 構成作成
/story theme "人間とAIの共存"      # テーマから構築
# → 保存先: my-stories/[story-title]/story.md

# シーン作成（引数付き）
/scene dialogue 佐藤明日香 緊張      # 会話シーン（キャラと雰囲気指定）
/scene emotion 田中美咲 懐かしさ 800   # 感情描写（文字数指定）
/scene action 緊迫                 # アクションシーン
# → 保存先: my-stories/[story-title]/scenes/scene-XX.md

# 品質チェック（引数付き）
/quality scene "手紙の発見" --detail     # 詳細評価
/quality character 佐藤明日香 --fix      # 修正案付き
/quality story "最後の手紙" --compare   # 比較分析
# → 保存先: my-stories/[story-title]/quality-checks/check-[date].md

# 会話作成（引数付き）
/dialogue first-meet 佐藤明日香 山田太郎  # 初対面の会話
/dialogue conflict 美咲 息子 --mood 緊張   # 対立シーン
/dialogue confession --subtext       # 告白（言外の意味重視）
# → 保存先: my-stories/[story-title]/scenes/scene-XX-dialogue.md
```

### 推奨保存先のまとめ

## テンプレートからの作業開始

```bash
# キャラクターテンプレートをコピーして開始
cp character-template/CHARACTER.md my-characters/new-character.character.md

# Claude Codeで編集
/character develop new-character

# 物語テンプレートをコピーして開始
cp story-template/STORY.md my-stories/new-story/story.md

# Claude Codeで構築
/story develop new-story
```

## 効率的なワークフロー

### 新作品の開始
1. キャラクター作成： `/character new`
2. キャラクターの一貫性確認： `/character check [名前]`
3. 物語構築： `/story plot "[タイトル]"`
4. 重要シーン作成： `/scene [タイプ] [オプション]`
5. 品質チェック： `/quality story "[タイトル]" --detail`

### 既存作品の改善
1. 現状評価： `/quality story "[タイトル]"`
2. 問題点の修正： `/quality scene "[シーン名]" --fix`
3. キャラクター調整： `/character develop [名前]`
4. 会話の改善： `/dialogue [タイプ] [キャラクター]`

---

💡 **ヒント**: 
- 作品フォルダは定期的に整理しましょう
- 完成した作品は`archive`フォルダに移動
- お気に入りのプロンプトは`personal-notes`に保存して再利用
- Claude Codeのコマンド引数を活用して効率化