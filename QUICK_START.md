# 5分で始めるAI Story Forge

このガイドでは、AI Story Forgeを使って最初のキャラクターと物語の骨組みを5分で作成する方法を説明します。

## 🚀 ステップ1: プロジェクトの準備（1分）

### リポジトリのクローン
```bash
git clone https://github.com/nwiizo/ai-story-forge.git
cd ai-story-forge
```

### または、必要なファイルだけコピー
最小限必要なファイル：
- `character-template/CHARACTER.md`
- `character-template/character-prompts.md`

## 📝 ステップ2: キャラクター作成（3分）

### 2-1. CHARACTER.mdをコピー
```bash
cp character-template/CHARACTER.md my-character.md
```

### 2-2. 基本情報を記入
まず、以下の4項目だけ埋めてください：
- 名前
- 年齢
- 職業
- 一言で表すと

### 2-3. AIとの対話でキャラクターを深める

#### Claude Codeをお使いの場合
```bash
# 新規キャラクター作成
/character new

# または特定のキャラクターを深化
/character develop 佐藤明日香
```

#### その他のAIツールの場合
`character-prompts.md`のStep 1をコピーして、お使いのAI（Claude、ChatGPT等）に投げてください：

```
次の人物の最も大切にしている価値観を1つだけ設定してください。

[基本設定]
- 年齢: 28歳
- 職業: 図書館司書
- 環境: 地方都市の公立図書館

条件：
- 具体的で行動の指針となるもの
- その人の人生の軸となるもの
- 「○○を通じて△△したい」の形式で
```

AIの回答を`CHARACTER.md`の「核となる価値観」欄に記入します。

## 🎯 ステップ3: 簡単な物語の骨組み作成（1分）

### Claude Codeをお使いの場合
```bash
# タイトルを指定して物語構築
/story plot "最後の手紙"

# または対話形式で開始
/story
```

### その他のAIツールの場合
AIに以下を聞いてください：

```
キャラクター：[作成したキャラクターの要約]

このキャラクターが主人公の短い物語を作りたいです。
1. どんな日常から始まりますか？（1行）
2. どんな出来事が起きますか？（1行）
3. 最後にキャラクターはどう変化しますか？（1行）
```

これで物語の骨組みが完成です！

## 🎮 Claude Codeのコマンド活用例

### キャラクター関連
```bash
/character new                    # 新規作成（対話形式）
/character develop 田中美咲       # 既存キャラクターを深化
/character check 佐藤明日香       # 一貫性をチェック
/character dialogue 山田太郎      # 対話シミュレーション
```

### シーン作成
```bash
/scene dialogue 佐藤明日香 緊張   # 会話中心のシーン
/scene emotion 田中美咲 懐かしさ 800  # 感情描写（800文字）
/scene action 緊迫               # アクションシーン
```

### 品質チェック
```bash
/quality scene "手紙の発見" --detail    # 詳細評価
/quality character 佐藤明日香           # キャラクター評価
/quality story "最後の手紙" --fix       # 改善提案付き
```

## 💡 次のステップ

### もう少し時間がある場合（+10分）

1. **キャラクターを深める**
   - `character-prompts.md`のStep 2-5を順番に実行
   - 各ステップの回答をCHARACTER.mdに記入

2. **物語を具体化する**
   - `story-template/STORY.md`を使用
   - 3幕構成を作成
   - 重要シーン3つを特定

3. **品質チェック**
   - `quality-check/checklist.md`で確認
   - 特に「キャラクター一貫性」を重視

## ❓ よくある質問

### Q: どのAIツールがおすすめ？
A: **Claude Code**なら専用コマンドで効率的に作業できます。その他、長文処理なら**Claude Opus 4**、短い対話なら**ChatGPT**がおすすめです。

### Q: キャラクターがぶれてきたら？
A: CHARACTER.mdの「核となる価値観」に立ち返ってください。すべての行動はこの価値観から生まれます。

### Q: 物語が進まなくなったら？
A: 重要シーン3つ（転換点・感情のピーク・テーマ体現）だけに集中し、他は後回しにしましょう。

## 🎉 成功のコツ

1. **完璧を求めない** - 後でいくらでも修正できます
2. **小さく始める** - まず1シーンだけ書いてみる
3. **AIとの対話を楽しむ** - 予想外の回答も創造性の源
4. **定期的に振り返る** - うまくいったプロンプトは記録
5. **コマンドを活用** - Claude Codeなら`/`で効率化

## 📚 もっと学びたい方へ

- **詳細なテクニック**: `story-template/techniques.md`
- **トラブルシューティング**: `quality-check/common-problems.md`
- **理論的背景**: `resources/principles.md`

---

**始める準備はできましたか？** まずは`CHARACTER.md`を開いて、あなたの物語の主人公を生み出しましょう！