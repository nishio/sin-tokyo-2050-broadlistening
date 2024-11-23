# シン東京2050ブロードリスニングプロジェクトの個人的ファイル置き場

シン東京2050ブロードリスニングプロジェクト関連で個人的判断で公開していいものをさっと公開するためのファイル置き場

## 1122-ReHacQ
[ReHacQでの安野さんの対談](https://www.youtube.com/watch?v=BFFmfWDEH6Q)由来データ

- transcript-summary.md:
    - LLM=Claude 3.5 Sonnet, Prompt="要約して", Input=transcript.txt
- items.txt
    - LLM=Claude 3.5 Sonnet, Prompt="このYouTubeコメントから、都政に対するリクエストだけを抽出し1行1アイテムで記述せよ", Input=livechat_messages.txt

メモ:

- ライブコメントの取得は[YouTubeのコメント/トランスクリプト/ライブチャット取得](https://scrapbox.io/nishio/YouTube%E3%81%AE%E3%82%B3%E3%83%A1%E3%83%B3%E3%83%88%2F%E3%83%88%E3%83%A9%E3%83%B3%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%2F%E3%83%A9%E3%82%A4%E3%83%96%E3%83%81%E3%83%A3%E3%83%83%E3%83%88%E5%8F%96%E5%BE%97)
- Transcriptの取得もこれでできるけど、ブラウザ上でも簡単にできる: [YouTubeのTranscript](https://scrapbox.io/nishio/YouTube%E3%81%AETranscript)
- データ量が少ないので現時点ではTalk to the Cityを使うほどではないと考え、Claudeに直接渡して抽出させた