# CS業務ワークハブ PWA 配置手順

## 1. index.html を作成
1. `make_cs_workhub_pwa.html` をブラウザで開く
2. 最新の `municipality_work_hub_correspondence_notes.html` を選択
3. ダウンロードされた `index.html` を、このフォルダへ置く

## 2. GitHub Pagesへ配置
次の5ファイルをリポジトリ直下へ配置します。

- index.html
- manifest.webmanifest
- service-worker.js
- icon-192.png
- icon-512.png

## 3. Edgeでインストール
GitHub PagesのURLをEdgeで開き、画面右上の「アプリをインストール」を押します。
ボタンが出ない場合は、Edgeのメニューから「アプリ」→「このサイトをアプリとしてインストール」を選びます。

## 4. ウィンドウサイズ
インストール後のアプリを最大化して閉じると、次回起動時にEdge側が前回のウィンドウ状態を引き継ぎます。

## データ保存について
顧客リスト、タスク、アクセスログ集計、ログイン状況、勉強会日程は、現在の実装どおりブラウザのLocalStorageへ保存されます。同じURLと同じブラウザプロファイルで利用してください。

## 更新時の注意
`service-worker.js` の `CACHE_NAME` を `cs-workhub-v2` のように変更すると、利用端末で新しい版へ切り替わりやすくなります。
