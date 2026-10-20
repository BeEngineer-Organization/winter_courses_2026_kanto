# BeEngineer 2026 冬の講習会 関東版 LP

飯田橋校・横浜校の会員生と保護者向けの、2026年冬の講習会案内ページです。プログラミング経験のある一般生、過去に BeEngineer のイベントへ参加した一般生も対象に含みます。

HTML / CSS / Vanilla JavaScript の静的サイトです。ビルドは不要です。GitHub Pages では `main` ブランチのルートを公開元にします。

## プレビュー

`index.html` をブラウザで開くか、このフォルダで次を実行します。

```bash
python -m http.server 5500

```

ブラウザで `http://localhost:5500` を開きます。

## ファイル

| ファイル | 役割 |
| --- | --- |
| `index.html` | 本文、講座、料金、日程、リンク |
| `assets/css/style.css` | 見た目 |
| `assets/js/main.js` | 校舎の絞り込み、締切を過ぎた枠の申込停止 |
| `assets/js/motion.js` | 演出（スクロールで現れる、雪など） |
| `assets/js/halloween.js` / `assets/css/halloween.css` | ハロウィン仕様（`?theme=halloween` のときだけ読み込む） |
| `assets/images/` | ロゴ、写真、OGP |
| `.nojekyll` | GitHub Pages でそのまま配信するための空ファイル |

講座・料金・開催枠の正本は HTML です。JavaScript が止まっていても、掲載した内容と申込リンクは読めます。

## 掲載講座

| ID | 校舎 | 講座名 | 日数 | 税込受講料 | 複数申込（税込） |
| --- | --- | --- | --- | --- | --- |
| `course-python-master` | 飯田橋校 | Pythonマスター講座 | 2日間 | 20,000円 | 12,000円 |
| `course-rpg` | 飯田橋校 | RPGを作ろう！ | 2日間 | 32,000円 | 24,000円 |
| `course-sudoku` | 飯田橋校 | 機械学習で数独（ナンプレ）を攻略しよう | 1日 | 16,000円 | 12,000円 |
| `course-typing` | 横浜校 | JavaScript でタイピングゲームを作ろう！ | 2日間 | 32,000円 | 24,000円 |

日程は2026年12月19日（土）〜28日（月）です。各時間帯は 14:00〜18:30 です。
※複数講座申込の際は、飯田橋校LINE(https://lin.ee/va50XGP)より問合せ案内を行っています。

## デザイン

2025年冬LPの表現を引き継いでいます。

* 地色 `#f1faff`、文字 `#00134d`、青 `#0072ff`〜シアン `#00bee8` のグラデーション
* 黄色ボタン＋濃紺のずらし影、黄色の切り欠きタグ、傾いた黄色・水色のライン
* 校舎識別ID：飯田橋校 `iidabashi`、横浜校 `yokohama`

## 申込先

| 開催枠の id | 講座 | 申込ページ |
| --- | --- | --- |
| `session-iidabashi-python-master` | 飯田橋校 Pythonマスター講座（12/19・20） | https://be-engineer.tech/event-list/516 |
| `session-yokohama-typing` | 横浜校 JavaScript でタイピングゲームを作ろう！（12/19・20） | https://be-engineer.tech/event-list/516 |
| `session-iidabashi-rpg` | 飯田橋校 RPGを作ろう！（12/26・27） | https://be-engineer.tech/event-list/516 |
| `session-iidabashi-sudoku` | 飯田橋校 機械学習で数独（ナンプレ）を攻略しよう（12/28） | https://be-engineer.tech/event-list/516 |

## 公開前チェック

* 並びが FV → 講習会紹介 → 料金 → スケジュールである
* 校舎が飯田橋校と横浜校だけである
* 講座名・日数・校舎が、紹介・料金・日程で一致している
* タイトル、OGP、フッター、フォームが 2026年冬の関東版である

```

---

### 注意点（CSS / JSについて）
`index.html` 内の校舎クラス名を `kyodai` → `iidabashi`、`umeda` → `yokohama` に書き換えております。
もし `assets/css/style.css` や `assets/js/main.js` に `kyodai` や `umeda` の記述が残っている場合、校舎別チップのカラー指定や絞り込みボタンが連動しない可能性があります。

CSSやJSの該当箇所の書き換え方法も必要でしたら、いつでもご提示できますのでお気軽におっしゃってください！

```