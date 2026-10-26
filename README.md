# 朝5分 銘柄ニュース

ウォッチしている銘柄の直近ニュースを、毎朝5分で読める日本語ダイジェストにまとめる個人用のスマホ向けアプリです。投資助言ではありません。

- 公開URL: https://pecpec37-gift.github.io/Stock-News/
- 毎朝 6:00ごろ（日本時間）、Claude の定期タスクが新しい号を追加します。

## 銘柄の変更

`data/watchlist.json` が銘柄リストです。アプリの「銘柄を編集」画面で追加・削除し、「保存用にコピー」→「GitHubで開く」→ 貼り付けて Commit すると、翌朝のニュースから反映されます。

## データ

- `data/watchlist.json` … ウォッチ銘柄（code / name 表示名 / formal 正式社名）
- `data/index.json` … 号の一覧（新しい順、最大30号）
- `data/editions/YYYY-MM-DD.json` … 各号の本文

`items[].codes` は関係する銘柄コードの配列、`items[].kind` は `disclosure`（開示）`earnings`（決算）`price`（株価）`index`（指数・需給）`industry`（業界）`other` のいずれか。`quiet` はニュースがなかった銘柄コードの配列です。
