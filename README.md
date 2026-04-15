# TRAIL QUEST WORLD - Design Mock v2.0

プロ品質UIリデザインのHTMLモックアップリポジトリです。Claude Codeがこのモックを読み取り、Reactコンポーネントに適用します。

## 画面一覧（7画面）

| ファイル | 画面名 | 主な要素 |
|---|---|---|
| `home.html` | ホーム画面 | プレイヤーカード、バトル/クエストCTA、ランキングTOP3、ボトムナビ |
| `deck-select.html` | デッキ選択画面 | 2x3グリッド、選択状態、ロック状態、出撃ボタン |
| `deck-phase.html` | デッキフェイズ画面 | 3x3提示カード（N/R/SR/SSR）、現在のデッキ、引き直し |
| `battle.html` | バトル画面 | スコアバー、HUD、対戦フィールド（敵/味方）、手札、ターン終了 |
| `quest.html` | クエスト画面 | 難易度タブ、進捗バー、学習カルーセル、4択クイズ |
| `shop.html` | ショップ画面 | タブ切替、アイテムグリッド、購入/使用中/ロック状態 |
| `ranking.html` | ランキング画面 | マイランクカード、表彰台TOP3、ランキングリスト |

## デザインシステム

### CSS変数（`css/common.css`）

```css
:root {
  --bg-dark: #0a0e1a;
  --bg-card: #1a1f3a;
  --bg-glass: rgba(26, 31, 58, 0.8);
  --gold: #ffd700;
  --gold-dark: #c5a03f;
  --gold-light: #ffe066;
  --red: #c0392b;
  --blue: #2980b9;
  --purple: #8e44ad;
  --green: #27ae60;
  --text-primary: #ffffff;
  --text-secondary: #a0a0b0;
  --text-muted: #6a6a7a;
  --radius: 16px;
  --shadow: 0 4px 15px rgba(0,0,0,0.5);
  --glass-blur: blur(12px);
  --font-main: 'Noto Sans JP', sans-serif;
  --font-display: 'Orbitron', sans-serif;
}
```

### カードレアリティカラー

| レアリティ | 色 | CSS変数 |
|---|---|---|
| N | `#b0b0c0` | `--rarity-n` |
| R | `#4a90d9` | `--rarity-r` |
| SR | `#9b59b6` | `--rarity-sr` |
| SSR | レインボーグラデーション | `--rarity-ssr` |

### 共通コンポーネント

| クラス名 | 用途 |
|---|---|
| `glass-panel` | フロストガラスエフェクト（backdrop-filter） |
| `card-panel` | カード型パネル（ゴールドボーダー対応） |
| `btn` / `btn-battle` / `btn-quest` / `btn-confirm` / `btn-gold` / `btn-ghost` | ボタンバリエーション |
| `bottom-nav` | ボトムナビゲーション（SVGアイコン） |
| `tab-bar` / `tab-item` | タブ切替（pill / underline） |
| `badge` | バッジ（gold / silver / blue / purple / rainbow） |
| `medal` | メダル（gold / silver / bronze） |
| `hud-pill` | バトルHUD情報ピル |
| `progress-bar` | プログレスバー |
| `game-card` | カードレアリティフレーム（N/R/SR/SSR） |
| `divider` | 区切り線（ゴールドグラデーション） |

### アニメーション

| クラス名 | 効果 |
|---|---|
| `animate-fadeInUp` | フェードイン＋上方向スライド |
| `animate-pulse` | パルスアニメーション |
| `animate-glow` | ゴールドグローアニメーション |
| `animate-float` | フロートアニメーション |
| `delay-1` ~ `delay-5` | スタガードアニメーション遅延 |

## アセット構造

```
assets/
├── backgrounds/
│   ├── bg-home.png      (1080x1920, ファンタジー風景)
│   └── bg-battle.png    (1080x1920, 闘技場)
├── buttons/
│   ├── btn-battle.png   (640x120, 赤+金)
│   ├── btn-quest.png    (640x120, 青+金)
│   └── btn-confirm.png  (640x120, 緑+金)
├── frames/
│   ├── card-frame-n.png   (N: シルバー)
│   ├── card-frame-r.png   (R: ブルー)
│   ├── card-frame-sr.png  (SR: パープル)
│   └── card-frame-ssr.png (SSR: ゴールド)
└── icons/
    ├── icon-sword.png   (128x128, 透過)
    ├── icon-book.png    (128x128, 透過)
    ├── icon-coin.png    (64x64, 透過)
    ├── icon-lock.png    (64x64, 透過)
    ├── icon-star.png    (64x64, 透過)
    ├── icon-trophy.png  (64x64, 透過)
    ├── nav-home.svg     (32x32, SVG)
    ├── nav-battle.svg   (32x32, SVG)
    ├── nav-shop.svg     (32x32, SVG)
    └── nav-settings.svg (32x32, SVG)
```

## クラス命名規則

BEM風の命名を採用しています。

| パターン | 例 |
|---|---|
| ブロック | `player-card`, `action-card`, `battle-score` |
| エレメント | `player-card__name`, `action-card__icon` |
| モディファイア | `deck-card--selected`, `quest-option--correct` |

## ローカル確認方法

```bash
cd tqw-design-mock
python3 -m http.server 8080
# ブラウザで http://localhost:8080/home.html を開く
```
