# VTT Grouper Tools

Democracy Now! などの動画字幕（VTT）を、翻訳作業向けにグルーピングして変換するWebツールです。

## ツール一覧

| ツール | URL | 出力形式 |
|--------|-----|----------|
| VTT to Grouped XLSX | [index.html](https://chuckmy.github.io/vtt-grouper/) | Excel (.xlsx) x 2 |
| VTT to Grouped SRT | [vtt2srt.html](https://chuckmy.github.io/vtt-grouper/vtt2srt.html) | SRT (.srt) |

## 使い方

### Step 1: VTTダウンロード

1. Democracy Now の記事URLを入力して「VTTダウンロード」をクリック
2. VTTファイルがダウンロードされる
3. テキストエディタで必要な部分だけに編集する

### Step 2: 変換

1. 編集済みのVTTファイルをドロップエリアにドラッグ＆ドロップ
2. 自動でグルーピングされ、ファイルがダウンロードされる

### XLSX版の出力ファイル（2つ）

- **`_detailed.xlsx`**: 各セグメントが個別行。グループ番号とSUM式付き（翻訳作業用）
- **`_grouped.xlsx`**: グループごとに1行にテキスト結合。タイムスタンプはグループ全体の開始〜終了

### SRT版の出力ファイル

- **`_grouped.srt`**: グルーピング済みのSRTファイル。動画プレイヤーで字幕として使用可能

## グルーピングのルール

- 1グループの目標: 約6〜9秒（最大11秒）
- 話者交代で必ず区切る（AMY GOODMAN:、KAREN HAO: など）
- 文末（. ! ?）で累計6秒以上なら区切る
- 句の区切り（; : -- "）で累計7秒以上なら区切る
- パラメータ（目標/最小/最大秒数）はUI上で調整可能
