# Blend English

文単位で土台言語と学習言語をランダムに混ぜ、前後の文脈から意味を取るための多言語ミックスリーダーです。

## v3.2
- 文単位ランダム混在
- 0〜100%を読みながら即時変更
- 本文は固定したまま、タップした文の対訳をその場の吹き出しに表示
- 18言語
- 見出し・段落・外部画像をできるだけ保持
- 翻訳スタイル（自然 / 原文忠実 / 学習者向け）
- 話者 / 丁寧さ / 相手 / 補足を翻訳指示へ反映
- CEFR / 英検相当レベル
- TTS読み上げ
- 保存表現 / 履歴
- 対訳確認回数から次のミックス率を提案する Flow Meter
- PWA / manual.html

## Mazelingo型の核
- 全文翻訳ではなく、一部の文だけを学習言語にする
- 比率を上げ下げして負荷を変える
- 学習言語の文をタップすると土台言語の対訳を即表示
- 土台言語の文をタップすると学習言語を即表示
- 別画面へ移動せず、読みの流れを切らない

## 翻訳
対応するChromeでは組み込みTranslator APIを利用できます。
iPhoneなどではChatGPT用指示文を生成し、JSONを貼り戻す方式を利用します。
秘密のAPIキーを公開GitHubへ埋め込みません。

## URL
- App: https://branzfamily01.github.io/blend-english-reader/
- Manual: https://branzfamily01.github.io/blend-english-reader/manual.html
