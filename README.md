# govpage-snap: Bulk Screenshot Tool for Government Websites

A tool to bulk-capture screenshots of local government websites in Japan from a specified CSV list. All processes run on Google Colab, supporting digital transformation initiatives for local governments, such as periodic website monitoring and archival.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HosoyaYusaku/govpage-snap/blob/main/govpage_snap.ipynb)

-----

## ✨ Features

  - **Bulk Processing from CSV**: Automatically processes all entries from a CSV file containing municipality codes, names, and URLs.
  - **Runs Entirely on Google Colab**: No complex environment setup required. Simply open the notebook in your browser and run the cells.
  - **Robust Error Handling**: The process continues even if some sites fail to load due to timeouts or other errors.
  - **Result Report**: Automatically generates a CSV file (`results.csv`) logging the success or failure (including error details) for each site.
  - **All-in-One ZIP Download**: All captured screenshots and the result report are bundled into a single ZIP file for easy download.

## 🚀 How to Use

### 1\. What You'll Need

A CSV file listing the municipalities to be processed.

  - **Format**: `code,name,url`
  - **Character Encoding**: UTF-8 or Shift\_JIS
  - **Header Row**: Optional

**📝 CSV File Example (`sample_municipalities.csv`)**

```csv
code,name,url
012092,Yubari City,https://www.city.yubari.lg.jp/
042021,Ishinomaki City,https://www.city.ishinomaki.lg.jp/
072125,Minamisoma City,https://www.city.minamisoma.lg.jp/
075477,Namie Town,https://www.town.namie.fukushima.jp/
```

> **(Reference) Finding Municipality Lists**
> A comprehensive list of official municipal websites can be found at the following external link:
>
>   - **Official Media of Prefectures and Municipalities**: [https://uub.jp/opm/ml\_homepage.html](https://uub.jp/opm/ml_homepage.html)
>
> **【Disclaimer】**
>
>   - The above site is not affiliated with this tool in any way.
>   - Please review the terms of use and notices of the linked website before using it.
>   - We do not guarantee that the information on the linked site is always current or accurate.

### 2\. Execution Steps

1.  Click the **[Open In Colab]** button above to open the notebook in Google Colab.
2.  Run the **Step 1: Environment Setup** cell to install the necessary libraries (this may take a moment on the first run).
3.  Run the **Step 2: Upload Municipality List** cell and choose your prepared CSV file to upload.
4.  Run the **Step 3: Prepare for Execution** cell.
5.  Run the **Step 4: Execute and Download** cell to start the screenshot capture process.
6.  Once the process is complete, the download of a ZIP file containing the results will start automatically.

## 📂 About the Output

The downloaded `municipality_screenshots.zip` file contains the following:

  - **`screenshots/` (folder)**
      - Contains the screenshot images for each municipality, named `{code}_{name}.png`.
  - **`results.csv` (file)**
      - A report detailing the processing status (success/failure, error messages, etc.) for each municipality.

## ⚠️ Important Notes

  - This tool only supports SSL-enabled (HTTPS) websites starting with `https://`. Sites using `http://` may result in an error.
  - The process can be time-consuming for a large number of entries. Be mindful of Google Colab's session timeout.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---
<br>

# govpage-snap: 自治体ウェブサイト一括スクリーンショットツール

指定した自治体のウェブサイトリスト（CSV）に基づき、トップページのスクリーンショットをGoogle Colab上で一括取得するツールです。ウェブサイトの定期的な状況確認やアーカイブ化、リニューアル時の参考調査など、確認作業を効率化します。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HosoyaYusaku/govpage-snap/blob/main/govpage_snap.ipynb)

---

## ✨ 主な機能

-   **CSVから一括処理**: 自治体コード、自治体名、URLが記載されたCSVファイルを元に、全件の処理を自動実行します。
-   **Google Colabで完結**: 面倒な環境構築は不要です。ブラウザでノートブックを開き、セルを順に実行するだけで利用できます。
-   **堅牢なエラー処理**: 一部のサイトでタイムアウト等が発生しても、処理全体が停止することはありません。
-   **結果レポート出力**: サイトごとに成功・失敗（エラー内容を含む）を記録したCSVファイルを自動で生成します。
-   **ZIPで一括ダウンロード**: 取得した全スクリーンショットと結果レポートを、一つのZIPファイルにまとめて手軽にダウンロードできます。

## 🚀 使い方

### 1. 準備するもの

処理対象となる自治体の情報を記載したCSVファイルをご用意ください。

-   **ファイル形式**: `自治体コード,自治体名,URL`
-   **文字コード**: UTF-8 または Shift_JIS
-   **ヘッダー行**: 有無は問いません

**📝 CSVファイル作成例 (`sample_municipalities.csv`)**
```csv
code,name,url
012092,夕張市,https://www.city.yubari.lg.jp/
042021,石巻市,https://www.city.ishinomaki.lg.jp/
072125,南相馬市,https://www.city.minamisoma.lg.jp/
075477,浪江町,https://www.town.namie.fukushima.jp/
````

> **（参考）自治体リストの入手先**
> 全国の自治体公式サイトのリストは、以下の外部リンクなどが参考になります。
>
>   - **都道府県市区町村の公式メディア（公式HP採用自治体一覧）**: [https://uub.jp/opm/ml\_homepage.html](https://uub.jp/opm/ml_homepage.html)
>
> **【免責事項】**
>
>   - 上記サイトは本ツールとは一切関係ありません。
>   - リンク先のウェブサイトを利用する際は、各サイトの利用規約や注意事項をご確認ください。
>   - リンク先の情報が常に最新・正確であることを保証するものではありません。

### 2\. 実行手順

1.  上にある **[Open In Colab]** ボタンをクリックし、Google Colabでノートブックを開きます。
2.  **Step 1: 環境設定** のセルを実行し、必要なライブラリをインストールします（初回は少し時間がかかります）。
3.  **Step 2: 自治体リストのアップロード** のセルを実行し、準備したCSVファイルを選択してアップロードします。
4.  **Step 3: 実行準備** のセルを実行します。
5.  **Step 4: 処理実行とダウンロード** のセルを実行すると、スクリーンショット取得が開始されます。
6.  処理が完了すると、成果物を含んだZIPファイルのダウンロードが自動的に始まります。

## 📂 出力ファイルについて

ダウンロードされる `municipality_screenshots.zip` には、以下のファイルが含まれています。

  - **`screenshots/` (フォルダ)**
      - 各自治体のスクリーンショット画像（`{自治体コード}_{自治体名}.png`）が保存されます。
  - **`results.csv` (ファイル)**
      - 各自治体の処理結果（成功/失敗、エラー内容など）が記録されたレポートです。

## ⚠️ 注意事項

  - 本ツールは `https://` で始まるSSL化されたウェブサイトにのみ対応しています。`http://` のサイトはエラーとなる可能性があります。
  - 処理件数が多い場合、完了までに時間がかかります。Google Colabのセッションタイムアウトにご注意ください。

## 📄 ライセンス

このプロジェクトはMITライセンスです。詳細は `LICENSE` ファイルをご覧ください。


