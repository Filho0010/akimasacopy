# Extended Skills — Design

通常は読まない。Web UI以外の視覚資料や、より専門的なデザイン作業でCoreだけでは不足する場合に参照する。

### pptx
use: PowerPoint資料・スライド・デッキの作成、編集、読み取り、テンプレート利用、視覚設計、チャート、レイアウト、QA
not: Web UIのデザイン、文章構造だけの整理
source: https://github.com/anthropics/skills/tree/main/skills/pptx

### diagram-design
use: システム構成図、データフロー図、状態遷移図、説明用の図解をHTML＋SVGで見やすく作成し、必要に応じSVG・PNGへ書き出す
not: GitHub上で頻繁に変更する軽量なMermaid図、Web UI全体、PowerPointデッキそのもの
source: https://github.com/cathrynlavery/diagram-design/tree/main/skills/diagram-design

## Design routing

- Web UI・ダッシュボード・Webアプリ・ページの見た目と実装 → Core `frontend-design`
- PowerPoint・スライドデッキ・プレゼン資料 → `pptx`
- 見せるための構成図・フロー図をHTML / SVGで作成 → `diagram-design`。頻繁に更新するGitHub内の簡易図はMermaidも検討する
- README・報告書・辞典などの文章構造 → Core `process-business-writing`
- 内容の圧縮・要約 → Core `summarization`

## Notes

`diagram-design` は図の視覚設計用Skill。出力はHTML＋SVGであり、構成の正確性や日本語の描画は別途確認する。LKDBの取得・保存フローで試作し、ユーザーから見た目が良いとの評価を得たが、作成時のブラウザ描画検証は未実施。初回のスタイル選択等は原典の最新手順を確認する。辞典への登録は実行環境へのインストールを意味しない。


`pptx` は単なるファイル操作Skillではなく、スライドごとの視覚要素、レイアウト、配色、タイポグラフィ、チャート、余白、視覚QAまで扱う。PowerPoint形式が関係する場合の第一候補とする。
