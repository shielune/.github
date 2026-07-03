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
| [`YaneuraOu`](https://github.com/shielune/YaneuraOu) | C++ / WASM | やねうら王思考エンジンの WASM ビルド |
| [`core`](https://github.com/shielune/core) | TypeScript | 棋譜・局面・指し手を扱う基本ライブラリ (`@shielune/core`) |
| [`jsa`](https://github.com/shielune/jsa) | TypeScript | JSA (日本将棋連盟) 関連フォーマットのパーサ (`@shielune/jsa`) |

新しい言語 / 領域のリポジトリも同じ命名規則で追加していきます。

## パッケージ

npm scope は [`@shielune`](https://www.npmjs.com/search?q=%40shielune) に統一しています。

```jsonc
{
  "dependencies": {
    "@shielune/core": "^2.3.4",
    "@shielune/jsa": "^0.9.0"
  }
}
```

Rust crate 群は近日 crates.io に、Dart package 群は pub.dev に、同じ `shielune-*` / `shielune_*` の名前空間で配布予定です。

## 名前の由来

- **SH**ogi
- **I**nteroperable &
- **E**xtensible
- **L**ibraries,
- **U**tilities &
- **N**etwork
- **E**cosystem

末尾の `LUNE` はフランス語で「月」。将棋を照らす月の光のような場所でありたい、という願いを込めています。
