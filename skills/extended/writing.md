# Extended Skills — Writing

通常は読まない。日本語の推敲でCoreの `natural-japanese` だけでは不足する場合に参照する。

### yomiyasu
use: AI生成の日本語（技術記事・設計書・仕様書・PR説明文・社内レポート等の実務文）の文構造を直す。主述・修飾の対応づけ、非生物主語の擬人化の整理、比喩動詞の平易化など、単語の置き換えでは直らない読みにくさへの対処
not: 一般的な日本語の自然化全般（第一候補はCore `natural-japanese`）、文書全体の構造設計、単なる要約、英語文
source: https://github.com/nanaism/yomiyasu/tree/main/skills/yomiyasu

## Writing routing

- 日本語を自然に仕上げる全般 → Core `natural-japanese`
- 実務文で主述のねじれ・比喩過多など、文構造の崩れが読みにくさの主因 → `yomiyasu`
- 文書全体の構造・並びの設計 → Core `process-business-writing`
- 情報の圧縮・要約 → Core `summarization`

## Notes

`yomiyasu` は2026-10-27にX投稿（@oga_aiichiro）をきっかけに登録した。未使用・未検証のためExtendedから開始する。`natural-japanese` との同時適用は避ける。どちらも削る方向の調整であり、重ねると文章が痩せる。実務文で頻用し有効性が確認できたら、Core昇格とprimaryの見直しを検討する。辞典への登録は実行環境へのインストールを意味しない。
