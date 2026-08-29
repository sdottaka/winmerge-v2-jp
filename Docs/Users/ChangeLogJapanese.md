---
title: 変更履歴
---

### 2026/08/29 2.16.58-jp-3

#### 外観

* 不具合修正: 高 DPI 時のツールバーアイコン間隔が狭すぎる問題を修正した。

* ツールバーおよびマージンのアイコンを BMP から PNG に変更した。([PR #3510](https://github.com/WinMerge/winmerge/pull/3510))

* メニューバーにMDI ウィンドウのコントロール(最小化／最大化／閉じる)を常に表示するか常に非表示にするコンテキストメニューを追加した。([#3511](https://github.com/WinMerge/winmerge/issues/3511))

#### ファイル比較

* 不具合修正: 表示行フィルタ適用時、単語単位の差異表示が正しく行われないことがある問題を修正した。([#3535](https://github.com/WinMerge/winmerge/issues/3535))

* 不具合修正: 単語選択後のShift+Ctrl+左/右の選択ができないことがある問題を修正した。([#3521](https://github.com/WinMerge/winmerge/issues/3521))

* 表示行フィルタ適用時の表示速度を改善した。([PR #3517](https://github.com/WinMerge/winmerge/pull/3517))

* 画像比較時の画像読み込みで WIC デコーダーを優先するオプションを追加した。([PR #3537](https://github.com/WinMerge/winmerge/pull/3537))

#### フォルダー比較

* 不具合修正: 比較中にソートしても安全な列であれば比較中にソートできるようにした。([#3579](https://github.com/WinMerge/winmerge/issues/3579))([PR #3581](https://github.com/WinMerge/winmerge/pull/3581))

#### フィルター式

* 不具合修正: `none`と`+` での文字列連結で結果が`none`にならないようにした。([#3550](https://github.com/WinMerge/winmerge/issues/3550))

* 不具合修正: contains 演算子で大文字小文字のみの違いがある文字列を検索できないことがある問題を修正した。([#3586](https://github.com/WinMerge/winmerge/issues/3586))

#### マージモード

* マージモードインジケーターをクリック可能にし、幅を縮小した。([PR #3529](https://github.com/WinMerge/winmerge/pull/3529))

#### アーカイブサポート

* 不具合修正: ZIPファイル内のフォルダーが比較できない問題を修正した。([#3588](https://github.com/WinMerge/winmerge/issues/3588))

#### プラグイン

* 不具合修正: `BUFFER_PACK_UNPACK` プラグインの出力で最後のバイトが失われるオフバイワンバグを修正した。

* ステータスバーにプラグイン選択ボタンを追加した。([PR #3518](https://github.com/WinMerge/winmerge/pull/3518))

* メニューからパイプラインにプラグインを追加できるようにした。([PR #3523](https://github.com/WinMerge/winmerge/pull/3523))

* プラグインパイプラインにフィルター式を追加した。([PR #3530](https://github.com/WinMerge/winmerge/pull/3530))([PR #3540](https://github.com/WinMerge/winmerge/pull/3540))

* AI プラグインに MiniMax プロバイダーのサポートを追加した。([PR #3499](https://github.com/WinMerge/winmerge/pull/3499))

* AI プラグイ: ローカル LLM とOpenAI互換APIサポートを追加(#3589)

### 2026/07/29 2.16.58-jp-1

#### 全般

* 不具合修正: ファイルマッピングに失敗した場合に、誤ってクラッシュとして扱われることがある問題を修正した。([#3412](https://github.com/WinMerge/winmerge/issues/3412))

* クラッシュログのスタックトレースにモジュール相対オフセットを追加した。

#### ファイル比較

* 不具合修正: ファイルが一定のしきい値を超えて外部から変更された場合にクラッシュ (Access Violation) する問題を修正した。([#3456](https://github.com/WinMerge/winmerge/issues/3456))
  ([PR #3457](https://github.com/WinMerge/winmerge/pull/3457))

* 不具合修正: 3方向マージモードで変更をコピーした後、ペインの一部が黒い背景に黒い文字で表示されることがある問題を修正した。([#3468](https://github.com/WinMerge/winmerge/issues/3468), [#3469](https://github.com/WinMerge/winmerge/issues/3469))

#### フォルダー比較

* 不具合修正: アーカイブとフォルダーの比較で、誤った比較元が選択される問題を修正した。([#3449](https://github.com/WinMerge/winmerge/issues/3449))
  ([PR #3458](https://github.com/WinMerge/winmerge/pull/3458))

* 不具合修正: イメージリスト初期化時の HICON リソースリークを修正した。

#### ファイルまたはフォルダーの選択ダイアログ

* 不具合修正: 共通ファイルダイアログの作成時に発生した例外を適切に処理するようにした。([#3462](https://github.com/WinMerge/winmerge/issues/3462))
  ([PR #3464](https://github.com/WinMerge/winmerge/pull/3464))

* 不具合修正: 3方向比較で MRU (最近使用した項目) が正しく処理されない問題を修正した。([#3452](https://github.com/WinMerge/winmerge/issues/3452))

#### ファイル比較レポート

* 複数のファイル比較結果から 1 つの HTML レポートを生成できるようにした。([PR #3450](https://github.com/WinMerge/winmerge/pull/3450))

#### パッチ生成

* パッチ生成ダイアログに、チェックボックス付きのファイル一覧を追加した。([PR #3470](https://github.com/WinMerge/winmerge/pull/3470))

#### アーカイブ生成

* 比較結果をアーカイブとして作成できるようにした。([PR #3483](https://github.com/WinMerge/winmerge/pull/3483))

#### アーカイブサポート

* 7-Zip を 26.02 に更新した。

#### コマンドライン

* シングルインスタンスグループ用の `/g` コマンドラインオプションを追加した。([PR #3472](https://github.com/WinMerge/winmerge/pull/3472))


### 2026/06/29 2.16.56-jp-4

#### ファイル比較

* 不具合修正: 編集後にステータスバーの行番号・列番号が正しく表示されないことがある問題を修正した。

* 不具合修正: 報告されたマージ操作時のクラッシュを回避する修正をした。（未再現）([#3402](https://github.com/WinMerge/winmerge/issues/3402))

#### フォルダー比較

* 不具合修正: ファイル名変更中に[マージ]→[削除]メニューを実行するとクラッシュすることがある問題を修正した。([#3411](https://github.com/WinMerge/winmerge/issues/3411))

#### アーカイブサポート

* 不具合修正: RAR4形式ファイルのファイル比較時に不要なエラーメッセージボックスが表示される問題を修正した。([#3392](https://github.com/WinMerge/winmerge/issues/3392))

#### プロジェクトファイル

* プラグイン引数を含む他所から提供されたプロジェクトファイルを開く際、外部コマンドが実行される可能性があるため、警告メッセージを表示するようにした。([#3396](https://github.com/WinMerge/winmerge/issues/3396))
 ([PR #3397](https://github.com/WinMerge/winmerge/issues/3397))

#### クラッシュ検知

* 不具合修正: クラッシュ検知が敏感すぎて無視しようとしている例外も検知してしまっていたのを修正した。

* クラッシュログのスタックトレースを解析しやすいようにモジュール内相対アドレスも出力するようにした。

### 2026/05/29 2.16.56-jp-3

#### ファイル比較

* 不具合修正: 選択範囲が単語差分の途中で終わる場合にコピーが正しく行われない問題を修正した。[(PR #3358)](https://github.com/WinMerge/winmerge/pull/3358)

* 不具合修正: 検索・置換で非表示の行をスキップするようにした。

* 不具合修正: ワードラップモードで行番号を切り替えた際のテキストのずれや再描画の乱れを修正した。

* 不具合修正: 移動ブロック検出が有効な場合に3ペイン差分でクラッシュする問題を修正した。

* 不具合修正: 同期ポイント設置後、別ファイルをドラッグして再比較すると、左右の表示位置がずれることがある問題を修正した。

* ファイル比較ウインドウにも表示フィルターを追加した。(Ctrl+Shift+Lで表示できます) [(PR #3374)](https://github.com/WinMerge/winmerge/pull/3374)

#### フォルダー比較

* 不具合修正: 更新後にツリーの展開状態と UI の状態を保持するようにした。([#3366](https://github.com/WinMerge/winmerge/issues/3366), [PR #3369](https://github.com/WinMerge/winmerge/pull/3369))

* 不具合修正: `C:` のようなドライブ相対パスを `C:\` に変換しないようにした。[(PR #3373)](https://github.com/WinMerge/winmerge/pull/3373)

* 不具合修正: 左側または右側のみのファイルを表示する際に「右側のみのファイル」が表示されない問題を修正した。([#3378](https://github.com/WinMerge/winmerge/issues/3378))

#### 画像比較

* 不具合修正: 画像比較でセッション間に「点滅」切り替えの状態が記憶されない問題を修正した。([#3368](https://github.com/WinMerge/winmerge/issues/3368))

* 不具合修正: WebP形式等のファイルが開けなくなった問題を修正した。

#### ファイルまたはフォルダの選択ウインドウ

* 参照ボタンのドロップダウンメニューでクリップボード履歴を選択できるようにした。[(PR #3352)](https://github.com/WinMerge/winmerge/pull/3352)

#### プラグイン

* 不具合修正: プラグインの編集ダイアログで「展開後のファイル拡張子」の値が表示されない問題を修正した。

* clip:// URLハンドラーを追加した。[(PR #3352)](https://github.com/WinMerge/winmerge/pull/3352)

#### アーカイブサポート

* 7-Zip を 26.01 に更新した。

### 2026/04/29 2.16.56-jp-1

#### 全般

* ヘッダーバーに無効なパスを入力した際にエラーメッセージを表示するようにした。[(PR #3322)](https://github.com/WinMerge/winmerge/pull/3322)

* ヘッダーバーのメニューに最近使用した項目およびクリップボード履歴を追加した。[(PR #3330)](https://github.com/WinMerge/winmerge/pull/3330)

#### フォルダー比較

* [形式を指定して比較]メニューに[アーカイブ]を追加した。[(PR #3320)](https://github.com/WinMerge/winmerge/pull/3320)

* リファクタリング：オープンパラメータを統一し、再帰処理を OpenFolderParams に移動した。[(PR #3326)](https://github.com/WinMerge/winmerge/pull/3326)

* コードページフィルタ UI と HasBOM フィールド対応を追加した。[(PR #3318)](https://github.com/WinMerge/winmerge/pull/3318)

#### アーカイブサポート

* アーカイブ検出に 7-Zip IsArc API を使用し、フォーマット推定ロジックをリファクタリングした。[(PR #3323)](https://github.com/WinMerge/winmerge/pull/3323)

* アーカイブ検出よりも明示的に選択されたプラグインを優先するよう変更した。[(PR #3324)](https://github.com/WinMerge/winmerge/pull/3324)

### 2026/03/29 2.16.54-jp-4

#### ファイル比較

* 不具合修正: Alt+マウスドラッグで矩形選択すると、メニューがアクティブになってしまう問題を修正した。[(PR #3254)](https://github.com/WinMerge/winmerge/pull/3254)

* 不具合修正: 1つのファイルのみを指定する自己比較実行時、履歴に登録されない問題を修正した。[(PR #3266)](https://github.com/WinMerge/winmerge/pull/3266)

#### 画像比較

* 不具合修正: 画像比較ウインドウを閉じる際にクラッシュすることがある問題を修正した。 [(PR #3255)](https://github.com/WinMerge/winmerge/pull/3255)

* ワイプ機能を高速化した。[(winimerge/PR #33)](https://github.com/WinMerge/winimerge/pull/33)(PRをいただきました。ありがとうございます。)

#### フォルダー比較

* 不具合修正: 表示フィルターでスキップされた項目を正しくフィルターできない問題を修正した。[(PR #3267)](https://github.com/WinMerge/winmerge/pull/3267)

* フィルター式で大文字小文字の違いを無視しない文字列比較を指示するディレクティブ @cs を追加した。(例: @cs Name = "file1.txt") [(PR #3253)](https://github.com/WinMerge/winmerge/pull/3253)

* ヘッダー部のコンテキストメニューに[この列でフィルター]メニュー項目を追加した。[(PR #3268)](https://github.com/WinMerge/winmerge/pull/3268)[(PR #3284)](https://github.com/WinMerge/winmerge/pull/3284)

#### プラグイン

* .class ファイルを Javaのソースコードにデコンパイルするプラグイン DecompileJVM を追加した。[(PR #3167)](https://github.com/WinMerge/winmerge/pull/3167) (PRをいただきました。ありがとうございます。)


### 2026/03/01 2.16.54-jp-3

#### 一般

* クラッシュ発生時、次回起動時にその旨を出力ペインで通知するようにした。[(PR #3167)](https://github.com/WinMerge/winmerge/issues/3167)

#### 外観

* 不具合修正: ダークモード時に WinMerge 起動直後、背景が一瞬白く表示される問題を修正した。[(#3210)](https://github.com/WinMerge/winmerge/issues/3210)

#### ファイル比較

* IME 再変換機能に対応した。[(PR #3214)](https://github.com/WinMerge/winmerge/pull/3214)

#### フォルダー比較

* 不具合修正: 「すべてのサブフォルダーを展開」が有効でも、名前変更／移動検出が有効な場合にフォルダーが展開されない問題を修正した。

* 不具合修正: 「名前変更された項目を 1 つの項目に統合」が有効な場合に、再比較（F5）中に誤った結果が表示されたりクラッシュしたりする問題を修正した。

* 不具合修正: 名前変更／移動検出が有効な状態で、フォルダー比較のコンテキストメニューから「選択項目を更新」を実行すると、比較結果が 0 件と表示される問題を修正した。

* 不具合修正: ファイル比較でリネームしたファイルを保存しても、フォルダー比較ウィンドウが更新されない問題を修正した。

* 不具合修正: 3 方向フォルダー比較において、名前変更／移動項目に対して誤ったファイル比較が開かれる問題を修正した。

* 不具合修正: フォルダー比較の実行中は並び替えを行わないようにした。

* 不具合修正: ダブルクリック時に、開かれたファイル比較ウィンドウの移動ダイアログが表示されることがある問題を修正した。

* 不具合修正: 統合されたリネーム項目で拡張子が異なる場合に、それぞれの拡張子を表示するようにした。

* 不具合修正: 列の設定ウィンドウで列の追加・削除を行った後、不要なアニメーションが発生しないようにして表示を高速化した。

* e:/e!: フィルタープレフィックスを追加した。[(PR #3205)](https://github.com/WinMerge/winmerge/pull/3205)

* replaceWithList および regexReplaceWithList フィルター関数を追加した。[(PR #3213)](https://github.com/WinMerge/winmerge/pull/3213)

* 名前変更／移動検出キーに「置換リスト」メニューを追加した。[(PR #3215)](https://github.com/WinMerge/winmerge/pull/3215)

* フィルター関数の replace および replaceWithList で、大文字と小文字を区別しないようにした。[(PR #3222)](https://github.com/WinMerge/winmerge/pull/3222)

#### オプションダイアログ

* 不具合修正: テキストボックスのサイズ変更要求に対応した。[(#3163)](https://github.com/WinMerge/winmerge/issues/3163)

* 「名前変更項目を 1 つの項目にマージする」機能を、移動項目にも適用できるようにした。[(PR #3181)](https://github.com/WinMerge/winmerge/pull/3181)

#### プラグイン

* 不具合修正: Replace プラグインで、置換後の文字列に空文字列を指定できない問題を修正した。

* 不具合修正: プラグイン引数（${1}, ${2}, …）が正しく置換されない問題を修正した。

* .po、.pot ファイル用プラグイン PrettifyPO、ValidatePO を追加した。[(PR #3190)](https://github.com/WinMerge/winmerge/pull/3190)

* CompareMSExcelFiles プラグイン: 設定ウィンドウに「ファイル名にシート番号を含める」を追加し、チェックを外した場合はファイル名の先頭にシート番号を挿入しないようにした（「ワークブックの情報を複数ファイルに展開する」が有効な場合）。[(#3212)](https://github.com/WinMerge/winmerge/issues/3212)

#### アーカイブサポート

* 7-Zip をバージョン 26.00 に更新した。

### 2026/01/29 2.16.54-jp-1

#### 全般

* 不具合修正: キリル文字のショートカットがメインメニューのキーボードショートカットで動作しない問題を修正

* 不具合修正: 1つのプロジェクトファイルを開くとJumpListに2件登録されてしまう問題を修正 [(#2990)](https://github.com/WinMerge/winmerge/issues/2990)

* expat をバージョン 2.7.3 に更新

#### フォルダ比較

* 不具合修正: 比較中にファイルを移動した際、予期せずファイルが閉じられる問題を修正した。[(PR #3088)](https://github.com/WinMerge/winmerge/issues/3088)

* フォルダー比較に表示フィルターを追加 [(PR #3106)](https://github.com/WinMerge/winmerge/pull/3106)

* フォルダー統計用のフィルター属性とヘルパーメニューを追加 [(PR #3111)](https://github.com/WinMerge/winmerge/pull/3111)

* 範囲の包含／非包含を明示的に判定する isWithin() および inRange() を追加 [(PR #3124)](https://github.com/WinMerge/winmerge/pull/3124)

* フィルター式に logInfo / logWarn / logError 関数を追加 ([(PR #3131)](https://github.com/WinMerge/winmerge/pull/3131)

* 新しいフィルター式関数を追加 (if, ifEach, choose, chooseEach, andEach, orEach, notEach) [(PR #3132)](https://github.com/WinMerge/winmerge/pull/3132)

* フィルターに BaseName / IsFolder および新しい文字列変換関数を追加 [(PR #3146)](https://github.com/WinMerge/winmerge/pull/3146)

* フォルダー比較用の実験的な名前変更/移動検出のカスタマイズ機能を追加 [(PR #3126)](https://github.com/WinMerge/winmerge/pull/3126)

#### オプションダイアログ

* オプションダイアログの高さと「既定値」ボタンの位置を調整

#### シェルエクステンション

* 不具合修正: パスがバックスラッシュで終わる場合に Add-AppxPackage が失敗する問題を修正 [(#3145)](https://github.com/WinMerge/winmerge/pull/3145)

#### インストーラー

* インストーラーパッケージからビルド時ツール (lemon.exe, re2c.exe) を削除

#### プラグイン

* CompareMSExcelFiles: Excel 数式内の改行をスペースに置換 [(PR #3028)](https://github.com/WinMerge/winmerge/pull/3028)(PRをいただきました。ありがとうございます。)

