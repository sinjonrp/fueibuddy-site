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

## 公開の仕組みと残手順（2026-08-17 更新）

`.github/workflows/deploy-pages.yml` を追加済み。main への push で公式 Actions が3ページを `_site` に抽出して Pages へデプロイする（`.claude/` と README は公開物に含めない）。

**ただし Pages 自体の有効化がまだ済んでいない。** ワークフロー内の `actions/configure-pages` に `enablement: true` を付けて自動有効化を試みたが、初回 run（#1）が次のエラーで失敗した:

```
Create Pages site failed. Error: Resource not accessible by integration
```

これは Actions の `GITHUB_TOKEN` では Pages サイトの新規作成ができない（権限外）ためで、ワークフロー側では解決できない。**リポジトリ所有者による Settings 操作が一度だけ必要。**

### 残手順（所有者が一度だけ実施）

1. Settings → Pages → Build and deployment → Source を **GitHub Actions** にする
   （「Deploy from a branch」で `main` / `/(root)` を選んでも公開はできるが、その場合 `.claude/` を含む全ファイルが配信対象になる。上記ワークフローは3ページだけを配信するので **GitHub Actions を推奨**）
2. Actions タブから「Deploy GitHub Pages」を再実行（または main へ何か push）
3. https://sinjonrp.github.io/fueibuddy-site/ ・ privacy.html ・ support.html が開くことを確認

※ privacy.html が開けないことが、ふうえいバディの App Store 提出の最大ブロッカー。この設定だけで解ける。

## 次にやること

1. **上記の Pages 有効化（最優先・提出ブロッカー）**
2. M4 ストア提出後、index.html のダウンロード節を App Store リンクに差し替える（正本 `site/` を先に更新してからコピー）
