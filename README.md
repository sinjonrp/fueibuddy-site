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
- **公開状態（GitHub API 実測 2026-07-17）: GitHub Pages 未有効（`has_pages: false`）。** リポジトリは public だが Pages 未設定のため、https://sinjonrp.github.io/fueibuddy-site/ は現時点で **404（未公開）**。Actions のデプロイ実行も 0 件で裏取り済み。＝ サイトはまだ世に出ていない
- 掃除候補: `claude/site-initial` ブランチはマージ済み・main と同一内容のため削除可

## 次にやること

1. **サイトを公開する（最優先）**: リポジトリ Settings → Pages → Build and deployment で Source =「Deploy from a branch」、Branch = `main` / `/(root)` を選んで Save。数分後に https://sinjonrp.github.io/fueibuddy-site/ （+ privacy.html / support.html）が開くことを目視確認。※ Pages の有効化は repo 設定操作で、Claude 側に該当ツールがないためブラウザ実施が必要
2. M4 ストア提出後、index.html のダウンロード節を App Store リンクに差し替える（正本 `site/` を先に更新してからコピー）
