# WinMerge 2.16.54 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.54 の新機能](#what-is-new-in-21654)
- [2.16.53 beta の新機能](#what-is-new-in-21653-beta)
- [既知の問題](#known-issues)

2026年1月

## このリリースについて

WinMerge の 2.16.54 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## 2.16.54 の更新内容

### 全般

* 不具合修正: キリル文字のショートカットがメインメニューのキーボードショートカットで動作しない問題を修正

* 不具合修正: 1つのプロジェクトファイルを開くとJumpListに2件登録されてしまう問題を修正 [(#2990)](https://github.com/WinMerge/winmerge/issues/2990)

* expat をバージョン 2.7.3 に更新

### フォルダ比較

* フィルター式に logInfo / logWarn / logError 関数を追加 [(PR #3131)](https://github.com/WinMerge/winmerge/pull/3131)

* 新しいフィルター式関数を追加 (if, ifEach, choose, chooseEach, andEach, orEach, notEach) [(PR #3132)](https://github.com/WinMerge/winmerge/pull/3132)

* フィルターに BaseName / IsFolder および新しい文字列変換関数を追加 [(PR #3146)](https://github.com/WinMerge/winmerge/pull/3146)

* フォルダー比較用の実験的なリネーム／移動検出のカスタマイズ機能を追加 [(PR #3126)](https://github.com/WinMerge/winmerge/pull/3126)

### オプションダイアログ

* オプションダイアログの高さと「既定値」ボタンの位置を調整

### シェルエクステンション

* 不具合修正: パスがバックスラッシュで終わる場合に Add-AppxPackage が失敗する問題を修正 [(#3145)](https://github.com/WinMerge/winmerge/pull/3145)

### インストーラー

* インストーラーパッケージからビルド時ツール (lemon.exe, re2c.exe) を削除

### 翻訳

* 新しい翻訳: Vietnamese (PR #3142)
* 翻訳の更新:
  * Brazilian (PR #3150)
  * Chinese Simplified (PR #3156)
  * French (PR #3137)
  * German (PR #3148)
  * Hungarian (PR #3149)
  * Italian (PR #3147)
  * Japanese
  * Korean (PR #3125,#3127)
  * Lithuanian (PR #3144,#3153)
  * Polish (PR #3154,#3155)
  * Turkish (PR #3152)
  * Ukrainian (PR #3130)

## 2.16.53 Beta の更新内容

### 全般

* ヘッダーバーのパスを直接編集してファイルを比較できるようにした。 (ショートカットキー: Ctrl+L/Alt+D) [(PR #3093)](https://github.com/WinMerge/winmerge/pull/3093)

### ファイル比較

* 「選択されたファイルは一致しています」メッセージボックスの表示中に、完全一致するかの確認を非同期で行うようにした。 [(PR #3060)](https://github.com/WinMerge/winmerge/pull/3060)

### バイナリ比較

* 不具合修正: 権限不足などによりファイルのオープン時にエラーが発生するとクラッシュする問題を修正した。

### 画像比較

* 未サポートの画像ファイルを開いた場合に、エラーメッセージを表示して画像比較ウィンドウを自動的に閉じるようにした。

* freeimage を[3.19.10](https://github.com/danoli3/FreeImage) に更新した。

### Webページ比較

* 不具合修正: Webページ比較のタブおよびヘッダーバーに表示されるファイル名が文字化けする問題を修正した。

### フォルダー比較

* 不具合修正: アーカイブファイルの展開に失敗した際のメッセージが翻訳されない問題を修正した。 [(#3073)](https://github.com/WinMerge/winmerge/issues/3073)

* 不具合修正: 比較中にファイルを移動した際、予期せずファイルが閉じられる問題を修正した。[(PR #3088)](https://github.com/WinMerge/winmerge/issues/3088)

* フォルダー比較に表示フィルターを追加 [(PR #3106)](https://github.com/WinMerge/winmerge/pull/3106)

* フォルダー統計用のフィルター属性とヘルパーメニューを追加 [(PR #3111)](https://github.com/WinMerge/winmerge/pull/3111)

* 範囲の包含／非包含を明示的に判定する isWithin() および inRange() を追加 [(PR #3124)](https://github.com/WinMerge/winmerge/pull/3124)

### オプションダイアログ

* ユーザーデータの保存場所として AppData または Documents を選択できるオプションを[システム]ページに追加した。 [(PR #3078)](https://github.com/WinMerge/winmerge/pull/3078)

### プラグイン

* CompareMSExcelFiles: Excel 数式内の改行をスペースに置換 [(PR #3028)](https://github.com/WinMerge/winmerge/pull/3028)(PRをいただきました。ありがとうございます。)

* jq を 1.8.1 に更新した。

### 翻訳

* 翻訳更新:

* 翻訳の更新:

  * Brazilian (PR #3034,#3064,#3085,#3101,#3107,#3121)
  * Chinese Simplified (PR #3035,#3077,#3086,#3097,#3123)
  * Chinese Traditional (PR #3052,#3073,WinMerge/frhed#26)
  * Corsican (PR #3119)
  * French (PR #3072,#3105,#3106)
  * German (PR #3037,#3068,#3081,#3098,#3108,#3115)
  * Hungarian (PR #3036,#3061,#3080,#3100,#3116)
  * Italian (PR #3033,#3062,#3099,#3113,#3118)
  * Japanese
  * Korean (PR #3062,#3082)
  * Lithuanian (PR #3032,#3065,#3087,#3104,#3114)
  * Polish (PR #3050,#3089,#3103,#3112,#3122)
  * Turkish (PR #3043,#3063,#3083,#3102,#3111,#3117)

### マニュアル

* Windows エクスプローラーでのファイル選択順に関する FAQ を追加した。([#3090](https://github.com/WinMerge/winmerge/issues/3090), [#3094](https://github.com/WinMerge/winmerge/pull/3094))

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。（[#2685](https://github.com/WinMerge/winmerge/issues/2685)）
 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
