# 銀座セールスギャラリー — 開業チラシ（B5）

Exceed Real Estate の銀座セールスギャラリー（2026年10月18日開業）の
B5チラシ・レイアウト検討用ページ。

**Live:** https://exceed-realestate.github.io/ginza-flyer/

| ページ | 内容 |
|---|---|
| `index.html` | Version 1〜4 を1ページに |
| `version-1.html` | **Version 1（採用）** — 見出しは空の左上 |
| `versions-2-4.html` | Version 2（縦組み）／ 3（下寄せ）／ 4（左柱） |

サイズは B5 片面 182 × 257 mm。入稿時は塗り足し3mm（188 × 263 mm）。

## ページ上部のセレクタ

- **背景画像 ／ Background** — ヒーロー画像を切り替える。全バージョンに同時反映
- **レイアウト ／ Layout** — Version 1〜4 の表示切替（すべて表示も可）

どちらの選択も `localStorage` に保存されるので、再訪時も同じ状態で開く。印刷時はセレクタ自体が消える（`@media print`）。

**背景画像を追加するには** `index.html` 内の `BACKGROUNDS` 配列に1行足すだけ:

```js
const BACKGROUNDS = [
  { id:'ginza-vanishing-point',
    name:'GINZA VANISHING POINT ／ 消失点のドバイ',
    file:'assets/hero-v4-daylight.png' },
  // { id:'新しいID', name:'表示名', file:'assets/新しい画像.png' },
];
```

## ⚠️ 校了前の未確定事項

- ショールームの**階数**
- 予約用**電話番号**、**LINE ID**、**予約URL**
- 日本側の**法人名**
- ヒーロー画像は 687×1024 で**印刷解像度に不足**（要再生成）
- 「日本初」表示の**合理的根拠**（景品表示法）
- デベロッパー4社の**ロゴ使用許諾**
- ブルジュ・ハリファの**商業利用**（Emaar）

赤い「【　】未確定」タグは校正用。印刷前に削除すること。
