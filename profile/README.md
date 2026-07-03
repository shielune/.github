# SHIELUNE

**Sh**ogi **I**nteroperable & **E**xtensible **L**ibraries, **U**tilities & **N**etwork **E**cosystem.

将棋のためのライブラリと道具をまとめて置いておく傘です。TypeScript を最初の住人として、Rust や Dart にも広げていきます。

---

## 何をやるところか

- **将棋関連のソースコードを、言語を問わずまとめる場所** です。
- 棋譜フォーマット、局面表現、指し手生成、思考エンジン、UI 部品 — 領域はどこでも構いません。
- TypeScript から始まっていますが、Rust / Dart / その他の実装も同じ屋根の下に揃えていく予定です。

## 主なリポジトリ

| Repo | 言語 | 概要 |
| --- | --- | --- |
| [`KIKAI`](https://github.com/shielune/KIKAI) | TypeScript | 将棋アプリケーション基盤 (Hono + Vite + Cloudflare Workers) |
| [`tsshogi-ext`](https://github.com/shielune/tsshogi-ext) | TypeScript | [`tsshogi`](https://github.com/sunfish-shogi/tsshogi) の上に載せる拡張群 (`@shielune/tsshogi-ext`)。JSA 独自バイナリ棋譜のパースなど |
| [`YaneuraOu`](https://github.com/shielune/YaneuraOu) | C++ / WASM | やねうら王思考エンジンの WASM ビルド |
| [`tsshogi-dart`](https://github.com/shielune/tsshogi-dart) | Dart | tsshogi の Dart 移植 (城・戦法・戦術検出付き) |

新しい言語 / 領域のリポジトリも同じ命名規則で追加していきます。

## パッケージ

npm scope は [`@shielune`](https://www.npmjs.com/search?q=%40shielune) に統一しています。

```jsonc
{
  "dependencies": {
    "@shielune/tsshogi-ext": "^0.9.0",
    // tsshogi 本体は sunfish-shogi さんの npm パッケージをそのまま使います
    "tsshogi": "^2.3.4"
  }
}
```

Rust crate 群は近日 crates.io に、Dart package 群は pub.dev に、同じ `shielune-*` / `shielune_*` の名前空間で配布予定です。

## tsshogi と shielune の関係

将棋の基本ライブラリ [`tsshogi`](https://github.com/sunfish-shogi/tsshogi) (作: Kubo, Ryosuke さん / MIT) は本家をそのまま利用させてもらっています。SHIELUNE 側は tsshogi を**そのまま使いつつ、その上に載る拡張・派生実装**を集めています。tsshogi のフォークや置き換えではありません。

## 名前の由来

- **SH**ogi
- **I**nteroperable &
- **E**xtensible
- **L**ibraries,
- **U**tilities &
- **N**etwork
- **E**cosystem

末尾の `LUNE` はフランス語で「月」。将棋を照らす月の光のような場所でありたい、という願いを込めています。
