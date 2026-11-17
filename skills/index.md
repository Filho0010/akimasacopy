# Skill Router

目的: 通常時に読む軽量なSkill索引。ここでは候補を絞るだけで、実行時は選んだSkillの最新 `SKILL.md` を原典から取得する。

## Routing rules

1. ユーザーがSkill利用を求めた場合、まずこのファイルだけを見る。
2. `use` が最も一致するSkillを候補にする。`not` に当たる場合は除外する。
3. 迷う場合は候補を最大2件に絞り、その `SKILL.md` を取得して最終判断する。
4. Coreで足りなければ該当する `extended/*.md` だけを見る。
5. Skill本体・references・scriptsは必要になった時だけ取得する。

## Core

### find-skills
use: 必要なSkill自体を探す、既存Skillで対応できない能力を追加したい
not: 既に適切なCore Skillが明確
source: https://github.com/vercel-labs/skills/tree/main/skills/find-skills

### imozuru
use: 未知分野、検索語不明、用語・人物・場・引用から原典まで芋づる探索
not: 単一事実や明確な仕様の確認
source: https://github.com/MaryCache/imozuru/tree/main/skills/imozuru

### research
use: 問いが明確、公式資料・一次情報・仕様・ソースで裏取り
not: 分野全体を未知状態から探索
source: https://github.com/PracticalSwan/agent-skills/tree/main/research

### last30days
use: 最近の評判、SNS、コミュニティ反応、直近トレンド
not: 長期的・歴史的事実、公式仕様だけの確認
source: https://github.com/mvanhorn/last30days-skill

### literature-review
use: 論文、先行研究、研究コンセンサス、研究ギャップ
not: 一般Web中心の調査、単一論文の確認
source: https://github.com/KalarisLabs/research-agent-skills/tree/main/skills/literature-review

### policy-brief
use: 複数案を同じ基準で比較し、Trade-offを整理して推奨まで出す
not: 単なる情報収集や要約
source: https://github.com/SkillMedev/skills/tree/main/skills/policy-brief

### axiom
use: 前提を疑う、第一原理から分解、隠れた制約や思い込みを洗う
not: 単純な事実確認
source: https://github.com/sickn33/agentic-awesome-skills/tree/main/skills/axiom

### summarization
use: 長文・記事・PDF・会話を目的に合わせて圧縮、重要情報を残す
not: 文書全体の情報設計、次セッションへの状態引き継ぎ
source: https://github.com/arjunprabhulal/agent-skills/tree/main/skills/research/summarization

### process-business-writing
use: README・レポート・説明文・仕様文書などを、目的・読者・メッセージ・構造から設計して「俯瞰→詳細」の読みやすい文章に組み立てる
not: 元情報を短く圧縮するだけ、会話状態の引き継ぎ、日本語表現の自然さだけを仕上げる
source: https://github.com/aleberriz/agent-skills/tree/main/plugins/core-skills/skills/process-business-writing

### natural-japanese
use: 日本語の文章を自然で読みやすくする、AI臭さ・直訳調・曖昧な言い回しを減らす、議事録・レポート・メール・技術文書・PR説明・ブログ等を内容を変えずに書く・推敲する
not: 文書全体の論旨・構造をゼロから設計するだけ、単なる要約、事実確認そのもの
source: https://github.com/coji/natural-japanese/tree/main/skills/natural-japanese

### frontend-design
use: Web UI・ダッシュボード・Webアプリ・ページ・コンポーネントを、題材に合った明確な美術方向、配色、書体、レイアウト、インタラクションで設計・再設計する
not: PowerPoint資料、文章構造だけの整理、軽微な文言修正
source: https://github.com/anthropics/skills/tree/main/skills/frontend-design

### session-handoff
use: 長い会話の決定事項・理由・制約・却下案・未決事項を次セッションへ引き継ぐ
not: 通常の文章要約
source: https://github.com/forest/agent-skills/tree/main/plugins/session-handoff/skills/session-handoff

### editorial-fact-checker
use: 回答・文章・数字・仕様など検証可能な主張を分離して事実確認
not: 未知分野の探索そのもの
source: https://github.com/iging/agent-spec/tree/main/spec/skills/research-and-productivity/research/editorial-fact-checker

### brainstorming
use: 問題設定が曖昧、選択肢を広げたい、アイデア段階の整理
not: 既に比較対象と判断基準が明確
source: https://github.com/prrao87/agent-skills/tree/main/skills/brainstorming

## Extended routing

- 学術・深掘り調査・証拠管理 → `extended/research.md`
- 比較・購入・意思決定・複数視点 → `extended/decision.md`
- Web UI以外の視覚資料・プレゼン、説明用の構成図・フロー図 → `extended/design.md`
- 長期文脈・知識管理・引き継ぎ → `extended/context.md`
- AI運用・トークン・Skill設計 → `extended/efficiency.md`
- プログラミング・実装・デバッグ・完了確認 → `extended/coding.md`
- 日本語推敲の専門（文構造・主述・比喩） → `extended/writing.md`
