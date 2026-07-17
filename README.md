# fueibuddy-site

「ふうえいバディ」公式サイト（GitHub Pages 公開用）。

- 正本は `sinjonrp/FueiBuddy` リポジトリの `site/` ディレクトリ。更新時はそちらを編集してからコピーする
- 公開URL: https://sinjonrp.github.io/fueibuddy-site/

## 現在地（2026-07-17 セーブ）

- PR #1（2026-07-08 squash マージ）で index / privacy / support の3ページを初回公開済み
- 整合レビュー実測結果（2026-07-17）:
  - 外部リソース参照ゼロ・JSなし・単一HTML自己完結（全文検索で裏取り済み）
  - ページ内アンカー（#hero / #features / #flow / #faq / #download）と3ページの相互リンクは全て実在
  - 連絡先 sinjonrp@gmail.com・© 2026・プライバシーポリシー制定日 2026年7月7日 で整合。プレースホルダー・古い記述の残存なし
  - ストア導線は「App Storeで、近日公開。」表記（M4 ストア提出前の実態どおり。提出後に差し替え）
- 未確認: GitHub Pages の有効化と公開URLの生存（Claude セッションからは github.io に到達できないため、ブラウザでの目視確認が必要）
- 掃除候補: `claude/site-initial` ブランチはマージ済み・main と同一内容のため削除可

## 次にやること

1. ブラウザで https://sinjonrp.github.io/fueibuddy-site/ （と privacy.html / support.html）を開いて公開を目視確認。404 の場合はリポジトリの Settings → Pages で `main` / root を有効化する
2. M4 ストア提出後、index.html のダウンロード節を App Store リンクに差し替える（正本 `site/` を先に更新してからコピー）
