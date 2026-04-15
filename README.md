# TRAIL QUEST WORLD - UI Design Mock

**TRAIL QUEST WORLD** のUIデザインモックアップです。HTML + CSS + 画像のみで構成されています。

## 画面一覧

| ファイル | 画面名 | 説明 |
|---------|--------|------|
| `home.html` | ホーム画面 | プレイヤー情報、バトル/クエストボタン、ランキング |
| `deck-select.html` | デッキ選択画面 | デッキ一覧（解放済み/未解放）、出撃ボタン |
| `battle-start.html` | バトル開始画面 | デッキアイコン表示、バトル開始ボタン |
| `battle.html` | バトル画面 | 対戦フィールド、手札、フラグ表示 |

## UI素材

| ファイル | サイズ | 説明 |
|---------|--------|------|
| `button-battle.png` | 640x120px | バトルボタンテクスチャ |
| `button-quest.png` | 640x120px | クエストボタンテクスチャ |
| `frame-card-n.png` | 400x560px | Nカード枠（透過PNG） |
| `frame-card-r.png` | 400x560px | Rカード枠・金色（透過PNG） |
| `frame-card-sr.png` | 400x560px | SRカード枠・紫+金（透過PNG） |
| `frame-card-ssr.png` | 400x560px | SSRカード枠・虹色+金（透過PNG） |
| `bg-home.png` | 1080x1920px | ホーム背景 |
| `bg-battle.png` | 1080x1920px | バトル背景 |
| `icon-sword.png` | 128x128px | バトルアイコン（透過PNG） |
| `icon-book.png` | 128x128px | クエストアイコン（透過PNG） |

## デザイントーン

- **背景**: ダークブルー基調（`#0a0e1a` 〜 `#1a1f3a`）
- **アクセント**: ゴールド（`#ffd700`, `#c5a03f`）
- **テーマ**: ファンタジーカードゲーム、重厚感
- **フォント**: Noto Sans JP（太めゴシック）
- **ボタン**: 影と光沢で立体感、パルス/シマーアニメーション

## 使い方

ブラウザで `home.html` を開いてください。各画面間はリンクで遷移できます。

```bash
# ローカルサーバーで確認する場合
python3 -m http.server 8000
# http://localhost:8000/home.html にアクセス
```

## ディレクトリ構成

```
tqw-design-mock/
├── README.md
├── home.html
├── deck-select.html
├── battle-start.html
├── battle.html
├── css/
│   └── common.css
└── assets/
    └── images/
        ├── bg-home.png
        ├── bg-battle.png
        ├── button-battle.png
        ├── button-quest.png
        ├── frame-card-n.png
        ├── frame-card-r.png
        ├── frame-card-sr.png
        ├── frame-card-ssr.png
        ├── icon-sword.png
        └── icon-book.png
```
