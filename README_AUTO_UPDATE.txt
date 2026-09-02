CS業務ワークハブ PWA自動更新化

1. add_pwa_auto_update_v19.html をブラウザで開く
2. 現在GitHubで使用中の index.html を選択
3. ダウンロードされた index.html をGitHubへ上書き
4. service-worker-auto-update.js を service-worker.js に改名してGitHubへ上書き
5. GitHub Pagesで新版が表示されることを確認
6. インストール済みPWAを一度閉じて開く

以後の更新:
- index.htmlをGitHubへ上書きするだけ
- キャッシュ名の変更は不要
- PWAは起動時、画面復帰時、オンライン復帰時、5分ごとに更新確認
- 新しいService Workerがあれば自動適用して1回だけ再読み込み

データについて:
- Cache Storageの更新や削除はLocalStorageを削除しません
- 顧客リスト、タスク、メモ、利用ログ集計、勉強会日程の保存データは維持されます
- Edgeの「サイトデータを削除」は実行しないでください
