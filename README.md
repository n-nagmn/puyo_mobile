# puyo_mobile

HTML5 Canvas と JavaScript のみで実装された、ぷよぷよ風の落ち物パズルゲームです。
外部ライブラリを一切使用せず、単一のHTMLファイルのみで動作します。PCおよびスマートフォン（タッチ操作）に対応しています。

## Features

- **Single File**: 画像や外部スクリプトを必要とせず、HTMLファイル1つで動作します。
- **Mobile Support**: 画面上のボタンによるタッチ操作に対応。
- **Core Mechanics**: 4つ以上の連結による消去、重力による連鎖、Next/Next2の表示。
- **Responsive**: 描画にCanvas APIを使用し、軽量に動作します。

## Controls

PC（キーボード）とモバイル（タッチボタン）の両方に対応しています。

| Action | Keyboard | Touch / Mouse |
| :--- | :--- | :--- |
| **Move Left** | `←` (Arrow Left) | `←` Button |
| **Move Right** | `→` (Arrow Right) | `→` Button |
| **Soft Drop** | `↓` (Arrow Down) | `↓` Button (Long press) |
| **Rotate Left** | `Z` | `⟲` Button |
| **Rotate Right** | `X` | `⟳` Button |

## Usage

### ローカルで実行する場合
リポジトリ内の `index.html` (または `puyo_mobile.html`) をブラウザで開くだけでプレイできます。

### サーバーにデプロイする場合
このプロジェクトは静的なHTMLファイルのみで構成されているため、以下のホスティングサービス等で即座に公開可能です。

* GitHub Pages
* Vercel
* Netlify
* Apache / Nginx Web Server

## Configuration

ソースコード内の定数を変更することで、ゲームバランスを調整可能です。
`index.html` 内の `<script>` タグ冒頭を確認してください。

```javascript
const COLS = 6;           // フィールドの幅
const ROWS = 12;          // フィールドの高さ
const PUYO_SIZE = 64;     // ぷよの描画サイズ (px)
const COLORS = [          // 使用する色
  null, 
  '#ff5555', // Red
  'green',   // Green
  'blue',    // Blue
  'yellow'   // Yellow
];
````

## Tech Stack

  * **HTML5 Canvas**: ゲーム画面の描画
  * **Vanilla JavaScript**: ゲームロジック（依存ライブラリなし）
  * **CSS3**: レイアウトとスタイリング

## Directory Structure

```text
.
├── index.html    # ゲーム本体 (puyo_mobile.htmlからリネーム推奨)
└── README.md     # ドキュメント
```

## License

MIT License