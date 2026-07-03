# note-marketing

イラスト発信のnote記事(マインドセット/テクニック論/有料note)を、
役割別AIエージェントのパイプラインで制作するリポジトリ。

## 使い方

このリポジトリで Claude Code を起動すると、Claude は自動的に
**編集長エージェント**(CLAUDE.md で定義)として振る舞う。
指示はすべて編集長に出せばよく、配下のエージェントへの割り振りは編集長が行う。

```
/article 線画が上達しない人向けのマインドセット   ← テーマ指定で記事制作開始
/article                                        ← テーマ未定ならネタ出しから
```

普通に話しかけてもよい(例:「有料noteの企画だけ先に3本出して」)。

## 初回セットアップ

`assets/persona.md` と `assets/style-guide.md` の【TODO】を自分の言葉で
埋めてから記事制作を始める(編集長に「一緒に埋めて」と頼めば
質問形式でヒアリングしてくれる)。

## 構成

```
CLAUDE.md               編集長(統括ディレクター)の定義
.claude/
  agents/               配下エージェント5人
    research-agent.md     企画・リサーチ
    outline-agent.md      構成
    writer-agent.md       執筆
    qa-agent.md           品質チェック
    publisher-agent.md    入稿・告知
  commands/article.md   /article コマンド(パイプライン実行)
assets/                 共通資産(ペルソナ・文体ガイド・品質基準・テンプレ・ネタ帳)
articles/
  briefs/               企画ブリーフ
  drafts/               構成案・原稿・QAレポート
  published/            入稿用最終稿・告知文
docs/                   設計ドキュメント
```

## 大原則

【体験談: …】プレースホルダはAIが創作しない。本人の実体験だけが商品価値。
