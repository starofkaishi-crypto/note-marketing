# Google ドキュメント連携台帳

スマホでの添削・記入用に使っている Google ドキュメントの一覧。
エージェントは Google Drive ツール(read_file_content)で fileId を指定して読み取る。

## 常設ドキュメント

| 用途 | fileId | 備考 |
|---|---|---|
| 体験談ストック(スマホ記入用) | `1vQPdCa0zGJjcwvRexfu8HBwmtTWXjnC66BUIwEKaGy4` | ユーザーが随時追記。「体験談同期して」の指示で assets/experiences.md に取り込む |

## 添削用ドキュメント(記事ごと)

| 記事スラッグ | 版 | fileId | 状態 |
|---|---|---|---|
| practice-without-motivation | v1 | `1c3eaxY2AqYK6TtpDXF1zZnkB14xEzwnOzlntz_pG-kw` | 反映済み(2026-07-04) |

## 運用ルール

- 添削用ドキュメントは原稿確定のたびに新規作成する(既存ドキュメントの
  上書き更新はツール上できないため、v2, v3 と版を上げる)
- 読み取り時は includeComments を有効にし、本文の直接編集とコメントの両方を拾う
- 反映後は GitHub 側(articles/)が正となる。この台帳の「状態」を更新する
