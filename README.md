# fueibuddy-site

「ふうえいバディ」公式サイト（GitHub Pages 公開用）。

- 正本は `sinjonrp/FueiBuddy` リポジトリの `site/` ディレクトリ。更新時はそちらを編集してからコピーする
- 公開URL: https://sinjonrp.github.io/fueibuddy-site/
- HIG 準拠レビュー用の `apple-design` スキル導入済み（`.claude/skills/apple-design/`・レビュー専用、2026-08-02 展開）。`/apple-design` や「HIGレビュー」で発動

## 現在地（2026-07-17 セーブ）

- PR #1（2026-07-08 squash マージ）で index / privacy / support の3ページを初回公開済み
- 整合レビュー実測結果（2026-07-17）:
  - 外部リソース参照ゼロ・JSなし・単一HTML自己完結（全文検索で裏取り済み）
  - ページ内アンカー（#hero / #features / #flow / #faq / #download）と3ページの相互リンクは全て実在
  - 連絡先 sinjonrp@gmail.com・© 2026・プライバシーポリシー制定日 2026年7月7日 で整合。プレースホルダー・古い記述の残存なし
  - ストア導線は「App Storeで、近日公開。」表記（M4 ストア提出前の実態どおり。提出後に差し替え）
- **公開状態（GitHub API 実測 2026-07-17）: GitHub Pages 未有効（`has_pages: false`）。** リポジトリは public だが Pages 未設定のため、https://sinjonrp.github.io/fueibuddy-site/ は現時点で **404（未公開）**。Actions のデプロイ実行も 0 件で裏取り済み。＝ サイトはまだ世に出ていない
- 掃除候補: `claude/site-initial` ブランチはマージ済み・main と同一内容のため削除可

## ★ 公開停止中（2026-08-17〜）

**GSdesk 統合方針により、ふうえいバディ単体のストア提出とサイト公開は停止。** 単体アプリを
並べると App Store ガイドライン4.3（重複アプリ）のリスクを自分で作ることになるため
（統合はそのリスクを構造的に消すのが狙いの一つ）。

停止対象:

- STORE.md 7章の提出13手順（ASC新規App作成・bundle ID 登録・EASビルド・TestFlight・
  スクショ・メタデータ入力・Submit for Review）
- 本リポジトリの GitHub Pages 有効化（Settings→Pages の操作を**行わない**）
- J-PlatPat 商標確認

そのため `.github/workflows/deploy-pages.yml` の push トリガーを外し、**手動実行のみ**にした
（誤って公開されないようにするため）。Pages 自体も未有効のまま（`has_pages: false`）。

### 公開を再開するときの手順（統合方針の決着後）

1. Settings → Pages → Source を **GitHub Actions** にする
2. `deploy-pages.yml` の `on:` に push トリガーを戻す（または Actions タブから手動実行）
3. https://sinjonrp.github.io/fueibuddy-site/ ・privacy.html ・support.html の表示を確認

※ 過去に自動有効化（`actions/configure-pages` の `enablement: true`）を試みたが、Actions の
`GITHUB_TOKEN` では Pages サイトを作成できず失敗した（`Resource not accessible by integration`）。
再開時も Settings 操作は人手で行う必要がある。

## 次にやること

1. なし（公開停止中）。GSdesk 統合方針の決着まで、本リポジトリへの公開系の作業は行わない
2. 再開時: 上記「公開を再開するときの手順」に従う。ストア提出後は index.html のダウンロード節を
   App Store リンクに差し替える（正本 `site/` を先に更新してからコピー）
