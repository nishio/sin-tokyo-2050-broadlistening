# シン東京2050ブロードリスニングプロジェクトの個人的ファイル置き場

シン東京2050ブロードリスニングプロジェクト関連で個人的判断で公開していいものをさっと公開するためのファイル置き場

## 1122-ReHacQ
[ReHacQでの安野さんの対談](https://www.youtube.com/watch?v=BFFmfWDEH6Q)由来データ

データ量が少ないので現時点ではTalk to the Cityを使うほどではないと考え、Claudeに直接渡して抽出させた

- livechat_messages.txt: Live Chatの全メッセージ
- items.txt
    - LLM=Claude 3.5 Sonnet, Prompt="このYouTubeコメントから、都政に対するリクエストだけを抽出し1行1アイテムで記述せよ", Input=livechat_messages.txt
- transcript.txt: 会話の文字起こしデータ
- transcript-summary.md:
    - LLM=Claude 3.5 Sonnet, Prompt="要約して", Input=transcript.txt
- transcript-items.md
    - LLM=Claude 3.5 Sonnet, Prompt="このYouTubeの対談から、都政に対するリクエスト/改善案だけを抽出し1行1アイテムで記述せよ", Input=transcript.txt

メモ:

- ライブコメントの取得は[YouTubeのコメント/トランスクリプト/ライブチャット取得](https://scrapbox.io/nishio/YouTube%E3%81%AE%E3%82%B3%E3%83%A1%E3%83%B3%E3%83%88%2F%E3%83%88%E3%83%A9%E3%83%B3%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%97%E3%83%88%2F%E3%83%A9%E3%82%A4%E3%83%96%E3%83%81%E3%83%A3%E3%83%83%E3%83%88%E5%8F%96%E5%BE%97)
- Transcriptの取得もこれでできるけど、ブラウザ上でも簡単にできる: [YouTubeのTranscript](https://scrapbox.io/nishio/YouTube%E3%81%AETranscript)

## 1129-Anno-Miro
安野たかひろはYouTubeライブの放送中にMiroの共同編集を使ってシン東京2050ブロードリスニングのブレインストーミングを行うワークショップを開催した

https://www.youtube.com/live/KF-WJLCTyG8?si=OnfVO8W2kuUkZns4&t=3060

視聴者200人中61人が編集に参加した(スマホやテレビで見ている人はMiroに入ることに困難があった)

データ

- anno-miro-q*.csv
  - Q1~Q5のそれぞれについてMiro上で範囲選択してexportしたもの
  - Miroからexportするとどうなるかのサンプルとしてクリーニングはしていない(空文字列が含まれたり、位置情報が失われたりしている)
- organized.md
  - LLM=ChatGPT 4o, Prompt=`下記は"Q1. 自分だけが知っている東京の良いところ"に対するブレインストーミングの結果である。整理して` 他4件


質問:
- Q1. 自分だけが知っている東京の良いところ
- Q2. 自分だけが知っている東京の伸びしろ！
- Q3. たぶん高い確率でこうなるんじゃね？　という2050年の東京
- Q4. ほとんど起きないと思うけどもしかしたら起きるかも？　という2050年の東京
- Q5. 2050年、こうなってほしい！ #シン東京2050

メモ:
- だんだん場が温まったり、みんながMiroに慣れたりしたのか、質問あたりの投稿の数が増えた。Q5で141件
- Q5の開始: https://www.youtube.com/live/KF-WJLCTyG8?si=yiuSOf9LbP4s21Ac&t=6149
- 普段のYouTubeのコメントと違って、特定のテーマに対する純度の高い短文の集合で、かつ分量も少ないので「整理して」で整理できるのではと試して見たものが organized.md である。コンテキストは全ての質問で引き継いでいる(出力のフォーマットの一貫性のため, 書いている人間のコンテキストも継続しているからそっちがいいかなと) GPT Builderで指示とフォーマットをSystem Promptに入れて、コンテキスト自体は分けるという選択肢も考えられる