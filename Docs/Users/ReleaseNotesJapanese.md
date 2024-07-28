# WinMerge 2.16.42 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.42 の新機能](#what-is-new-in-21642)
- [2.16.41 beta の新機能](#what-is-new-in-21641-beta)
- [既知の問題](#known-issues)

2024年7月

## このリリースについて

WinMerge の 2.16.42 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21642"></a>2.16.42 の新機能

### 全般

- Windows11上でメニューが角丸になるようにした。[(PR #2364)](https://github.com/WinMerge/winmerge/pull/2364)
- ステータスバーの分割線を描画しないようにした。[(PR #2377)](https://github.com/WinMerge/winmerge/pull/2377)

### フォルダー比較

- 不具合修正: フォルダー比較のステータスがツールバーに正確に反映されていなかった問題を修正した。[(#2374)](https://github.com/WinMerge/winmerge/issues/2374)
- 不具合修正: 再読み込み(F5)後にタブアイコンがフォルダー比較のステータスを正しく反映していなかった問題を修正した。[(#2383)](https://github.com/WinMerge/winmerge/issues/2383)

### ファイル比較

- ファイル全体と選択範囲の置換をより賢く選択するように置換機能を変更した。[(#2368)](https://github.com/WinMerge/winmerge/issues/2368)

### 画像比較

- 不具合修正: 画像比較でオーバーレイアニメーション中にダイアログがフリーズする問題を修正した。[(#2370)](https://github.com/WinMerge/winmerge/issues/2370)
- ステータスバーの右端が白く表示される問題を修正した。
- 点滅間隔やオーバーレイアニメーション間隔を変更できるようにした。

### プラグイン

- AIConvertTextプラグイン設定ウィンドウでgpt4-o-miniモデルを選択可能にした。

### アーカイブサポート

- 7-Zip 24.07 に更新した。

### 翻訳

- 翻訳の更新:
  - Chinese Simplified (PR #2392)
  - Brazilian (PR #2391)
  - Hungarian (PR #2388)
  - Lithuanian (PR #2390)

## <a name="what-is-new-in-21641-beta"></a>2.16.41 beta の新機能

### 全般

- タブバーのタブを、Firefox のように角丸にした。

### ファイル比較

- F# シンタックスハイライトを追加した。 [(PR#2298)](https://github.com/WinMerge/winmerge/pull/2298)(PRをいただきました。ありがとうございます。)
- F#のパーシングを改善し、複数行コメントをサポートした。[(PR#2301)](https://github.com/WinMerge/winmerge/pull/2301)(PRをいただきました。ありがとうございます。)
- F# シンタックスハイライトの改善。 [(PR#2303)](https://github.com/WinMerge/winmerge/pull/2303)[(PR#2309)](https://github.com/WinMerge/winmerge/pull/2309)(PRをいただきました。ありがとうございます。)
- マルチラインコメント修正その2(PR #2309)
- TypeScript ファイルにJavaScriptシンタックスハイライトを適用するようにした。 [(PR#2312)](https://github.com/WinMerge/winmerge/pull/2312)(PRをいただきました。ありがとうございます。)

### フォルダー比較

- 不具合修正: [選択項目を最新に更新]をクリックして再比較した際、比較進捗ウインドウに選択していないファイル名が表示される問題を修正した。 [(#2338)](https://github.com/WinMerge/winmerge/issues/2338)
- 不具合修正: ファイルやフォルダ等を選択している状態でフォルダを展開すると別のファイルやフォルダが選択されることがある問題を修正した。[(#2359)](https://github.com/WinMerge/winmerge/issues/2359)

### オプションダイアログ

- 不具合修正: (色 > テキスト)カテゴリーの"テキストの色をカスタマイズする" を変更するとキャンセルしても(色 > シンタックス) カテゴリの設定がデフォルトに戻ってしまう問題を修正した。[(#2355)](https://github.com/WinMerge/winmerge/issues/2355)
- (エディタ > 比較/マージ) カテゴリーに「デフォルト」ボタンを追加した。 [(PR #2348)](https://github.com/WinMerge/winmerge/pull/2348)(PRをいただきました。ありがとうございます。)
- (アーカイブサポート)カテゴリーに「デフォルト」ボタンを追加した。[(PR #2362)](https://github.com/WinMerge/winmerge/pull/2362)(PRをいただきました。ありがとうございます。)

### プラグイン

- プラグインの選択ダイアログ表示時、プラグインパイプラインの設定が正しく行われていなかった問題を修正した。
- AIConvertText プラグインを追加した。 [(PR#2258)](https://github.com/WinMerge/winmerge/pull/2258) (OpenAI API を使用して、指示した通りテキストを変換します。利用には OpenAI API Key の取得が必要になります）
- md4c 0.5.2 に更新した。
- jq 1.7.1 に更新した。

### アーカイブサポート

- 7-Zip 24.05 に更新した。

### インストーラー

- 不具合修正; WinMerge 2.16.40 インストーラーにバージョン情報やアーキテクチャー情報がない [(#2300)](https://github.com/WinMerge/winmerge/issues/2300)

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2308)
  - Chinese Simplified (PR #2306,#2310,#2314,#2352)
  - Corsican (PR #2361)
  - French (PR #2354)
  - German (PR #2349)
  - Hungarian (PR #2307)
  - Italian (PR #2299)
  - Lithuanian (PR #2318,#2320)
  - Japanese
  - Korean (PR #2333)
  - Polish (PR #2313)
  - Portuguese (PR #2321)
  - Turkish (PR #2315)

### その他

- GitHub Actions CI の更新。 [(PR#2304)](https://github.com/WinMerge/winmerge/pull/2304)(PRをいただきました。ありがとうございます。)
- Typo 修正。 [(PR#2305)](https://github.com/WinMerge/winmerge/pull/2305)(PRをいただきました。ありがとうございます。)
- Boost 1.85 に更新。
- POCO C++ Libraries 1.13.3 に更新。
- Google C++ Testing Framework 1.14.0 に更新。

## <a name="known-issues"></a>既知の問題

 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
