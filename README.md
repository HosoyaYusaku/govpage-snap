# govpage-snap: Bulk Screenshot Tool for Government Websites

A tool to bulk-capture screenshots of local government websites in Japan from a specified CSV list. All processes run on Google Colab, supporting digital transformation initiatives for local governments, such as periodic website monitoring and archival.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HosoyaYusaku/govpage-snap/blob/main/govpage-snap.ipynb)

---

## ✨ Features

- **Bulk Processing from CSV**: Automatically processes all entries from a CSV file containing municipality codes, names, and URLs.
- **Runs Entirely on Google Colab**: No complex environment setup required. Simply open the notebook in your browser and run the cells.
- **Robust Error Handling**: The process continues even if some sites fail to load due to timeouts or other errors.
- **Result Report**: Automatically generates a CSV file (`results.csv`) logging the success or failure (including error details) for each site.
- **All-in-One ZIP Download**: All captured screenshots and the result report are bundled into a single ZIP file for easy download.

## 🚀 How to Use

### What You'll Need

- **A CSV file listing the municipalities**: This file will be the input for the tool.

#### Preparing the CSV File

Create a CSV file in the following format. The tool supports both **UTF-8** and **Shift_JIS** character encodings. A header row is optional.

**Format:** `code,name,url`

**Example (`sample_municipalities.csv`):**
This sample CSV is provided as a gesture of support for municipalities working towards recovery and fiscal reconstruction.

```csv
code,name,url
012092,Yubari City,https://www.city.yubari.lg.jp/
042021,Ishinomaki City,https://www.city.ishinomaki.lg.jp/
072125,Minamisoma City,https://www.city.minamisoma.lg.jp/
075477,Namie Town,https://www.town.namie.fukushima.jp/
```

<details>
<summary><strong>Reference: Finding Municipality Lists</strong></summary>
<div>
You can find a comprehensive list of official municipal websites at the following external link.
Link: Official Media of Prefectures and Municipalities  ([https://uub.jp/opm/ml_homepage.html](https://uub.jp/opm/ml_homepage.html)) (External Link)
Disclaimer:
The above site is not affiliated with this tool in any way.
Please review the terms of use and notices of the linked website before using it.
We do not guarantee that the information on the linked site is always current or accurate.
</div>
</details>
Execution Steps
Click the [Open In Colab] button above to open the notebook in Google Colab.
Run the Step 1: Environment Setup cell to install the necessary libraries. (This may take a moment on the first run).
Run the Step 2: Upload Municipality List cell and choose your prepared CSV file to upload.
Run the Step 3: Prepare for Execution cell.
Run the Step 4: Execute and Download cell to start the screenshot capture process.
Once the process is complete, the download of a ZIP file containing the results will start automatically.
⚠️ Important Notes
This tool only supports SSL-enabled (HTTPS) websites starting with https://. Sites using http:// may result in an error.
The process can be time-consuming for a large number of entries. Be mindful of Google Colab's session timeout.
📂 About the Output
The downloaded municipality_screenshots.zip file contains the following:
screenshots/ (folder)
Contains the screenshot images for each municipality, named {code}_{name}.png.
results.csv (file)
A report detailing the processing status (success/failure, error messages, etc.) for each municipality.
📄 License
This project is licensed under the MIT License. See the LICENSE file for details.

```

govpage-snap: 自治体ウェブサイト一括スクリーンショットツール
指定した自治体のウェブサイトリスト（CSV）から、トップページのスクリーンショットをGoogle Colab上で一括取得・保存するためのツールです。HP更改時の他の団体の状況調査などを支援します。
![alt text](https://colab.research.google.com/assets/colab-badge.svg)
✨ 主な機能
CSVから一括処理: 自治体コード、自治体名、URLが記載されたCSVファイルをアップロードするだけで、全件の処理を自動実行します。
Google Colabで完結: 面倒な環境構築は不要です。ブラウザ上でノートブックを開き、上からセルを実行するだけで使えます。
堅牢なエラーハンドリング: サイトへの接続タイムアウトなど、一部のエラーが発生しても処理は停止しません。
結果レポート出力: どのサイトが成功し、どのサイトが失敗したか（エラー内容も含む）を記録したCSVファイル（results.csv）を自動で生成します。
ZIPで一括ダウンロード: 取得した全てのスクリーンショットと結果レポートは、一つのZIPファイルにまとめてダウンロードできます。
🚀 使い方
準備するもの
自治体リストCSVファイル: 処理対象となる自治体の情報を記載したCSVファイル。
CSVファイルの準備
以下のフォーマットでCSVファイルを作成してください。文字コードは UTF-8 または Shift_JIS に対応しています。1行目はヘッダーがあってもなくても構いません。
フォーマット: 自治体コード,自治体名,URL
例 (sample_municipalities.csv):
このサンプルCSVには、復興や財政再建に向けて歩む自治体へのエールの意味を込めています。

code,name,url
012092,夕張市,https://www.city.yubari.lg.jp/
042021,石巻市,https://www.city.ishinomaki.lg.jp/
072125,南相馬市,https://www.city.minamisoma.lg.jp/
075477,浪江町,https://www.town.namie.fukushima.jp/

<details>
<summary><strong>参考: 自治体リストの取得について</strong></summary>
<div>
全国の自治体公式サイトのリストは、以下の外部リンクなどが参考になります。
リンク: 都道府県市区町村の公式メディア（公式HP採用自治体一覧） ([https://uub.jp/opm/ml_homepage.html](https://uub.jp/opm/ml_homepage.html)) (外部リンク)
※免責事項:
上記サイトは、本ツールとは一切関係ありません。
リンク先のウェブサイトを利用する際は、各サイトの利用規約や注意事項等をご確認ください。
リンク先の情報が常に最新・正確であることを保証するものではありません。
</div>
</details>
実行手順
上の [Open In Colab] ボタンをクリックして、Google Colabでノートブックを開きます。
Step 1: 環境設定 のセルを実行し、必要なライブラリをインストールします。（初回は少し時間がかかります）
Step 2: 自治体リストのアップロード のセルを実行し、準備したCSVファイルを選択してアップロードします。
Step 3: 実行準備 のセルを実行します。
Step 4: 処理実行とダウンロード のセルを実行すると、スクリーンショット取得が開始されます。
処理が完了すると、成果物（スクリーンショットとレポート）を含んだZIPファイルのダウンロードが自動で始まります。
⚠️ 注意事項
本ツールは、https:// で始まるSSL化された（HTTPS）ウェブサイトにのみ対応しています。http:// のサイトはエラーとなる可能性があります。
処理件数が多い場合、完了までに時間がかかります。Google Colabのセッションがタイムアウトしないようご注意ください。
📂 出力ファイルについて
ダウンロードされる municipality_screenshots.zip には、以下のファイルが含まれています。
screenshots/ (フォルダ)
各自治体のスクリーンショット画像（{自治体コード}_{自治体名}.png）が保存されています。
results.csv (ファイル)
各自治体の処理結果（成功/失敗、エラー内容など）が記録されています。
📄 ライセンス
このプロジェクトはMITライセンスです。詳細は LICENSE ファイルをご覧ください。
```
