# WinMerge 2.16.40 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.40 の新機能](#what-is-new-in-21640)
- [2.16.39 beta の新機能](#what-is-new-in-21639-beta)
- [既知の問題](#known-issues)

2024年4月

## このリリースについて

WinMerge の 2.16.40 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21640"></a>2.16.40 の新機能

### 全般

- 不具合修正: Wine上で発生する不具合をいくつか修正した。

### ファイル比較

- 不具合修正: テキストを選択状態にした後に置換すると正しく置換されないことがある問題を修正した。 [(#2279)](https://github.com/WinMerge/winmerge/issues/2279)

### オプションダイアログ

- "オプション (エディター > 一般)" ダイアログに "デフォルト" ボタンを追加した。 [(PR #2283)](https://github.com/WinMerge/winmerge/pull/2283)(PRをいただきました。ありがとうございます。)
- "オプション > 比較 > テーブル" 内の "デフォルト" ボタンの位置を調整した。 [(PR #2295)](https://github.com/WinMerge/winmerge/pull/2295)(PRをいただきました。ありがとうございます。)

### プラグイン

- 不具合修正: CompareMSExcelFiles.sct: 'ワークブックの情報を複数ファイルに展開する' オプションが有効になっている場合、10枚以上のシートを含む .xlsx ファイルのすべてのシートが比較されない問題を修正した。（このバグはバージョン2.16.39 ベータで発生しました。)
- 不具合修正: insert datetime.sct: 地域によっては正常に動作しなかった問題を修正した。（このバグはバージョン2.16.39 ベータで発生しました。）
- 不具合修正: ファイルとフォルダーの選択ウィンドウが表示されているときにプラグインを再読み込みすると "Catastrophic failure" メッセージボックスが表示される可能性がある問題を修正した。
- GUI にプラグインパイプラインのエイリアスまたは単純なプラグインを登録できるようにした。 [(PR #2257)](https://github.com/WinMerge/winmerge/pull/2257)

### インストーラー

- 不具合修正: 不具合修正: インストールの最後（最後のダイアログボックス）でのフランス語のエンコーディングの問題を修正した。 [(#2272)](https://github.com/WinMerge/winmerge/issues/2272)

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2289)
  - Catalan (PR #2270,#2274)
  - Chinese Simplified (PR #2290)
  - Corsican (PR #2288)
  - French (PR #2271,#2275)
  - Hungarian (PR #2291)
  - Japanese
  - Polish (PR#2277)

## <a name="what-is-new-in-21639-beta"></a>2.16.39 Beta の新機能

### 全般

- 不具合修正: ヘッダーバーに1文字だけを入力するとクラッシュすることがある問題を修正した。

### ファイル比較

- 不具合修正: クラッシュする可能性がある箇所を修正した。
- 不具合修正: 元のファイル名がドットで始まる場合、.bak ファイルの作成が失敗する問題を修正した。[(#2217)](https://github.com/WinMerge/winmerge/issues/2217)
- Java シンタックスハイライトのキーワードを更新した。 [(PR#2215)](https://github.com/WinMerge/winmerge/pull/2215)(PRをいただきました。ありがとうございます。)
- "Match similar lines" を "Align similar lines" に修正。[(PR #2230)](https://github.com/WinMerge/winmerge/pull/2230)(PRをいただきました。ありがとうございます。)
- テキストを選択した状態で「右にコピー」等で別ペインにコピーする際の粒度を「差異ブロック」、「行内差異」、「行」、「文字」から選択できるようにした。
  (オプションウインドウの[エディター/比較/マージ]カテゴリの[選択された差異のコピー粒度]で選択できます)[(PR#2224)](https://github.com/WinMerge/winmerge/pull/2224)
- 「右側へコピー」または「左側へコピー」でコピーするテキストをプラグインで加工できるようにした。
   ([プラグイン]→[コピー時適用エディタースクリプト]メニューでプラグインを選択できます) [(PR#2238)](https://github.com/WinMerge/winmerge/pull/2238)
- PHP シンタックスハイライトのキーワードを更新した。 [(PR#2265)](https://github.com/WinMerge/winmerge/pull/2265)(PRをいただきました。ありがとうございます。)

### Webページ比較

- 不具合修正: ロケーションペインで[イベント同期]等の設定を変更しても、次回起動時に反映されない問題を修正した。 [(#2248)](https://github.com/WinMerge/winmerge/issues/2248)

#### ファイルまたはフォルダーの選択ウインドウ

- アーカイブファイルと通常ファイルを指定した場合に比較ボタンが押せない問題を修正した。

#### HTMLレポート

- 不具合修正: HTML レポートの左ペインと右ペインの幅が等しくないことがある問題を修正した。
- 不具合修正: ヘッダー バーに設定されたキャプションが HTML レポートに適用されない問題を修正した。

### プラグイン

- 不具合修正: 展開プラグインでエラーが発生したとき、クラッシュする問題を修正した。
- VBScriptが非推奨となったため、プラグインをJScriptで書きなおした。 [(PR #2217)](https://github.com/WinMerge/winmerge/pull/2217)
- 置換フィルターのパターンを使用して置換する機能を置換プラグインに追加した。 (Replace プラグインに -s オプションを指定します) [(PR#2252)](https://github.com/WinMerge/winmerge/pull/2252)
- PrediffLineFilter プラグイン正規表現の正常性チェックを追加した。

### インストーラー

- 不具合修正: 前回のインストールで /noicons オプションが指定されていた場合、次回のインストール時に以前のスタート メニューを削除するように求めるメッセージ ボックスが表示されてしまう問題を修正した。[(#2206)](https://github.com/WinMerge/winmerge/issues/2206)
- 一部の翻訳可能メッセージを .iss ファイルから .islu ファイル達に移動した。 [(#2247)](https://github.com/WinMerge/winmerge/issues/2247)

### アーカイブサポート

- ファイル名を暗号化して圧縮した 7z ファイルを比較できない問題を修正した。[(#2225)](https://github.com/WinMerge/winmerge/issues/2225)

### その他

- codeql-analysis.yml をバージョン v2 から v3 に更新した。 [(PR #2196)](https://github.com/WinMerge/winmerge/pull/2196)

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2234,#2243)
  - Chinese Simplified (PR #2241,#2244,#2251,#2256,#2259)
  - Corsican (PR #2266)
  - French (PR #2237,#2264)
  - Hungarian (PR #2232,#2250)
  - Italian (PR #2245,#2249)
  - Japanese
  - Korean (PR #2239)
  - Lithuanian (PR #2235,#2246)
  - Portuguese (PR #2263)
  - Russian (PR #2194,#2195,#2198,#2210,#2211,#2212)
  - Slovenian (#2096)

## <a name="known-issues"></a>既知の問題

 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
