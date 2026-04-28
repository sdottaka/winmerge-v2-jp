# WinMerge 2.16.56 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.56 の新機能](#what-is-new-in-21656)
- [2.16.55 beta の新機能](#what-is-new-in-21655-beta)
- [既知の問題](#known-issues)

2026年4月

## このリリースについて

WinMerge の 2.16.56 安定版リリースです。  
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は https://github.com/WinMerge/winmerge/issues で報告してください。  
日本語での報告は、https://sourceforge.net/p/winmerge-v2-jp/tickets/ でお願いします。

## 2.16.56 の更新内容

### 全般

* ヘッダーバーに無効なパスを入力した際にエラーメッセージを表示するようにした。[(PR #3322)](https://github.com/WinMerge/winmerge/pull/3322)

* ヘッダーバーのメニューに最近使用した項目およびクリップボード履歴を追加した。[(PR #3330)](https://github.com/WinMerge/winmerge/pull/3330)

### フォルダー比較

* [形式を指定して比較]メニューに[アーカイブ]を追加した。[(PR #3320)](https://github.com/WinMerge/winmerge/pull/3320)

* リファクタリング：オープンパラメータを統一し、再帰処理を OpenFolderParams に移動した。[(PR #3326)](https://github.com/WinMerge/winmerge/pull/3326)

* コードページフィルタ UI と HasBOM フィールド対応を追加した。[(PR #3318)](https://github.com/WinMerge/winmerge/pull/3318)

### アーカイブサポート

* アーカイブ検出に 7-Zip IsArc API を使用し、フォーマット推定ロジックをリファクタリングした。[(PR #3323)](https://github.com/WinMerge/winmerge/pull/3323)

* アーカイブ検出よりも明示的に選択されたプラグインを優先するよう変更した。[(PR #3324)](https://github.com/WinMerge/winmerge/pull/3324)

### 翻訳

* 翻訳の更新:
  * Brazilian (PR #3328,#3341)
  * Chinese Simplified (PR #3307,#3331,#3344)
  * French (PR #3312)
  * German (PR #3329)
  * Italian (PR #3335,#3342)
  * Korean (PR #3334)
  * Lithuanian (PR #3308)
  * Russian (PR #3309)
  * Turkish (PR #3333)

### ドキュメント

* イタリア語ドキュメントを更新した。[(PR #3319)](https://github.com/WinMerge/winmerge/pull/3319)

* フランス語マニュアルを更新した。[(PR #3325)](https://github.com/WinMerge/winmerge/pull/3325)

## 2.16.55 Beta の更新内容

### 全般

* 修飾キー検出における GetAsyncKeyState の誤った使用を修正した。[(PR #3257)](https://github.com/WinMerge/winmerge/pull/3257)

* POCO C++ Libraries を 1.15.1 に更新した。[(PR #3292)](https://github.com/WinMerge/winmerge/pull/3292)

### ファイル比較

* 不具合修正: Alt+マウスドラッグで矩形選択すると、メニューがアクティブになってしまう問題を修正した。[(PR #3254)](https://github.com/WinMerge/winmerge/pull/3254)

* 不具合修正: 1つのファイルのみを指定する自己比較実行時、履歴に登録されない問題を修正した。[(PR #3266)](https://github.com/WinMerge/winmerge/pull/3266)

* SaveClosingDlg::ShowAndSave を使用して保存確認ロジックをリファクタリング[(PR #3256)](https://github.com/WinMerge/winmerge/pull/3256)

* IME 再変換機能に対応した。[(PR #3214)](https://github.com/WinMerge/winmerge/pull/3214)

### 画像比較

* 不具合修正: 画像比較ウインドウを閉じる際にクラッシュすることがある問題を修正した。[(PR #3255)](https://github.com/WinMerge/winmerge/pull/3255)

* ワイプ機能を高速化した。([PR winimerge/#33](https://github.com/winimerge/winimerge/pull/33))

### フォルダー比較

* 不具合修正: 表示フィルターでスキップされた項目を正しくフィルターできない問題を修正した。[(PR #3267)](https://github.com/WinMerge/winmerge/pull/3267)

* 不具合修正：DiffWorker シャットダウン時のハングの可能性を修正した。[(PR #3300)](https://github.com/WinMerge/winmerge/pull/3300)

* 「名前変更された項目をマージ」オプションを移動された項目にも対応した。[(PR #3181)](https://github.com/WinMerge/winmerge/pull/3181)

* 比較エンジンを DiffContext を使用するようリファクタリング[(PR #3197)](https://github.com/WinMerge/winmerge/pull/3197)

* 比較結果を DIFFITEM に書き込み、FullQuickCompare を追加した。[(PR #3201)](https://github.com/WinMerge/winmerge/pull/3201)

* `e:/e!:` フィルタープレフィックスを追加した。[(PR #3205)](https://github.com/WinMerge/winmerge/pull/3205)

* replaceWithList および regexReplaceWithList フィルター関数を追加した。[(PR #3213)](https://github.com/WinMerge/winmerge/pull/3213)

* 名前変更／移動検出キーに「置換リスト」メニューを追加した。[(PR #3215)](https://github.com/WinMerge/winmerge/pull/3215)

* フィルター関数の replace および replaceWithList で、大文字と小文字を区別しないようにした。[(PR #3222)](https://github.com/WinMerge/winmerge/pull/3222)

* フィルター式で大文字小文字の違いを無視しない文字列比較を指示するディレクティブ @cs を追加した。(例: @cs Name = "file1.txt") [(PR #3253)](https://github.com/WinMerge/winmerge/pull/3253)

* ヘッダー部のコンテキストメニューに[この列でフィルター]メニュー項目を追加した。[(PR #3268)](https://github.com/WinMerge/winmerge/pull/3268)[(PR #3284)](https://github.com/WinMerge/winmerge/pull/3284)

* 比較結果によるフィルタ用の属性表示と UI を追加した。[(PR #3284)](https://github.com/WinMerge/winmerge/pull/3284)

* ツリーモードで空フォルダを非表示にする機能を追加した。[(PR #3293)](https://github.com/WinMerge/winmerge/pull/3293)

* ファイルフィルタ式に Unpacker および Prediffer フィールドを追加した。[(PR #3295)](https://github.com/WinMerge/winmerge/pull/3295)

* 比較スレッド数の動的増減に対応した。[(PR #3304)](https://github.com/WinMerge/winmerge/pull/3304)

### プラグイン

* .po、.pot ファイル用プラグイン PrettifyPO、ValidatePO を追加した。[(PR #3190)](https://github.com/WinMerge/winmerge/pull/3190)

* CompareMSExcelFiles プラグイン: 設定ウィンドウに「ファイル名にシート番号を含める」を追加し、チェックを外した場合はファイル名の先頭にシート番号を挿入しないようにした(「ワークブックの情報を複数ファイルに展開する」が有効な場合)([ #3212](https://github.com/WinMerge/winmerge/issues/3212))

* .class ファイルを Javaのソースコードにデコンパイルするプラグイン DecompileJVM を追加した。([PR #3242](https://github.com/WinMerge/winmerge/pull/3242), [PR #3243](https://github.com/WinMerge/winmerge/pull/3243))

### 翻訳

* 翻訳の更新:
  * Brazilian (PR #3185,#3194,#3219,#3231,#3245,#3275,#3287,#3303)
  * Chinese Simplified (PR #3183,#3191,#3220,#3228,#3244)
  * Corsican (PR #3259,#3299)
  * French (PR #3239)
  * German (PR #3187,#3196,#3217,#3232,#3237,#3251,#3274,#3288,#3297)
  * Hungarian (PR #3186,#3238,#3252)
  * Italian (PR #3199,#3218,#3229,#3235,#3236,#3246,#3249,#3269,#3272,#3285,#3302)
  * Japanese (PR #3258)
  * Korean (PR #3247,#3279,#3301)
  * Lithuanian (PR #3184,#3192,#3230,#3276,#3290)
  * Polish (PR #3233,#3273)
  * Russian (PR #3226,#3281)
  * Turkish (PR #3204,#3221,#3227,#3250,#3271,#3286,#3298)


### ドキュメント

* 追加：コミュニティ標準ファイル(issue テンプレート、PR テンプレートなど)[(PR #3225)](https://github.com/WinMerge/winmerge/pull/3225)

* PO ファイルにコンテキスト ID を追加し、リリース用にコメントを削除[(PR #3296)](https://github.com/WinMerge/winmerge/pull/3296)

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。([#2685](https://github.com/WinMerge/winmerge/issues/2685))
- フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。([#1391](https://github.com/WinMerge/winmerge/issues/1391))
- 巨大ファイルの比較でクラッシュすることがある。([#325](https://github.com/WinMerge/winmerge/issues/325))
- 大幅に異なるフォルダの比較が非常に時間がかかる。([#322](https://github.com/WinMerge/winmerge/issues/322))
- 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。([#296](https://github.com/WinMerge/winmerge/issues/296))
