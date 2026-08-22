# Blend English

日本語本文の一部をランダムに英語へ置き換え、日本語の文脈を翻訳代わりにしながら読むPWAです。

## 主な機能
- 日本語文章の文分割
- 英語割合 0〜100% の調整
- 設定した英語割合に応じて、本文全体から文をランダムに英語表示
- 割合変更では配置順を維持し、`混ぜ直す`で再抽選
- 文タップで日本語 / 英語を切替
- 英文の読み上げ
- 保存したい表現のローカル保存
- 読書履歴のローカル保存
- PWA / オフライン閲覧
- ChatGPTコピペ連携（APIキー不要）
- 対応PC Chromeでは内蔵 Translator API による端末翻訳

## 重要
GitHub Pagesは静的ホスティングなので、公開リポジトリへAI APIキーを埋め込んでいません。
iPhoneでは「ChatGPTで英語化」を使ってください。英語化済みの文章は端末内に保存され、その後はオフラインでも読めます。

## GitHub Pages公開
このZIPを解凍し、**ZIPそのものではなく、解凍後の中身すべて**をGitHubリポジトリのルートへアップロードしてください。

公開起点は `index.html` です。

推奨リポジトリ名:
`blend-english-reader`

GitHub Pages:
Settings → Pages → Deploy from a branch → main / (root)

## 技術
HTML / CSS / JavaScriptのみ。ビルド不要。
