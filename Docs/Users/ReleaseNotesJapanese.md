# WinMerge 2.16.20 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.20の新機能](#what-is-new-in-21620)
- [2.16.19 beta の新機能](#what-is-new-in-21619-beta)
- [既知の問題](#known-issues)

2022年4月

## このリリースについて

WinMerge の 2.16.20 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://osdn.net/projects/winmerge-jp/ticket/">こちら</a>でお願いします。

## 2.16.20 の新機能

### 全般

- ファイル名が長いとタブの右側に表示される「(U)」、「(F)」が表示されなくなってしまうため、左側に表示するようにした。(#1281 a))

### ファイル比較

- 不具合修正: 使用しているフォントによっては、タブを含む行でカレットが正しい位置に表示されないことがあるのを修正。
    (osdn.net #44417)

### Webページ比較

- Webページ比較 \[実験的\] (PR #1182)
  - WebView2 ランタイムが必要です。
  - Windows 10 以上でのみ動作します。
  - 現在、Webページ上で直接差異を強調表示することはできませんが、2つまたは3つのWebページを並べて表示できます。表示したWebページの以下の内容を比較することが可能です。
    - スクリーンショット
    - HTMLコンテンツ
    - 抽出したテキスト
    - リソースツリー

### フォルダ比較

- 不具合修正: 3つのディレクトリを比較する場合にフォルダ比較ウィンドウで大文字と小文字が異なる項目が正しく表示されない不具合を修正。
    (PR #1299)

### オプションダイアログ

- オプションダイアログを縦方向にも広げられるようにした。(#1265)

### プラグイン

- 不具合修正: CompareMSExcelFiles.sct: ExcelファイルとCSVファイルを比較した場合、CSVファイルに含まれる日付データが現在のロケールで解釈されないのを修正
    (#1279)
- [ファイルまたはフォルダの選択]ウインドウ等でファイル名の替わりにURLを指定したときにそのURLを処理できるプラグインを追加。(PR #1270)
  - HandleSchemeHTTP プラグイン (`https://winmergejp.bitbucket.io/` の様に指定すると curlコマンドを使用してリクエスト結果を表示します。curlコマンドを使用しているため、curlコマンドがインストールされている必要があります。Windows10 1803以降はcurlコマンドが標準でインストールされています。)
  - HandleSchemeReg プラグイン (`reg:HKEY_CURRENT_USER\Software\Thingamahoochie\WinMerge` の様に指定すると`reg:`の後をレジストリーキーとみなしてレジストリデータを表示します。)
- Replace プラグイン: `-e`オプションによる正規表現置換で、2番目の引数に含まれる `\r`や`\n`が制御文字CRとLFとして扱われるようにした。
- PrettifyHTML プラグイン: デフォルトプラグイン引数に `--tidy-mark no` を追加し、tidy-html5 のMETAタグが挿入されないようにした。

### コマンドライン

- コマンドラインオプション `/t webpage` を追加。

### マニュアル

- 不具合修正: SelectLines プラグインのオプションに記載されている `-g` オプションは指定しても意味はないので削除した。(#1309)

### 翻訳

- 翻訳の更新:
  - Corsican (PR #1305,#1307)
  - Bulgarian (PR #1269)
  - French (PR #1294)
  - Galician (PR 1292)
  - German (PR #1276)
  - Hungarian (PR #1274, #1306)
  - Japanese
  - Lithuanian (PR #1263, #1275)
  - Polish (PR #1272, #1287, #1288)
  - Portuguese (PR #1273, #1277)
  - Slovenian (#1289)
  - Turkish (PR #1264)

### 内部変更

- 最適化、リファクタリング。(PR #1304)
- Windows 10 SDK version 10.0.19041.0 以下でビルドするとリンクエラーが発生するのを修正。

## 2.16.19 Beta の新機能

### 全般

- タイポ修正、一部ショートカットキーの表示がないメニュー等の修正。(PR #1219,#1227,#1231,#1232)

### ファイル比較

- 不具合修正: [類似行をマッチさせる]オプションを有効にしたとき、空白の無視設定によっては期待通り動作しないことがあるのを修正。
- 不具合修正: [移動ブロック検出を有効にする]オプションを有効にしている場合、[右側/左側にコピーして次に進む]メニューまたはツールバーのアイコンをクリックすると差異が一つスキップされてしまうことがあるのを修正。
    (#1235)
- 不具合修正: F4キーによる行内差異選択が正しく動作しないことがあるのを修正。
- 不具合修正: `/x` や `/xq` 等のコマンドラインオプションを指定しているにもかかわらず、サイズが大きいファイルを比較する場合にファイルが一致していてもWinMergeが終了する動作になっていなかったのを修正。(#1218)
- [表示]→[上マージンを表示]メニューを追加。上マージンにはルーラーが表示されます。

### テーブル比較

- ヘッダー部を右クリックしたときにコンテキストメニューが表示されるようにし、[最初の行をヘッダーとして使用する]メニューを選択した場合、ヘッダー部に最初の行を列名とみなして表示するようにした。(#999)

### フォルダ比較

- 不具合修正: 複数ファイルやフォルダを選択しているにもかかわらず、ステータスバーに「0個の項目を選択」と表示されてしまうことがある問題を修正。
- 不具合修正: フォルダ比較レポートにリンクしているファイル比較レポートがファイル名によっては別のものに置き換わってしまう可能性があるのを修正。
    (PR #1171)
- 不具合修正: 同じ名前のフォルダとファイルを選択して「選択項目を最新に更新」メニューをクリックすると、比較結果が正しく表示されない問題を修正。
    (PR #1189)
- 不具合修正: [オプション]ウインドウの[比較/画像]カテゴリの[フォルダー比較で画像比較を有効にする]にチェックしてフォルダ内の画像を比較するとクラッシュすることがある問題を修正。(#1176)
- ファイルを他方にしか存在しないフォルダと同じ名前に変更した場合に結果が正しく表示されない問題を修正。(逆も同様)(PR #1246)

### ファイルフィルタ

- ファイルフィルタの拡張 (PR #1179)
  - その1: [ファイルまたフォルダーの選択]ウインドウの[フォルダー:フィルター]で`!*.bak`のように前に「!」を付けた場合、パターンにマッチしたファイルを無視するようにした。また、`!.git\`のように末尾に「\」をつけた場合、フォルダにマッチするパターンとみなすようにした。この例では、`.git` フォルダを無視して比較します。
  - その2: ファイルフィルタファイル(.fltファイル)で `f:`や`d:`に指定したパターンにマッチしたファイルまたはフォルダの一部を除外する指定 `f!:` と `d!:` を追加した。

### オプションダイアログ

- 不具合修正: [オプション]ウインドウの[メッセージボックス]カテゴリや[プラグイン]ウインドウのリストビューのツールチップが途中で切れることがあるのを修正。(#1210)
- Improve vertical alignment string (#1200)
- 不具合修正: 文字が欠けて表示される箇所を修正。(#1212)

### プラグイン

- 不具合修正: プラグインの選択ダイアログ: [パイプを追加]ボタンを押下すると入力したプラグイン引数が消えてしまうのを修正。

### 翻訳

- 翻訳の更新:
  - Catalan (PR #1237)
  - Chinese Simplified (PR #1257)
  - Chinese Traditional (PR #1204)
  - Corsican (PR #1188,#1205,#1221,#1251,#1260)
  - Dutch (PR #1187)
  - French (PR #1211)
  - German (PR #1208,#1228,#1254,#1262)
  - Hungarian (PR #1203,#1220,#1252,#1259)
  - Japanese (PR #1165)
  - Korean (PR #1181)
  - Lithuanian (PR #1197,#1202,#1224,#1255)
  - Norwegian (PR #1170)
  - Portuguese (PR #1178,#1222)
  - Russian (PR #1164)
  - Slovak (PR #1196)
  - Slovenian (PR #1163,#1261)
  - Ukrainian (PR #1172)

### 内部変更

- ソースコードのコメント内のタイポ修正。(PR #1256)
- 最適化、リファクタリング。(PR #1258)
- winmerge.orgの翻訳ページのリンクが示す先が間違っている。 (#1185)
- 翻訳ステータス生成スクリプトの改善。 (PR #1201)

## 既知の問題

 - 巨大ファイルの比較でクラッシュすることがある。(GitHub #325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 (GitHub #322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 (GitHub #296)