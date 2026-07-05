# HisakuRankingViewer-web

hisaku ランキングビューアのフロントエンド（GitHub Pages）。

Cloudflare Worker API（`https://hisaku-ranking-api.rimuse.workers.dev`）を参照して、
イベント・大会のランキングと順位推移を表示する静的サイト。

- 単一ファイル `index.html`（ビルド不要）。推移グラフのみ CDN の Chart.js を使用。
- データ取得・蓄積は別リポジトリ（private）の HisakuRankingViewer 側で行う。

## 公開手順（GitHub Pages）

1. リポジトリの Settings → Pages
2. Source: Deploy from a branch
3. Branch: `main` / `/ (root)` を選択して Save
4. 数分後 `https://rimuse.github.io/HisakuRankingViewer-web/` で公開される

## API 接続先の変更

Worker の URL が変わった場合は `index.html` 冒頭の `const API = "..."` を書き換える。
