## はじめに
本リポジトリはoneshot型観光地提案アプリのソースコードを格納するリポジトリです．

## 環境構築
|              |      |
| ------------ | ---- |
| React        | 18.2 |
| TypeScript   | 4.9  |
| mui/material | 5.14 |

※その他のライブラリはpackage.json参照

npx create-react-app --template typescript [プロジェクト名]
npm install firebase
npm install npm install @mui/material @emotion/react @emotion/styled

環境変数は.env.localに以下の変数を格納する．
※空文字が格納されている変数は各自の環境に合わせて設定する．
REACT_APP_GPTAPIKEY = ""
REACT_APP_GPTURL="https://api.openai.com/v1/chat/completions"
REACT_APP_GPTMODEL="gpt-3.5-turbo"
REACT_APP_APIKEY=""
REACT_APP_AUTHDOMAIN=""
REACT_APP_DATABASEURL=""
REACT_APP_PROJECT_ID=""
REACT_APP_STORAGE_BUCKET=""
REACT_APP_MESSAGING_SENDER_ID=""
REACT_APP_APP_ID=""
REACT_APP_MEASUREMENT_ID=""
REACT_APP_MAIL_URL="http://localhost:3000/"

## 各ブランチの説明
* main：本番環境用
* dev：各機能実装後にマージする開発用(テスト環境用)
* feat-XXX：追加および修正機能開発用，基本的にはこちらのブランチを作成してプルリク出してください
※XXXには追加および修正する機能を記述します

## commitメッセージの書き方
以下のフォーマットとします。

1行目：変更内容の要約（タイトル、概要）\
2行目 ：空行\
3行目以降：変更した理由（内容、詳細）

※1行目は課題Noがある場合のみ、refs #[課題No]を記載する．

### 例
[fix]refs #110 削除フラグが更新されない不具合の修正

[detail] 更新SQLの対象カラムに削除フラグが含まれていなかったため追加しました。

### コミット種別
* fix：バグ修正
* add：新規（ファイル）機能追加
* update：機能修正（バグではない）
* remove：削除（ファイル）

## 補足
* バックエンドサーバー実装開始する場合はリポジトリを分けます
* タスク管理は「SaqQutto」で行います．
URL：<https://app.saqqutto.com/apps/board>
