# ミックスコーデ作成アプリ

アイプリ × プリマジ のパーツを組み合わせてコーデをプレビューするツール。

**URL:** https://yuishopri-rgb.github.io/e34tgea/

---

## ファイル構成

```
/
├── index.html           # アプリ本体
├── manifest.json        # データファイル一覧
├── aipri_to_csv.js      # アイプリ用 CSVエクスポートスクリプト
├── primagi_scraper.js   # プリマジ用 スクレイパー
└── data/
    ├── AP_01.csv        # アイプリ 1だん
    ├── AP_02.csv        # アイプリ 2だん
    ├── ...
    ├── APR_01.csv       # リング 1だん
    ├── OAP_01.csv       # おねがい 1だん
    ├── APSP_01.csv      # スペシャル
    ├── P1_01.csv        # プリマジ 第1章
    ├── ...
    ├── P2_01.csv        # スタジオ 第1・2章
    └── ...
```

---

## CSVファイル命名規則

### アイプリ
| シリーズ | ファイル名 |
|---------|----------|
| 1だん〜6だん | `AP_01.csv` 〜 `AP_06.csv` |
| リング1〜6だん | `APR_01.csv` 〜 `APR_06.csv` |
| おねがい1〜2だん | `OAP_01.csv` 〜 `OAP_02.csv` |
| スペシャル | `APSP_01.csv` |

### プリマジ
| シリーズ | ファイル名 |
|---------|----------|
| 第1〜6章 | `P1_01.csv` 〜 `P1_06.csv` |
| スタジオ第1・2章 | `P2_01.csv` |
| スタジオ第3・4章 | `P2_02.csv` |
| スタジオ第5・6章 | `P2_03.csv` |
| スタジオ第7・8章 | `P2_04.csv` |
| スタジオ第9章 | `P2_05.csv` |
| スタジオ第10章 | `P2_06.csv` |

---

## CSVフォーマット

```
brand,card_id,coord_name,part,img_url
"アイプリ1だん","V1-001","ポッピンハートバズリウム","ワンピース","https://..."
```

---

## データ追加手順

### アイプリ
1. `https://aipri.jp/verse/item/1.html` を開く
2. F12 → コンソールに `aipri_to_csv.js` の内容を貼り付けてEnter
3. ダウンロードされた `AP_01.csv` を `data/` に配置してpush

### プリマジ
1. `https://www.takaratomy-arts.co.jp/specials/primagi/item/P01/` を開く
2. F12 → コンソールに `primagi_scraper.js` の内容を貼り付けてEnter
3. ダウンロードされた `P1_01.csv` を `data/` に配置してpush

---

## GitHub Pages 有効化

Settings → Pages → Source: main / root → Save
