---
title: 変更履歴(2004～2014年)
---

### 2013/12/29 2.14.0-jp-25

* 2.14.0-jp-24のフォルダ比較リポートの修正でフォルダ比較レポートからリンクするファイル比較結果が生成されなくってしまっていたのを修正...

### 2013/12/29 2.14.0-jp-24

* ご連絡いただいた以下の問題の修正
    * [同期ポイントを追加]にショートカットキーを割り当ててほしい。(Alt+Sに割り当ててみました)
    * Adobe Photoshop がインストールされていると .sct 拡張子のプラグインが動作しない。[\#28](https://bitbucket.org/winmerge/winmerge/issue/28)
    * オプション[コメントの差異を無視する]のチェックを外してもコメントの差異が無視されるとご連絡いただきましたが、
      おそらく、比較前処理プラグイン IgnoreCommentsC.dll が有効なってしまっているためだと思われます。
      このようにプラグインが適用されていることが気づきにくいため、現在適用中のプラグインの名前をステータスバーに表示するようにしました。
      なお、比較前処理プラグインの自動適用をやめるには、[プラグイン]メニュー→[手動比較前処理]を選択します。
* アーカイブファイルを含んだフォルダのフォルダ比較レポートをしようとするとクラッシュする問題を修正

### 2013/11/29 2.14.0-jp-22

* ご連絡いただいた以下のご要望の実装
    * タブを右クリックして表示されるメニューに「他の全てのタグを閉じる」、「右側のタブを全て閉じる」、「左側のタブ全て閉じる」を追加してほしい
    * フォルダ比較ウインドウからファイル比較ウインドウを開いている状態でファイル比較ウインドウを残したままフォルダ比較ウインドウを閉じると最小化されてしまう
    * 比較中のフォルダ比較ウインドウを閉じられるようにしてほしい
* フォルダ比較ウインドウから2度目以降の[圧縮]メニュー選択でエラーが発生してしまう問題を修正
* [プラグイン]メニュー→[リスト]→[プラグインを有効にする]のチェックを外したとき、少しだけフォルダ比較が高速化されるようにした

### 2013/10/29 2.14.0-jp-19

* ご連絡いただいた以下の問題を修正
    * 比較するフォルダ内に4MB以上のファイルが存在するとき、比較が進まなくなることがある
* HTMLファイルやXMLファイルを複数含むフォルダを比較すると異常終了することがある問題を修正
* meld や kdiff3 のような同期ポイントを設置する機能を追加

    #### 使い方
    1.  左側と右側両方で同期させたい行にカーソルを移動します。
    2.  [マージ]メニュー→[同期ポイントを追加]をクリックします。
    3.  void hello_world(... の行が同期します。

    ※この機能は同期ポイントというよりも分割ポイントと言ったほうがよいようなもので、同期ポイントを境にファイルを分割して比較しているだけの機能です。
    このため、設置した同期ポイントが必ずしも同じ行に表示されないことがあります。(特に差異のない行を同期ポイントとして指定した場合)

### 2013/09/29 2.14.0-jp-17

* frehd(HexView用)を同梱
* VS2010関連ファイルがフィルタされるようファイルフィルタ Merge_VC_loose.flt を変更
* ExcelプラグインでExcelブックを開くとき、余計な処理が行われないようにするたWorkbook_Open等のイベントを無効化するようにした

### 2013/08/29 2.14.0-jp-16

* フォルダ比較中のウインドウ内でフォルダを開いたとき、クラッシュすることがあった問題を修正

### 2013/07/29 2.14.0-jp-15

* ご連絡いただいた以下の問題の修正
    * ファイルを開くダイアログのサイズを変更したい[\#27](https://bitbucket.org/winmerge/winmerge/issue/27)
    * ファイルを開くダイアログから比較ウインドウを出しても、ファイルを開くダイアログが閉じない[\#26](https://bitbucket.org/winmerge/winmerge/issue/26)→  [編集]メニュー→[設定]→[一般]カテゴリの「OKボタン押下時に「ファイルまたはフォルダの選択」ダイアログを閉じる] を追加しました
* 起動時間を微妙に短縮

### 2013/06/29 2.14.0-jp-13

* ご連絡いただいた以下の問題の修正
    * 大文字小文字の違いを無視する設定で比較前処理プラグインを使用すると正常に処理されない[\#22](https://bitbucket.org/winmerge/winmerge/issue/22)
    * 64bit版でも32bit版のShellExtensionをインストールしてほしい
* フォント名を変更しても、次回起動時は元に戻っている問題を修正
* Visual Sourcesafe 連携機能が壊れていたのを修正

### 2013/05/29 2.14.0-jp-10

* 環境によっては、フォルダ比較ウインドウになにも表示されないことがある現象への対応。(ANSIビルド版(WinMerge.exe)で再現したが、UNICODEビルド版(WinMergeU.exe)では再現していないので改善されているかは不明)

### 2013/05/27 2.14.0-jp-9

* ご連絡いただいた以下の問題の修正
    * 大文字小文字の違いを無視する設定でフォルダ比較を行うと比較的サイズの大きい差異のあるファイルを同一ファイルと表示してしまうことがある。[\#20](https://bitbucket.org/winmerge/winmerge/issue/20)
    * 設定ファイルをインポートしてもフォント設定が反映されない。[\#21](https://bitbucket.org/winmerge/winmerge/issue/21)
* MFCライブラリをスタティックリンクするようにし、配布サイズを削減した

### 2013/05/20 2.14.0-jp-8

* ご連絡いただいた以下のご要望の実装
    * (C:\Users\All Usersのような）ジャンクションやシンボリックリンク等のリパースポイント以下を比較しないオプション([編集]→[オプション]→[フォルダ]カテゴリ→[リパースポイントを無視する]を追加
* プラグイン選択ダイアログでプラグインを選択するときにクラッシュすることがあった問題を修正

### 2013/05/15 2.14.0-jp-7

* ご連絡いただいた以下の問題の修正
    * タスクバー上の緑色のフォルダ比較進捗状況表示が比較が終了しても緑色のままになっている。[パッチをいただきました](https://bitbucket.org/winmerge/winmerge/commits/745b47dbd71a98346bc3cea9d2355d89d37e98dc)。ありがとうございます
    * ファイル比較ウインドウや、フォルダ比較ウインドウが表示されていない状態で[表示]→[フォントの選択]メニューからフォントの変更を行うと、WinMerge再起動後に変更前のフォントに戻る。[\#19](https://bitbucket.org/winmerge/winmerge/issue/19/) 左記状態ではフォントの選択メニューを表示しないようにしました。
* 比較前処理プラグインを自動モードにした場合、フォルダ比較時、WinMergeがクラッシュすることがあった問題を修正
* フォルダ比較ウインドウでサブディレクトリを選択して比較してもそのフォルダがジャンプリストに追加されないようにした

### 2013/04/22 2.14.0-jp-6

* スタートメニューでジャンプリストが表示されない問題を修正(ショートカットにAppIDがセットされていなかった)
* 圧縮ファイルを比較した後、ジャンプリストにテンポラリフォルダが登録されてしまう問題を修正
* ファイル比較時のメモリリークを修正
* 開くウインドウで3つのファイルをドラッグ＆ドロップしても3つ目のファイルが受付れらない問題を修正

### 2013/04/17 2.14.0-jp-5

* atl100.dllがシステムに存在しない場合、64bit版に添付したWinMerge32BitPluginProxy.exeが起動しない問題を修正。64bit版のみバージョンを変えずに差し替えています。

### 2013/04/15 2.14.0-jp-5

* ご連絡いただいた以下の問題の修正
    * -e コマンドラインオプションを指定した場合、ESCキーでWinMergeが終了するようになるが、2つ以上ウインドウを開いている場合はESCキーでWinMergeを終了せず、1つづつウインドウを閉じてほしい。[\#17](https://bitbucket.org/winmerge/winmerge/issue/17/)
    * zipファイルを比較後フォルダを比較したタブを閉じるときに、比較したファイル数が多いと一時ファイルの削除に時間がかかり次の操作が行えない。→一時ファイルの削除はWinMerge終了時に行うようにした。[\#18](https://bitbucket.org/winmerge/winmerge/issue/18/)
* WindowsXPでWinMerge終了時に一時フォルダが削除されなかったのを修正(開始時には削除されていましたが)
* xdocdiff plugin 等の32bitDLLのプラグインが64bit版のWinMergeでも使えるようにした。(作った後に気づきましたが、64bit版のxdocdiff plugin([xdocdiffPlugin64](http://crus.mydns.jp/xdocdiffPlugin64/))が既に存在していました)
* Windows 7 のタスクバーのジャンプリストで最近比較したファイルまたはフォルダが選択できるようにした。(うまく表示されない場合は一度ピン留を付け直すと表示されるかもしれません)
* プロジェクトファイル内のパス等に'&'等の文字が含まれていた場合にファイルが開けなくなっていたのを修正

### 2013/03/17 2.14.0-jp-4

* ご連絡いただいた以下の問題の修正
    * エクスプローラ上の右クリックドラッグアンドドロップでWinMergeのメニューが表示されない
    * WinMergeへShiftキーを押しながらファイルを一つドラッグするとクラッシュする
    * WinMergeU.exe と同じフォルダに レジストリファイル WinMerge.reg をおいた場合にそのレジストリ情報を実行インポート、終了時エクスポートする機能が動作しない [\#16](https://bitbucket.org/winmerge/winmerge/issue/16/)

### 2013/03/04 2.14.0-jp-3

* ご連絡いただいた以下の問題の修正
    * 前バージョンの修正（「改行文字の違いを無視する」の設定にもかかわらず、フォルダ比較時、改行コード以外に違いがないファイルを差異があると表示してしまうことがある)がまだ完全ではない
    * 比較前処理プラグインでUTF-8のファイルを正常に処理できない
    * フォルダ比較ウインドウから異なるファイルを開き、ファイル比較画面でファイルの内容を一致させたにもかかわらず、フォルダ比較ウインドウに反映されない
    * カスタムコードページに65001(UTF-8)を選択している場合、フォルダ比較時に同じ内容のバイナリファイルが差異があると表示されることがある
    * カスタムコードページに65001(UTF-8)を選択している場合、フォルダ比較時に0バイトサイズのファイルが比較できないと表示される
    * フォルダ比較ウインドウで複数ファイルを選択し、[パス名をコピー]メニューを実行するとスペースで区切られたパスがクリップボードにコピーされる。2.12では改行で区切られていた。→ これは、2.14での仕様変更でしたが元に戻しました。そのかわり、[項目をクリップボードにコピー]でファイルそのものと共にスペースで区切られたパスもクリップボードにコピーするようにしました。

### 2013/02/18 2.14.0-jp-2

* ご連絡いただいた以下の問題の修正
    * 「改行文字の違いを無視する」の設定にもかかわらず、フォルダ比較時、改行コード以外に違いがないファイルを差異があると表示してしまうことがある
    * 1ブロックの差異行の行数が長い場合、単語単位の差異を検出しなくなり、1ブロック全体が差異として表示される(これは比較時間が長くなりすぎなくするための処置でしたが、前よりこのように表示されにくくしました）

### 2013/02/12 2.14.0-jp-1

* 本家で 2.14.0 がリリースされたので更新
* ご連絡いただいた以下の問題の修正
    * 一時フォルダ内に存在するフォルダの先頭が"WM_"だった場合、WinMerge起動時にそのフォルダが削除されてしまう。
* エディタプラグイン(editor addin.sct)に選択範囲の行をソートする機能と任意のフィルタコマンドの実行結果で置換する機能を追加
* フォルダ比較レポートを色付きにした
* Windows98で動作しなくなっていたので98/ME/2000版サポートを断念

### 2013/02/04 2.13.22+-jp-2

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウで表示されるファイルのタイムスタンプがUTCになっている。
* フォルダ比較状況の表示の仕方を変更
* Explorerシェルエクステンションアイコンの背景がVista以降で透明にならない問題を修正
* 0バイトのファイルを開くとエラーが発生する問題を修正

### 2013/01/21 2.13.22+-jp-1

* マルチコア・マルチCPUのマシンならばフォルダ比較時に各ファイルの比較を並列に実行するようにしてみた
* 64bit版でたまにメニューのキーボードショートカットが受け付けられないことがある問題を修正
* WinMerge-2.13.22-jp-1-Setup.exe.zipのアップロードに失敗していたのでアップロードし直しました。(21:15)

### 2012/03/26 2.12.4+-jp-31, 2.13.20+-jp-12

* ご連絡いただいた以下の問題の修正
    * /eオプション指定(ESCキーで終了)で起動したとき、設定ウインドウで「複数のウインドウを閉じるときに尋ねる」のチェックが入っているにもかかわらず、
* プラグインを無効化している場合、フォルダ比較時一時ファイルがテンポラリフォルダ(%TEMP%)に残ってしまうことがある問題を修正。

### 2012/02/13 2.13.20+-jp-11

* ご連絡いただいた以下の問題の修正
    * [垂直分割]メニューにチェックが入っているにもかかわらず、ウインドウが水平に分割される。
* 64ビット版WinMergeでプラグインがインストールされていると終了時にエラーが発生することがある問題の修正。
* フォルダ比較レポートにファイル比較レポートをリンクできるようにした。

### 2012/02/05 2.12.4+-jp-30, 2.13.20+-jp-10

* ご連絡いただいた以下の問題の修正
    * 'ケ'と'パ'、'サ'と'フ'、 'ジ'と'ヘ'等が「大文字と小文字を区別しない」場合に同じとみなされる
* ヘルプの日本語化更新

### 2011/12/29 2.12.4+-jp-29, 2.13.20+-jp-9

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウからファイルを開いた後、ファイルを開いたままフォルダ比較ウインドウで開いたファイルの[項目を非表示]にした後、ファイルを変更して保存するとWinMergeがクラッシュする。

### 2011/11/24 2.12.4+-jp-28, 2.13.20+-jp-8

* ご連絡いただいた以下の問題の修正
    * 外部エディタのパスとして相対パスを指定するとファイルやフォルダ選択ダイアログで選択後に外部エディタの実行に失敗する。

### 2011/10/11 2.12.4+-jp-27, 2.13.20+-jp-7

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウの[項目をクリップボードにコピー]メニューが動作しなくなっていた。
* ヘルプの日本語化更新

### 2011/08/08 2.12.4+-jp-26, 2.13.20+-jp-6

* ご連絡いただいた以下の問題の修正
    * 3wayファイル比較ウインドウで最右ペインのサイズを縮小すると再描画されない領域が現れてしまう

### 2011/08/01 2.12.4+-jp-25

* ご連絡いただいた以下の問題の修正
    * 一方が空行のとき行内の差異を選択を実行すると強制終了する

### 2011/07/20 2.12.4+-jp-24, 2.13.20+-jp-5

* ご連絡いただいた以下の問題の修正
    * BMP外の文字を含むUTF-8のファイルが正しく読み込めない

### 2011/07/04 2.13.20+-jp-4

* 「開く」ダイアログの表示中でも親ウインドウのリサイズができるようにした。

### 2011/06/27 2.13.20+-jp-3

* ご連絡いただいた以下の問題の修正
    * 再帰的ではないフォルダ比較時に、サブディレクトリへ移動後、親フォルダへ移動できない
    * フォルダ比較時、1つしかない名前が異なるサブフォルダをマッチさせて比較してしまう
* 移動行で行内差異を強調表示してしまっていたのを修正

### 2011/06/27 2.12.4+-jp-23, 2.13.20+-jp-3

* [プロジェクトファイルを開く時の脆弱性](http://www.zeroscience.mk/mk/vulnerabilities/ZSL-2011-4997.php)を修正

### 2011/05/23 2.12.4+-jp-22

* 2.12.4+-jp-22 32bit Zip版のMergeLang.dll が古いバージョンになっていました。ごめんなさい。

### 2011/05/23 2.13.20+-jp-2

* 印刷時よけいな描画がされてしまうことがある問題の修正
* 改行文字が2つ以上描画されてしまうことがある問題の修正

### 2011/05/23 2.12.4+-jp-22

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウからパッチを生成するとパッチ内のファイル日付が不正になることがある

### 2011/05/17 2.13.20+-jp-1

* ご連絡いただいた以下の問題の修正
    * ファイル比較ウインドウでテンキーの+と-の入力が効かない。
* 行内差異の表示を1行単位でなく、差異ブロック単位で計算して表示するようにした。
* [表示]メニュー→[垂直分割]にチェックを入れると縦に分割して表示するようにした。
* エンコードエラー時、文字コード選択、プラグイン選択、HEX表示の選択ができるようにした。

### 2011/04/11 2.13.13+-jp-12

* ご連絡いただいた以下の問題の修正
    * フィルタファイル内のコメントマークがない行が無視されてしまう。
    * フィルタファイル内がすべてファイルフィルタ行だった場合、フォルダが全てフィルタされてしまう。

### 2011/03/14 2.12.4+-jp-21, 2.13.13+-jp-11

* ご連絡いただいた以下の問題の修正
    * UTF-8のファイルを誤認することがある

### 2011/02/28 2.13.13+-jp-10

* ご連絡いただいた以下の問題の修正
    * 64bit版のWinMergeでヘルプメニューをクリックすると異常終了することがある
* 四つ以上のファイルまたはフォルダを指定すると異常終了する問題の修正

### 2011/02/14 2.12.4+-jp-20, 2.13.13+-jp-9

* ご連絡いただいた以下の問題の修正(だいぶ遅くなってごめんなさい)
    * マニュアルでコマンドラインオプションの/wmの説明が/wrの説明になっていた
    * フォルダ比較でプラグインが使用されないことがある
* 7-zipバージョン9.20対応プラグイン

### 2011/02/14 2.13.13+-jp-9

* ご連絡いただいた以下の問題の修正(だいぶ遅くなってごめんなさい)
    * フィルタファイルが正しいフォルダに格納されていなかった
    * 比較方法を変更して再比較しても新しい比較方法で比較されない

### 2010/11/15 2.12.4+-jp-19, 2.13.13+-jp-8

* ご連絡いただいた以下の問題の修正
    * フォルダ比較でサロゲートペア文字がファイル名に含まれていると比較されない
    * もうひとつUTF-8のファイルが御認識する件をご連絡いただいているのですが再現できないのですよね...
* 別アプリケーションで更新したファイルを開いているWinMergeを最小化状態から復元すると異常終了する問題の修正

### 2010/10/12 2.13.13+-jp-7

* ご連絡いただいた以下の問題の修正
    * 外部エディタ等で変更されたファイルを再読み込みした時、カーソル位置がファイルの先頭に戻ってしまう。

### 2010/09/06 2.12.4+-jp-18, 2.13.13+-jp-6

* ご連絡いただいた以下の問題の修正
    * Visual Studio .net 2003のVCランタイムファイルがインストールされていないとインストール時にShellExtensionの登録に失敗する
* 一応[DLLハイジャック脆弱性](https://www.microsoft.com/japan/technet/security/advisory/2269637.mspx)の対策をしてみた。(XP SP1以上で効果あり)
* 無効になっているメニュー項目のアイコンが表示されない問題の修正

### 2010/07/27 2.12.4+-jp-17, 2.13.13+-jp-5

* ご連絡いただいた以下の問題の修正
    * 2.12.4+-jp-14からBOM付きのファイルを開くと、BOM付の内容に更にBOMを付加したファイルとして読み込まれてしまう

### 2010/07/13 2.12.4+-jp-16, 2.13.13+-jp-4

* ご連絡いただいた以下の問題の修正
    * WindowsXP上で実行するとメニューの幅が非常に小さく表示されるようになった
* WindowsXP上で実行するとメニューのアイコンが表示されない問題の仮対策

### 2010/07/11 2.12.4+-jp-15, 2.13.13+-jp-3

* Visual Studio 2010でビルドするようにした。
    						Visual Studio 2010でビルドしたバイナリは、WindowsXP以降でしか動作しなくなるため、Windows2000/ME/98の環境では、「(2000/ME/98)」と書いてある方を使用してください。
* ヘルプの日本語化更新

### 2010/07/05 2.13.13+-jp-2

* ご連絡いただいた以下の問題の修正
    * 32bit版インストーラが 7-Zip 4.65用プラグインをインストールしない
    * 前バージョンのフォルダ比較時のステータスバーに未翻訳メッセージが表示される問題の修正が不完全だった
    * ツールバーアイコンのツールチップ説明に"Ctrl-"と"Ctrl+"が混在

### 2010/06/30 2.13.13+-jp-1

* 2.13.13に更新
* 「コメントの差異を無視する」機能の改善(サイタマンさんにご協力いただきました)

### 2010/06/30 2.12.4+-jp-14, 2.13.13+-jp-1

* ご連絡いただいた以下の問題の修正
    * [オプション]ダイアログで.iniファイルをインポートしたときに、[一般]カテゴリの項目が更新されない
    * カスタムコードページに65001(UTF-8)を指定した場合、バイナリ比較で異常終了することがある
    * バックアップファイル名に追加されるタイムスタンプが分かりにくい
* 7-Zip 4.65 用プラグインの追加
* フォルダ比較時のステータスバーに未翻訳メッセージが表示される問題の修正

### 2010/04/19 2.12.4+-jp-13, 2.13.11+-jp-8

* ご連絡いただいた以下の問題の修正
    * Windowsコントロールパネルの「日付と時刻」の設定がフォルダウインドウのファイル日付表示に反映されない
* http://bitbucket.org/winmerge/winmerge/overview にソースを置いてみた

### 2010/04/08

* 7-Zipのリンク切れ?を修正

### 2010/04/05 2.13.11+-jp-7

* F5キーでフォルダを再比較したとき、ツリーノードの展開状態を覚えておくようにした。
* [設定]ダイアログ→[比較→フォルダ]カテゴリに「自動的にサブフォルダを展開する」チェックボックスを追加。このチェックボックスがチェックされている場合、ツリー表示であれば、フォルダ比較完了後全てのサブフォルダが展開状態になる。

### 2010/03/22 2.12.4+-jp-12, 2.13.11+-jp-6

* ご連絡いただいた以下の問題の修正
    * Windows98/ME上でコピー＆ペーストをすると語尾に不正なデータが追加されてしまう
    * Windows98/ME上でLocation Paneをクリックすると異常終了することがある
    * Windows98/ME上でファイル比較を行うと「テンポラリファイルが作成できません…」というエラーが発生する
    * フォルダ内にフォルダが1つしかなくフォルダ名が異なる場合に無理やりマッチさせて比較する機能が正しく動作していなかった
* ANSI版WinMerge.exeの「ファイルまたはフォルダの選択」ダイアログで、パスのコンボボックスリストにアイコンが表示されなかった問題の修正
* 行内に差異ブロックが1つしかない場合、F4キーで選択するブロックの範囲が正しくなかった問題の修正

### 2010/03/05

* ご連絡いただいた以下の問題の修正
    * ExcelToTextプラグインのZIPファイルに旧バージョンと新バージョンが混在していた。

### 2010/02/27 2.12.4+-jp-11, 2.13.11+-jp-5

* ご連絡いただいた以下の問題の修正
    * ANSIビルド版(WinMerge.exe)で文字単位の行内差異表示をする場合に２バイト文字が文字化けすることがある。

### 2010/02/19 2.13.11+-jp-4

* マージ後、比較結果が更新されなくなっていたのを修正。
* 行内に差異が多い場合に動作が遅くなってしまっていたのを対策。

### 2010/02/14 2.12.4+-jp-10, 2.13.11+-jp-3

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウで右クリックすると異常終了することがある。

### 2010/02/11 2.13.11+-jp-2

* 2.13.11+-jp-1で空白の比較設定を「すべて無視する」にすると異常終了してしまうようになってしまったのを修正。

### 2010/02/10 2.13.11+-jp-1

* ご連絡いただいた以下の問題の修正
    * WordドキュメントやExcelブックのファイル名にfilename.xls.r3227の様なバージョン管理ソフトがつけてしまった拡張子があっても、WinMerge付属のプラグインでは認識できるようにしてみた。
* 行内比較のアルゴリズムがちゃんとしたものではなかったので改善してみた。

### 2009/12/21 2.12.4+-jp-9, 2.13.8+-jp-3

* ご連絡いただいた以下の問題の修正
    * コンフリクトファイルを保存するときに、「変更されたファイルをほぞんしますか?」ダイアログで表示されるパスが一時ファイルのものになっていた。(表示のみの問題)
    * 読取専用ファイルに名前を付けて保存すると異常終了する。
    * オートインデントが機能していない。

### 2009/11/16 2.12.4+-jp-8, 2.13.8+-jp-2

* 前バージョンの修正は、Vistaでしか動かなかったみたいです。ごめんなさい。

### 2009/11/09 2.12.4+-jp-7, 2.13.9+-jp-1

* ご連絡いただいた以下の問題の修正
    * WinMerge[U].exeと同じにフォルダにWinMerge.regファイルがあれば、そのファイルを起動時と終了時に読み書きする偽ポータブル機能で、空白を含むパスにWinMerge.regがあると正しく動作しない。
    * WinMergeのレジストリキーが存在しないと、WinMerge.regファイルから正しく読み込めない。

### 2009/10/18 2.12.4+-jp-6, 2.13.8+-jp-7

* ご連絡いただいた以下の問題の修正
    * Diffコンテキストが[全て]以外のとき、セレクションマージン(行番号)をクリックすると異常終了することがある。
    * 3pane表示時に「左(右)にコピーして次に進む」を行っても、次の差異に移動しないことがある。
    * プロジェクトファイルを保存するとき、パスを編集して相対パス指定にしたにも関わらず、絶対パスに変換されてしまう。
* 最大化をしたとき等に異常終了することがあった問題の修正。

### 2009/09/15 2.13.8+-jp-6

* 2.13.8+-jp-5のUnicodeビルド版のEXEが更新されていなかったのを修正

### 2009/09/14 2.13.8+-jp-5

* ご連絡いただいた以下の問題の修正
    * タブなどの表示位置がずれることがある。
* フォルダ比較ウインドウで2つの項目を選択したとき、最初の左側項目と二番目の左側項目等、非水平的に比較ができるようにしてみた。

### 2009/09/14 2.12.4+-jp-4, 2.13.8+-jp-5

* ご連絡いただいた以下の問題の修正
    * Diffペインやロケーションペインを非表示にしたにもかかわらず、複数タブを開くと表示されてしまう。

### 2009/08/19 2.12.4+-jp-3, 2.13.8+-jp-4

* ご連絡いただいた以下の問題の修正
    * 片方にだけ存在するフォルダがフィルタリングされないことがある

### 2009/08/17 2.12.4+-jp-2, 2.13.8+-jp-3

* ご連絡いただいた以下の問題の修正
    * 左右両方のエディタペインの表示上の行数が異なる場合、ロケーションペインをクリックすると「無効な引数が発生しました。」というメッセージが表示されるか、異常終了してしまう。


### 2009/07/13 2.13.8+-jp-2

* ご連絡いただいた以下の問題の修正
    * Unicode (UTF16) のファイルを比較するとランタイムエラーになる
* マージモードに入る時、メッセージボックスを表示するようにした
* 3-way比較で左から中央へマージする機能をAlt+4に、右から中央へマージをAlt+6キーに割り付けた

### 2009/07/13 2.12.4+-jp-1, 2.13.8+-jp-2

* ヘルプの日本語化開始(3/21完了)[tacahiroy](http://github.com/tacahiroy/)さんにご協力いただいています。
* "100%1"のような"%1"を含むフォルダを比較すると無限ループすることがある問題の修正
* 行折り返ししない場合に、ウインドウ幅よりも長い行の後方で文字の削除などを行うと、行の先頭にスクロールしてしまいカレットが見えなくなってしまうことがある問題の修正

### 2009/06/01 2.13.8+-jp-1

* 行内差異表示で削除された単語の位置が分かるようにしてみた

### 2009/06/01 2.12.2+-jp-5

* ご連絡いただいた以下の問題の修正
    * 正規表現の置換がうまく動作しないことがある
    * ANSI版WinMergeのフォルダ比較で特定の文字を含むファイル名を正しく比較できない
* F4キーによる行内差異のローテーション表示が正しく動作しない問題の修正

### 2009/05/08 2.12.2+-jp-4

* ご連絡いただいた以下の問題の修正
    * ファイルフィルタに##を含むパターンが定義された場合、WinMergeが起動しなくなる
* 2.12.2+-jp-3の修正でファイルフィルタの一部が正しく動作しない可能性がある問題の修正
* 試しにLinux上のWine経由でWinMergeを動作させてみたら結構動いて面白かったけど二回目の比較で落ちてしまうようなので修正

### 2009/04/21 2.12.2+-jp-3

* ご連絡いただいた以下の問題の修正
    * 比較するファイルのフルパスがUTF-8に変換して200バイト以上の場合、プラグインの自動展開が機能しない

### 2009/04/20 2.12.2+-jp-2

* ご連絡いただいた以下の問題の修正
    * ANSI版WinMergeのフォルダ比較で特定の文字を含むファイル名を正しく比較できない
* ファイル比較ウインドウを表示後、左右のファイルが両方とも更新された場合に一方のファイルしかリロードできない問題の修正
* x64版でUTF-8のファイルを読み込んだ時、UTF-8としては不正な文字が含まれているとその文字以上読みこまない問題の修正

### 2009/04/03 2.12.2+-jp-1

* ご連絡いただいた以下の問題の修正
    * コンフリクトファイルを開くと最終行の改行が消えていしまう

### 2009/03/19 2.12.0+-jp-3

* ご連絡いただいた以下の問題の修正
    * ANSI版WinMerge(WinMerge.exe)で「着」等、0x85を含むファイル名のファイルが比較されない

### 2009/03/12 2.12.0+-jp-2

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウの拡張子列ヘッダをクリックしても拡張子でソートされない

### 2009/03/09 2.12.0+-jp-1

* 2.12.0に更新
* (22:52)zip版がダウンロードできなかったようです。ごめんなさい。

### 2009/02/23 2.11.2+-jp-1

* 2.11.2に更新
    * ご連絡いただいたご要望の実装(ご要望に完全には応えられていないような気がしますが...)
    * Explorer上でファイルやフォルダをマウスの右ボタンで別フォルダにドラッグしたとき、コンテキストメニューにWinMergeのメニューが表示されるようにした。  
      上記メニューを選択すると、ドラッグしたものがファイルであれば、別フォルダ内の同名ファイル、フォルダであれば別フォルダと比較されます。

### 2009/01/26 2.10.4+-jp-1, 2.11.1.8+-jp-1

* 2.10.4, 2.11.1.8に更新
* ご連絡いただいた以下の問題の修正
    * インストール時にシェルエクステンションの設定がクリアされてしまう問題の修正
    * [設定]ダイアログの参照ボタンを押すと、直前の変更が元に戻ってしまう問題の修正
* 最終行をマージ後Undoできないことがある問題の修正
* mlang.dllを使用した文字コード判定を初回インストール時のデフォルトとした

### 2008/12/03 2.10.2+-jp-2, 2.11.1.7+-jp-2

* ご連絡いただいた以下の問題の修正
    * ANSIビルド版(WinMerge.exe)でEUC-JPのファイルを修正して保存するとShiftJISに変化してしまう問題の修正

### 2008/11/26 2.11.1.7+-jp-1

* 2.11.1.7に更新
* ご連絡いただいた以下のご要望の実装
    * ツリー表示モードの時、Explorerと同様にテンキーの`*`, `+`, `-`による展開/折りたたみ操作ができるようにした。
* ESCキーが利かなくなるのでロケーションビューにフォーカスが移らないようにしてみた。

### 2008/11/26 2.10.2+-jp-1

* 2.10.2に更新
* 実際の最終行の後に挿入されている削除行(灰色の行)にテキストを貼り付け後、UndoしてもUndoできないことがある問題の修正

### 2008/11/04 2.11.1.6+-jp-2

* 200MBぐらいのファイルでも比較しようとするとメモリ使用量が32bitアプリケーションの限界に達してしまうようなので、x64版を作成してみた。

* x64版ではVB6で作られたDLLのような32bitDLLのプラグインは動作しません。x64版では、ExcelやWord用にVBScriptのプラグインをインストールします。
* 7-zipバージョン4.57のみ対応しています。既に32bit版の7-Zipがインストールされている場合は、7-Zipをアンインストールしてから、x64版の7-Zipをインストールした後、x64版のWinMergeをインストールしてください。
* フォルダ比較中に途中の比較状況もリストビューに表示されるようにしてみた。また、フォルダ比較中でもフォルダビューからファイルが開けるようにするためdiffエンジンをスレッドセーフにした。

### 2008/10/27 2.11.1.6+-jp-1

* 2.11.1.6に更新
* 実際の最終行の後に挿入されている削除行(灰色の行)にテキストを貼り付け後、UndoしてもUndoできないことがある問題の修正

### 2008/09/23 2.11.1.4+-jp-3

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ウインドウからファイルを表示後、修正＆保存しても、同一・差異状態の変化がフォルダ比較ウインドウに反映されない

### 2008/09/23 2.10+-jp-2

* ご連絡いただいた以下の問題の修正
    * インストール時に「QuickLaunchアイコンを作成する」にチェックをしてもQuickLaunchアイコンが作成されない
    * 初回起動時、メニューなどが全部英語。自分で言語を選択する必要がある
    * アンインストールしても、レジストリの内容が残る
* その他インストーラでTortoiseSVNとの統合や、シェルエクステンションの指定も反映されなくなっていた問題の修正

### 2008/09/22 2.10+-jp-1

* ご連絡いただいた以下の問題の修正
    * 拡張子のないファイルのバックアップファイル名がFileName..bakのように余計なピリオドが付加されてしまう問題の修正
* パスに&を含んでいるとプロジェクトファイルの保存に失敗する問題の修正。
* 正規表現でケースを無視しない検索に失敗する問題の修正。
* ファイル比較ウインドウからでも[展開プラグインで開く]メニューが使えるようにした。

### 2008/09/15 2.10RC+-jp-1, 2.11.1.4+-jp-2

* ご連絡いただいた以下の問題の修正
    * プライベートファイルフィルタのフォルダ位置をグローバルファイルフィルタのフォルダと同じにしたとき、フィルタリングが正しく動作しないことがある問題の修正
* 3-wayフォルダ比較した後、一時ファイルが残ってしまうことがある問題の修正
* ANSIビルド版WinMergeで翻訳されないメッセージボックスがあったのを修正

### 2008/09/01 2.8.6+-jp-2

* ご連絡いただいた以下の問題の修正
    * [マージ]メニューの[右にコピーして進む]と[左にコピーして進む]メニュー項目の意味が逆転していた

### 2008/08/25 2.9.10+-jp-1

* 2.9.10に更新
* フォルダのツリー表示をtrunkからバックポート
* ツリーモードのとき、BSキーで親フォルダへ移動するようにしてみた。

### 2008/08/25 2.11.1.4+-jp-1

* 2.11.1.4に更新
* ツリーモードのとき、BSキーで親フォルダへ移動するようにしてみた。
* インストーラがアップロードされていなかったのでアップロードした(21:50)。ご連絡ありがとうございました。

### 2008/08/13 2.11.1.3+-jp-3

* ご連絡いただいた以下の問題の修正
    * 付属DLLがデバッグ版ランタイムライブラリ(msvcr71d.dll)を参照していたため、VS.net2003がインストールされていないとWinMergeが起動しない問題の修正

### 2008/08/12 2.11.1.3+-jp-2

* フォルダ比較で片方しかないサブフォルダを含んでいる場合、比較が途中で中断されてしまうことがある問題の修正
* ソースのファイルサイズが大きくなりすぎてまともにダウンロードできなくなってしまったので圧縮の形式をZipから7zに変えてファイルサイズを削減してみた

### 2008/08/11 2.11.1.3+-jp-1

* 2.11.1.3に更新
* 比較方法を「更新日付・サイズ」にして比較後、フォルダビューからファイルを開くとUTF-8等のファイルが文字化けする問題の修正。

### 2008/08/11 2.8.6+-jp-1

* 2.8.6に更新
* 比較方法を「更新日付・サイズ」にして比較後、フォルダビューからファイルを開くとUTF-8等のファイルが文字化けする問題の修正。

### 2008/07/28 2.11.1.2+-jp-1

* フォルダビューのツリー表示でフォルダ内に差異があるかどうか表示するようにした
* フォルダビューのツリー表示でフォルダのダブルクリック、Enterキーを押したときにフォルダの展開または折りたたみされるようにした。

### 2008/07/22 2.11.1.1+-jp-2

* フォルダビューのツリー表示で非表示にしている項目があるとすべてのファイルが表示されないことがある問題の修正
* 片方しかないファイルを削除するとクラッシュすることがある問題の修正
* フォルダ比較結果レポートの生成でクラッシュする問題の修正

### 2008/07/22 2.8.4.+-jp-2, 2.11.1.1+-jp-2

* ご連絡いただいた以下の問題の修正
    * フォルダ比較ビューでファイルの時刻が00:00:00のとき、時刻が表示されない問題の修正

### 2008/07/16 2.11.1.1+-jp-1

* 2.11.1.1に更新
* サブフォルダまで比較している場合、フォルダを階層的に表示できるようにしてみた。この機能を使用するには[表示]メニューの[ツリー表示]にチェックを入れてください

### 2008/06/30 2.9.1.4+-jp-1

* 2.9.1.4に更新
* ラインフィルタを有効にしているとUndo,Redoで落ちてしまうことがある問題の修正
* ロケーションペインの一部が黒くなってしまうことがある問題の修正
* F4キーの行内差異選択ローテーション機能が動作しなくなっていた問題の修正

### 2008/06/30 2.8.4+-jp-1

* 2.8.4に更新
* ラインフィルタを有効にしているとUndo,Redoで落ちてしまうことがある問題の修正

### 2008/06/16 2.9.1.3+-jp-1

* 2.9.1.3に更新
* ロケーションペインでドラッグして比較ビューをスクロールさせた時、チラつかないようにしてみた
* 差異が沢山あるファイルで行フィルタを使用した場合、非常に遅くなるのを若干改善

### 2008/06/16 2.8.2+-jp-1

* 2.8.2に更新
* シングルインスタンスモードのときTortoiseSVN等から起動後、WinMergeのショートカットから起動するとクラッシュする問題の修正

### 2008/05/11 2.8+-jp-2

* ご連絡いただいた以下の問題の修正
    * フォルダビューから片方しか存在しないファイルを開いた後、両方とも存在するファイルを開いたとき、タイトルが「無題」になってしまう問題の修正

### 2008/04/21 2.8+-jp-1

* フォルダ比較の[選択範囲を最新に更新]を実行したとき、落ちてしまうことがある問題の修正
* 行折り返しモードで、行がすごく長いとき、PageUp, PageDownキーでスクロールしないことがある問題の修正
* 行折り返しモードを若干高速化

### 2008/04/16 2.8RC+-jp-4

* 改造しすぎた...
* 数千個レベルの差異をマージするのがすごく遅くなってしまっていたので高速化
* 紛失行(灰色になっている行)の1行上の行を削除すると紛失行が普通の行になってしまう問題の修正
* 行折り返し状態でフォントサイズを変更した場合、ロケーションペインに行数の変更が反映されない問題の修正
* [設定]→[エディタ]カテゴリ→[自動的に再スキャンする]が無効になっているときに、行の削除や挿入操作を行うとロケーションペインの表示が非常に怪しくなるのでいっそのこと表示しないようにした。
* Undoバッファの上限が1024となっており、かなり少なかったので100倍にしてみた。なんでこんな制限をしているのだろう?

### 2008/04/07 2.8RC+-jp-3

* 差異行のみを表示しているときに選択範囲をコピーまたは、削除したとき表示している行のみが対象になるようにしてみた。
* フォルダビューの表示で片一方しか存在しないファイルの表示順番が同一ファイルと差異のあるファイルの間に表示されるようにしてみた。

### 2008/03/23 2.8RC+-jp-2

* RCなのに1文字づつ入力するとUndoできなくなっていた問題の修正
* ペインのスワップをすると、Undoができなくなる問題の修正

### 2008/03/17 2.6.14+-jp-1, 2.8RC+-jp-1

* ご連絡いただいた以下の問題の修正
    * フォルダビューでファイルを削除した後にフォーカスがフォルダビューに戻らない問題の修正

### 2008/03/17 2.8RC+-jp-1

* 2.8RCに更新
* 印刷するときに本文の部分がクリッピングされなくなっていた問題の修正
* 「開く」ダイアログのフィルタテキストボックス等にごみデータが表示されることがある問題の修正
* パッチの生成で異常終了する問題の修正
* マージ後UndoでNULL文字が挿入されてしまうことがある問題の修正

### 2008/03/03 2.7.7.6+-jp-1

* 2.7.7.6に更新
* コンフリクトファイルの文字コードを検出するようにした
* VB6からテキストをコピー＆ペーストしたときテキスト後ろにごみが追加されてしまう問題の修正
* プラグインで開くと文字化けすることがある問題の修正

### 2008/02/25 2.7.7.5+-jp-1

* 2.7.7.5に更新

### 2008/02/18 2.7.7.4+-jp-1

* 2.7.7.4に更新
* フォルダ比較でサイズが大きいファイルがフォルダに含まれていると比較方法がずっとクイックコンテンツに変わってしまう問題の修正
* 比較方法がクイックコンテンツのとき、改行コードの違いを無視してくれないことがある問題の修正

### 2008/01/26 2.7.7.3+-jp-1

* 2.7.7.3に更新
* VC7でビルドしているのにShellExtension[U].dllがVC8のライブラリにリンクされてたりとかおかしなことになっていたのを修正
* 文字幅が少し広めになってしまったのを修正
* DLLの再配置を防ぐためlibexpat.dll等のベースアドレスを変更
* NT4.0で起動できなくなっていたのを修正

### 2008/01/22 2.7.7.2+-jp-1

* 2.7.7.2に更新

### 2008/01/08 2.7.7.1+-jp-1

* 2.7.7.1に更新
* 行フィルタを使用するとWinMergeが異常終了することがある問題の修正
* Vistaのシンボリックリンクファイルを開いてもなにも表示されない問題の修正
* ファイルまたはフォルダの選択ダイアログを開くと異常終了することがあったが原因がわからなかったため作りを変えてみた
* レジストリ`HKEY_CURRENT_USER`直下にThingamahoochieフォルダが作られてしまう問題の修正
* インストーラで表示されるTortoiseCVS、TortoiseSVNとの統合コンボボックスが表示されないことがある問題の修正
* ファイルの再読み込みを実装

### 2007/12/10 2.7.6+-jp-1

* 2.7.6に更新
* 右上から左下方向の矩形選択で異常終了することがある問題の修正

### 2007/11/18 2.7.5.6+-jp-1

* 2.7.5.6に更新
* 行を折り返さない場合に、差異行付近のみ表示する機能がおかしくなっていたので修正

### 2007/10/31 2.7.5.3+-jp-2

* クリップボードからの貼り付けがおかしくなってしまったので修正
* 「類似行をマッチさせる」オプション動作の改善の試み

### 2007/10/28 2.7.5.3+-jp-1

* 矩形選択を実装してみた。他のエディタの様にAltキーを押しながらマウスで選択すると矩形選択になります。キーボードのみで操作する場合は、Ctrl+Bを押してからShift+矢印キーで選択か、Shift+矢印キーで選択してからCtrl+Bを押してください。
* 今の改行文字の表示は日本人にはあまりなじみがないので矢印っぽい表示に変えてみた。グラフィックを使わず文字だけで表現したかったのですが、CRLFの表示はかなり強引になってしまった...
* 文字コードがお互いに異なるファイルを比較すると%TEMP%ディレクトリに一時ファイルが残ってしまう問題の修正
* PageUp, PageDownキーを押したときの動作を改善
* Pluginが対応していないバージョンの7-zipがインストールされていると、「アーカイブサポートが無効」ダイアログ地獄になる問題の修正
* OSがNT系の場合、WinMerge.exeはもはやインストールされなくなったようです

### 2007/10/03 2.6.12+-jp-1

* 2.6.12に更新
* ANSI版(WinMerge.exe)のオプションウインドウでコードページを65001(UTF-8)に指定してもUTF-8としてファイルが開けない問題の修正
* [ジャンプ]ウインドウから指定した行へ移動するときに異常終了することがある問題の修正

### 2007/09/10 2.7.5.1+-jp-3

* ご連絡いただいた以下の問題の修正
    * 2つのバイナリファイルを強制的にテキストファイルとして比較しなかった場合、「～は、バイナリファイルです。バイナリファイルとテキストファイルを比較できません。」と表示される問題

### 2007/09/04 2.7.5.1+-jp-2

* ご連絡いただいた以下の問題の修正
    * 設定情報をエクスポートするとハングアップする問題
    * 訳語の統一
* [ファイル]→[ファイルエンコーディング]メニューからコードページを指定してファイルを読み直せるようにしてみた。

### 2007/08/20 2.7.5.1+-jp-1

* ロケーションペインでゴミが残ることがある問題の修正
* パッチ生成で改行コードの違いを無視するオプションを追加
* ファイル読み込みの微妙な高速化

### 2007/08/06 2.7.4+-jp-2

* ロケーションペインのデザインをちょっとだけ変えてみた。

### 2007/07/01 2.6.8+-jp-1

* 2.6.8に更新
* 削除行を含んだ行番号付きコピーがなにかおかしいのを修正

### 2007/07/01 2.7.4+-jp-1

* 2.7.4に更新
* 更に少しだけHTML出力サイズを削減...
* 削除行を含んだ行番号付きコピーがなにかおかしいのを修正
* 試しにアーカイブファイルとディレクトリを比較できるようにしてみた

### 2007/06/18 2.7.3.7+-jp-1

* 2.7.3.7に更新
* スペースでインデントしていて場合にファイルの比較結果をHTMLに出力するとインデントが反映されない問題の修正
* HTMLでの折り返しが少しでもましになるようにIEでしか使えないword-breakプロパティを使用
* 少しだけHTML出力サイズを削減。6000行近くあるファイルをHTMLに出力してFirefoxで開くと200Mメモリを使ってしまうけどもっと効率のよいHTMLにすればなんとかなるのかしら...

### 2007/06/11 2.7.3.6+-jp-1

* mlang.dllによるエンコーディング判定を有効して標準のExcelプラグイン等を使用すると文字化けすることがある問題の修正
* ファイル比較結果のHTML出力機能を追加。([ツール(T)]→[レポートの生成(R)...]) できるだけ、画面表示の表示と同じイメージでHTMLに出力するようにしています。(行番号とか、Diffコンテキストとか)

### 2007/06/04 2.7.3.5+-jp-2

* ご連絡いただいた以下の問題の修正
    * ファイル比較ウインドウのフォントがフォルダ比較ウインドウのフォントになってしまう問題の修正
* フォルダ比較ウインドウで片方にしか存在しない項目のコピーができない問題の修正

### 2007/06/04 2.7.3.5+-jp-1

* 行折り返しモードの時の行数が多いファイルでのカーソル移動の高速化
* 普通にファイル比較結果を印刷するとすごい勢いで紙が消費されてしまうので、差異行とその付近だけ表示するモードを作ってみた。([表示]→[Diffコンテキスト]メニュー) 検索などで非表示の行にカーソルがいくとカーソルが迷子になってしまうけどこれはどうしたものか...

### 2007/05/20 2.6.6+-jp-2, 2.7.3.4+-jp-1

* 本家2.7.3.3以上のShellExtensionをインストールした後、日本語版のShellExtensionをインストールするとデスクトップの背景を右クリックしたとき等にExplorerがShellExtensionで落ちてしまう問題が発生したためShellExtensionを修正
* Diffペインで中ボタンを押しながらトラックポイントを動かすと落ちてしまう問題の修正(マウスホイールでもおきると思う。VC6でコンパイルすると起きないのはなぜかしら...)
* タブバーのタブを閉じたときにあるタブのキャプション表示が別のタブと同じになってしまうことがある問題の修正
* 空白の変更を無視する比較方法で行内差異が正しく表示されないことがある問題の修正
* 本家: 壊れていた DisplayBinaryFiles プラグインの修正

### 2007/05/06 2.7.3.3+-jp-2

* ツールバーの親ウインドウをRebarにし、ツールバーにグラデーションがかかるようにしてみた。(XPのテーマが有効になっている場合)
* 「ファイルまたはフォルダの選択」ウインドウのコンボボックスをアイコン付きにしてみた。
* DocBook形式のソースからHTMLHelpを作るためのXSLTプロセッサをsaxonからxsltprocに変更

### 2007/05/06 2.6.6+-jp-1, 2.7.3.3+-jp-2

* ご連絡いただいた以下の問題の修正
    * 拡張子が.nsi, .issのファイルを開くとクラッシュすることがある問題の修正
* 「行折り返し」に変更した後、カーソルを上下に移動すると、行がずれて描画されることがある問題の修正
* テーマを有効にしているXP上で、フォルダ比較ウインドウのリストビューヘッダーの一部がテーマ通りに描画されない問題の修正
* Inno Setup を最新(5.1.12)に更新してインストーラを作成(たぶんVistaでよくなっているはず)
* ShellExtensionのバージョンが更新されたのでインストーラ実行後、再起動するか聞いてくると思います。  
    まったくもってお勧めしないが、どうしても再起動したくない人向けのインストール方法(2000/XP系)
    1.  WinMergeのインストーラを実行して、最初の画面のままにしておく
    2.  ファイラー等のShellExtensionを使っていそうなプロセスを終了させておく。
    3.  タスクマネージャを起動
    4.  [プロセス]タブでExplorer.exeを右クリックし、[プロセスの終了]を選択→Explorer(デスクトップ)が死ぬ。
    5.  WinMergeのインストールを続行
    6.  Ctrl+Shift+Escキーでタスクマネージャを表示し、[ファイル]→[新しいタスクの実行]でExplorer.exeを実行→デスクトップ復活

### 2007/04/09 2.7.3.3+-jp-1

* 2.7.3.3に更新
* BOM付きUTF-8のファイルとSJISのファイルを比較したとき一行目に差異がなくても差異があるように表示される問題の修正
* ファイルに1文字でもNUL文字が入っているとバイナリファイルとみなしてしまってがっくりしてしまうので、強制的にテキストファイルとして開けるようにしてみた。このとき、NUL文字はスペースに置換され、ファイルはReadonlyになります。あまりにバイナリすぎるファイルを開くとひどい目にあいます...
* [ファイルまたはフォルダの選択]ダイアログで存在しないネットワークパスを指定すると数十秒間フリーズしてしまうのでフリーズしないようにしてみた。ただし、そのようなパスを指定した場合、WinMergeを終了してもが数十秒間プロセスが残り続ける場合があります...
* アイコンが変になっていたので修正
* MFCの日本語リソースDLL(mfc71jpn.dll)を含んでいなかったので追加
* 3フォルダ比較でバイナリファイルもテキストファイルと表示していた問題の修正
* ファイルを開くときに真っ黒なウインドウが表示されてびっくりすることがあるので、その場合は白くウインドウを塗りつぶすようにした。
* [ファイルまたはフォルダの選択]ダイアログでフィルタにワイルドカードを指定できるが、拡張子パターン(`*.c`, `*.h`)しか指定できないので、もう少し複雑なパターン(`abc??d*.c`等)も指定できるようにした。

### 2007/04/02 2.7.3.2+-jp-1
* 2.7.3.2に更新
* ご連絡いただいた以下の問題の修正
    * プリンタがインストールされていない場合、印刷プレビュー実行後、ファイルビューのフォントが変化してしまう問題の修正
    * 「開く」ダイアログの[フィルタ]で"`*.h`"等の拡張子フィルタを指定した場合、前回のフィルタの内容も反映されてしまう問題の修正
    * [オプション]→[片方しか存在しないフォルダ内もスキャンする]をチェックしてフォルダ比較したとき、一方にしか存在しない空フォルダを表示するようにした
* MFCのランタイムライブラリを更新

### 2007/03/26 2.7.3.1+-jp-1

* 2.7.3.1に更新
* 最後のページが印刷できない問題の修正。

### 2007/03/20 2.7.2+-jp-1

* 2.7.2に更新
* 印刷機能を若干改善。
    * ファイル比較ビューで行番号を表示していれば、行番号を印刷するようにした
    * ファイル比較ビューで行折り返しにしていれば、行を折り返して印刷するようにした

### 2007/02/26 2.7.1.7+-jp-1

* 2.7.1.7に更新
* フォルダビューから選択したファイルをクリップボードにコピーできるようにしてみた(エクスプローラ等に貼り付けできます)

### 2007/02/26 2.6.4+-jp-5, 2.7.1.7+-jp-1

* ご連絡いただいた以下の問題の修正
    * ファイル比較ビューでタイトルに表示されているパスが/で区切られている場合にファイル名のクリップボードへのコピーが正しく動作しない問題の修正
    * フォルダビューで一つ上に上がる項目を非表示にしようとするとWinMergeが異常終了する問題の修正

### 2007/02/14 2.6.4+-jp-4, 2.7.1.6+-jp-3

* 2.6.4+-jp-3, 2.7.1.6+-jp-2で改行のみ行のマージ動作がおかしくなってしまったのを修正orz

### 2007/02/12 2.6.4+-jp-3, 2.7.1.6+-jp-2

* ご連絡いただいた以下の問題の修正
    * フォルダビューの読み取り専用メニューが正しく動作しない問題の修正
    * 改行コードがLFの行をマージするとCRが付加されたり、逆にLFの行にCR+LFの行をマージしてもLFのままである問題の修正
* コマンド引数に4つ以上のファイル名またはフォルダ名を指定すると異常終了する問題の修正
* 行折り返しと[自動的に最初の差異にスクロールする]を選択している場合、ファイルを開いたときに差異行までちゃんとスクロールしていないことがある問題の修正

### 2007/02/05 2.7.1.6+-jp-1

* 他のアプリケーションによるファイル更新をチェックするタイミングを比較時ではなく、他のエディタのようにWinMergeがアクティブになった時やタブを変更した時にしてみた
* 行フィルタの正規表現に一致していても日本語が含まれる行に対しては行フィルタが正しく適用されない問題の修正
* シフトJIS以外のファイルでも行フィルタが動作するようにしてみた

### 2007/02/05 2.6.4+-jp-2, 2.7.1.6+-jp-1

* [設定]→[比較]→[片方しか存在しないフォルダ内もスキャンする]を追加。チェックをはずすことで2.6.2+-jp-2以前の動作に戻せるようにしてみた
* 片方しか存在しないファイルのファイル名を変更した後すぐに再び別名に変更すると親フォルダがリネームされてしまう問題の修正

### 2007/01/29 2.7.1.5+-jp-3

* 行内の隣接している単語単位差異が連結されてしまうのを改善してみた
* ステータスバーのコードページの隣にコードページ名を表示してみた
* バックアップフォルダを指定した場合のバックアップファイル名命名規則を変更(フルパスのようなファイル名になります)

### 2007/01/29 2.6.4+-jp-1, 2.7.1.5+-jp-3

* ご連絡いただいた以下の問題の修正
    * ANSIビルド版(WinMerge.exe)でDiffペインの行内差異が正しく表示されない問題の修正
    * [ヘルプ(H)]→[WinMergeについて(A)]で日本語版のバージョンがわからない問題の修正
* ANSIビルド版(WinMerge.exe)でUTF-8やUTF-16のファイルを開くと正しく読込まれているように見えるのに「エンコーディングエラー」と表示されることがある問題の修正(※NT系OSの人ならできればUNICODEビルド版を使用してください。本家の中の人もANSIビルド版はまじめにテストしていないので2.8でサポートをきろうかという話もあります)
* サイズが64Kバイト以上のファイルで文字コードに自動認識がたまにうまくいかないことがある問題の修正
* 7-zipをインストールしていてもフォルダビューで圧縮ファイルを開こうとするとバイナリファイルとみなされてしまう問題の修正

### 2007/01/24 2.7.1.5+-jp-2

* ご連絡いただいた以下の問題の修正
    * バージョン2.7.1.\*で レジストリ保存位置が`HKEY_CURRENT_USER`直下になってしまった問題の修正。DefaultSyntaxColors,Font,FontDirCompare,Merge7z,Settingsができています... orz

### 2007/01/14 2.6.2+-jp-4

* プラグインの自動展開が動作しなくなっていました。すみませんです。orz  
    (まさか、本家のファイルフィルタの変更がプラグインに影響するとは...)

### 2007/01/14 2.7.1.5+-jp-1

* 実験的にBOMなしのUCS-2ファイルも扱えるようにしてみた。(mlang.dllを使用する場合)

### 2007/01/14 2.6.2+-jp-3

* ご連絡いただいた以下の問題の修正
    * ANSI版(WinMerge.exe)でパスが260バイトを超えるファイルを比較できない問題の修正(Explorerやcmd.exeで扱えるパス長はワイド文字260文字ぐらいのようなのでそれにあわせてANSI版のみ`_MAX_PATH`マクロを強引に`260*2`へ変更)
    * フォルダビューにファイルがない状態でプロジェクトの保存をするとWinMergeが異常終了する問題の修正
    * 日本語パスを含んでいるとプロジェクトファイルの読込/保存が正しく行われない問題の修正(日本語版失格です...)
* 2.7.1.4の修正を取り込み
* タブをスペースにする指定をしていた場合、Enterキーを押すと異常終了することがある問題の修正
* 3方向フォルダ比較でメモリリークする問題の修正
* 3方向ファイル比較で特殊な差異への移動でうまくいかないことがあるところを修正

### 2007/01/04 2.7.1.4+-jp-1

* コンフリクトに泣きそうになりながらSVNトランクとマージ
* [サブフォルダを含む]をチェックしてフォルダ比較したとき、片方にしかないフォルダ内のファイルも表示するようにしてみた。(今までフォルダ表示のみだった)
* 2.7.1.\*で行折り返しを有効にすると、ロケーションペインの表示がかなり遅くなってしまっていたので若干の高速化
* Excelプラグイン等を使用して開くとファイル比較ウインドウが少しの間真っ黒になるのを若干改善。(完全ではない)

### 2006/12/23 2.6.2+-jp-2

* ご連絡いただいた以下の問題の修正

    * [パッチ生成]からのhtmlの差分生成で`<table>`の幅指定がおかしかった問題の修正
    * F6キー等でマージエディタのペイン変更後、キーボードで範囲選択すると予期しない範囲となる問題の修正
    * 「ファイルを走査しています」という和訳がなんか変なので修正
    * UTF-16のファイルを含むフォルダを比較するとUTF-16のファイルをバイナリとみなしてしまう問題の修正
* Excelプラグインを使用しているとフォルダ比較で片方にしか存在しないExcelファイルが存在していると"NUL.xlsが開けません"云々というエラーが表示される問題の修正
* Excelプラグインを使用していてもフォルダビューから片方にしか存在しないExcelファイルを開くとバイナリとみなされる問題の修正
* フォルダビューでファイル名の変更に失敗するとファイル名が表示されなくなる問題の修正
* 旧安定版は別サイトに移動

### 2006/12/17 2.6.2+-jp-1

* ご連絡いただいた以下の問題の修正
    * コマンド引数-dl/-dr等で指定するタイトルが長すぎると落ちてしまう問題の修正
    * ディレクトリ比較画面で項目「差異数」が表示されない問題の修正
    * 2.6+-jp-3で直したコピー先指定のフォルダコピーが失敗する問題はまだ直しきれていないところがあったので修正
* タブのタイトルが長くなりすぎないように比較する名前が一致していれば[name x 2]と表示するようにした
* いまさらながら初期インストール後のあまりの表示のだささに驚愕したので初期パラメータを微調整。色は...まあいいや
* StampVer.exeがないとソースのビルドに失敗しているように見えるのでプロジェクトファイルからStampVer.exeを実行しているところを削除

### 2006/11/27 2.6+-jp-3

* 2.6+jp-2でつけたタブはやっぱりだめだったので修正。
* ファイルの日付とサイズによる比較がだめだめだったので修正
* NT4.0上でフォルダ比較ウインドウのアイコン表示がだめだめだったので修正
* ファイルコピー中にWinMergeを閉じられると落ちたり、プロセスが残りっぱなしになる問題の修正
* ShellExtenstionのアイコンがなんか欠けているので修正
* ご連絡いただいた2つの問題のうちコピー先指定のフォルダコピーが失敗する問題の修正。もう一つのXMLファイルがバイナリファイルとみなされる問題は再現できてません。困った...

### 2006/11/21 2.6+-jp-2

* かなりやっつけ気味なMDIウインドウ切替用のタブをつけてみた。
* 3ペイン表示の時、自分に便利なように 左と真ん中に差異がある行(ALT+1)等特殊な差異への移動用ショートカットキーとメニューを追加。
* 複数ウインドウを開くと異常なぐらいCPU負荷が増える問題の修正
* 3ペイン表示をしたとき、TEMPディレクトリに一時ファイルが残ってしまう問題の修正
* 外部エディタをMIFESにしたとき行番号指定起動がうまくいかない問題の修正
* 外部エディタの指定でコマンド行を小文字に変換してしまっていたのを修正

### 2006/10/16 2.6+-jp-1

* 本家で2.6がリリースされたのでこちらも更新。まだ未実装な部分が多い3方向比較機能が入っているけど2.4よりはバグフィックスされている気がするのでこれをリリース版としてみる...
* ファイル差分のHTML出力でハングアップしてしまう問題の修正
* [プラグイン(P)]→[スクリプト(S)]メニューでスクリプトファイルがあるのに「空」と表示される問題の修正
* 「類似行をマッチさせる」にチェックをいれると、行フィルタが無視されてしまう問題の修正
* 「置換」ウインドウのコンボボックス履歴がソートされてしまっているのでソートしないようにした
* Ctrl+UとCtrl+Shift+Uキーに選択範囲の小文字化、大文字化を割付
* 3つのフォルダ比較でクイックコンテンツや日付、サイズによる比較を実装
* 行数が多い差分を他のペインにコピーするのがすごく遅いので若干高速化。
* フォルダビューアイコンの24bitカラー化
* ファイルオープン時の微妙な高速化...

### 2006/09/19 2.5.6.0+-jp-1

* 2.5.6に更新。
* 編集メニューを開くときやCtrl+C等のキーボードショートカットを実行するとき遅くなるので[編集]→[スクリプト]メニューを[プラグイン]へ移動。

### 2006/08/13 2.5.5.6+-jp-2

* ANSI版(WinMerge.exe)で行の最後の差異ブロックに移動すると異常終了することがある問題の修正。
* [設定(O)]→[比較]→[類似行をマッチさせる(M)]をチェックすると、比較時に非常にメモリを使用してしまうので改善してみた。
* 編集行マークがUndoで消えないことがある問題の修正

### 2006/08/10 2.5.5.6+-jp-1

* ANSI版(WinMerge.exe)で2バイト文字含む行を水平スクロールすると文字化けが発生する問題の修正。
* 編集した行がわかるようにした。

### 2006/07/29 2.5.5.3+-jp-2(ソースのみ)

* Visual Studio 2005 でコンパイルできるようにした。

### 2006/07/17 2.5.5.3+-jp-1

* 本家で放置されていた2つのパッチを取り込んでみた。
* 1つ目は、差異ブロック内の類似行が同じ行になるように調整するパッチ。[設定(O)]→[比較]→[類似行をマッチさせる(M)]のチェックをはずすとこの機能が無効になります。
* 2つ目は、フォルダビューに色付けするパッチ。ちょっとどぎついかも
* ファイルビューで編集した結果がフォルダビューに反映されない問題の修正
* [開く]ダイアログを開くときかくかくするのを直してみた。

### 2006/07/02 2.5.5.1+-jp-1

* 外部エディタでファイルを開くとき、行番号($linenum)とファイル名($file)を指定できるようにした。
* [オプション]→[システム]→[外部エディタ]の指定例) `C:\Program Files\vim\vim70\gvim.exe +$linenum $file`
* 3ディレクトリ比較機能の実装をすこしだけ進めた。
* 開くダイアログから直接バイナリファイルを比較したとき、内容が違っていても同一と表示されてしまう問題の修正(ディレクトリ比較では問題ない)
* 2006/07/02 21:00: インストーラなし版の.langファイルが更新されていなかったので差し替え
* 2006/07/03 22:30: インストーラ版がなぜか消えていたので再上げ。orz

### 2006/05/08 2.5.3.7+-jp-1

* 3つのファイルを比較するとき、ファイルの先頭行に差異があると異常終了することがある問題の修正。
* 起動がちょっとだけ速くなるようにした。そのかわり、[編集]メニューと[プラグイン]メニューの初回の表示が遅くなっています。
* まだかなり荒削りなViewCVSぽいファイル比較結果HTML出力機能を追加。パッチ生成メニューからどうぞ。
* 害がありすぎるので WatchBeginningOfLog.dll, WatchEndOfLog.dllプラグインを削除。拡張子が.logのファイルを比較したときファイルの全てが表示されない場合はこのプラグインのせいです。

### 2006/04/09 2.5.3.5+-jp-1

* 本家にあわせてコンパイラをVC6からVC.net2003に変更
* フォルダ比較で比較するファイルの文字コードが互いに違っていたらUTF-8に変換して比較するようにした。
* WinMergeU.exe, WinMerge.exeが格納されているフォルダにWinMerge.regファイルがあれば、設定情報としてそれを優先的に読み書きするようにした。(USBメモリでの持ち運び用 ※レジストリには書き込んでしまいます。)

### 2006/02/23 2.5.3.2-jp-1

* BOM付きではないUTF-8のファイルもたまに識別できるようにしてみた(mlang.dllを使用する場合)
* プロジェクトファイルが開けない問題の修正
* エディタの置換で[全て置換]の動作がおかしかった問題の修正
* レジストリ[HCU\Software\Thingamahoochie\WinMerge]に変なごみデータができてしまう問題の修正

### 2005/12/11 2.5.0.3-jp-1

* 行番号を表示できるようにしてみた。
* ブックマークを使えるようにした。
* 半角の'ｰ'が全角の幅で表示されてしまっていたのを修正
* 単語単位の検索が変だったので修正

### 2005/11/28 2.5.0.2-jp-1

* もともとあったWinMerge組み込みエディタの行折り返し機能を使えるようにしてみた。ただし、行折り返しをすると、一行がすごく長かったり、行数が多いファイルを扱うとすごく遅くなるので注意
* ペインの入れ替えをできるようにしてみた
* Windows XP上でUnicode版のWinMergeを使用する場合、なぜかフォントをCourierNewにしても日本語が表示できてしまうのだけれども、文字幅が変になっていたので多少改善してみた

### 2005/11/08 2.4-jp-4

* フルソースの拡張子がzipなのに中身は7z形式になっていたのであげなおし...orz
* ソース差分にruby.cppが抜けていた o...rz

### 2005/11/07 2.4-jp-4

* 日本語版のビルドでトラブルが多そうなのでフルソースもアップロードしてみた

### 2005/11/07 2.4-jp-4

* 2.4-jp-4のソース差分ファイルが壊れていたのであげなおし

### 2005/11/06 2.4-jp-4

* コマンド引数 /e を指定しても、ESCキーでWinMergeが終了しない問題の修正

### 2005/10/31 2.4-jp-3

* フォルダ比較結果ウインドウから片方しかないファイルを開くと以下の条件でエラーが発生する問題の修正

* 最終行が改行コードを含んでいないファイル
* [設定(O)]メニュー→[比較]→[空白]→[比較する(C)]を選択した場合
* フォルダ比較結果ウインドウをESCキーかCtrl+Wで閉じた後にファイル比較ウインドウを操作するとエラーが発生する問題の修正
* IgnoreCommentsC.dll等のpredifferがうまく動かなくなっていたのを修正

### 2005/10/15 2.4-jp-2

* [マージ(M)]メニューをクリックするとフリーズする問題の修正
* フォルダ比較結果ウインドウからファイルを開くと、ファイル名ではなく[左/右]無題と表示されることがある問題の修正
* 3ペイン実験版を実行した後にファイルを開くと異常終了することがある問題の修正
* ウインドウを[Ctrl+W]で閉じられるようにしてみた。

### 2005/10/02 2.4-jp-1

* 本家2.4がリリースされたので更新
* フィルタを設定してもすべてのファイルが比較されてしまう問題の修正
* Windowsの[画面のプロパティ]→[デザイン]で配色を変更してWinMergeを再起動しても設定が反映されない問題の修正
* Ansiビルド版のWinMerge.exeでEUC-JPのファイルを表示できない問題の修正
* 新規プライベートファイルフィルタ作成がうまくできない問題の修正

### 2005/09/10 2.3.6.0-jp-2

* EUC-JPのファイルを比較したときに差異が表示されない問題の修正
* ※上記の不具合の連絡をメールでくれた方ありがとうございます。メールアドレスが無効のようでしたので返信できませんでした。
* EUC-JPのファイルのロードに時間がかかるようになってしまっていたのを改善
* EUC-JPのファイルを誤認識してのコードページ932で表示したときにハングアップすることがある問題の修正(原因がよくわかっていないので根本的な修正ではない)
* Unicodeファイルなのにコードページを932と表示してしまう問題の修正

### 2005/09/14

* Excelからテキストへの変換プラグインのライセンスを明示(GPL)
* シンタックスハイライトでキーワードでない単語も色が変わってしまう2.3.1.2-jp-1からの不具合を修正

### 2005/03/27 2.3.1.6-jp-4

* ディレクトリ比較方法を「更新日付」にした場合にディレクトリ比較ビューから開いたファイルが化けて表示されてしまう問題の修正
* ディレクトリ比較方法が「クイックコンテンツ」で「改行文字の違いを無視する」にした場合にディレクトリ比較が終わらないことがある問題の修正
* ディレクトリ比較方法の「更新日付」と「クイックコンテンツ」の意味が逆転していたのを修正
* VBScriptで作成したプラグインに文法の誤りがあった場合に表示されるエラーメッセージボックスが文字化けしている問題の修正

### 2005/03/26 2.3.1.6-jp-3

* Excelブック内のVBAコードを比較したくなったので、[Excelからテキストへの変換プラグイン](ExcelToText.sct.zip)を作ってみた。C++で作るのは難しそうだったのでVBScriptで作ってみたが、今のWinMergeでは、VBScriptで作ったUNPACK/PACK形式のプラグインをうまく処理できないようなので、処理できるようにWinMergeを改造してみた。(Wordからテキストの展開プラグインは[UK-Taniyamaさん](http://homepage3.nifty.com/UK-taniyama/)が作っていますのでそちらをどうぞ)
* 色つき行内差異の表示がうまくいかないことがあったので修正。
* Alt+Up/Downで差異行に移動したあとすぐにDelキーを押すと以前カーソルがあったところの文字が削除されてしまうバグの修正

### 2005/03/14 2.3.1.6-jp-2

* バックアップファイル保存先指定機能が動作しなくなっていた...
* ステータスラインにファイルのコードページを表示するようにした。
* パッチ生成で結果格納ファイルを指定しなかったらTEMPディレクトリに一時ファイルを作成してそれに出力するようにした。

### 2005/03/13 2.3.1.6-jp-1

* バージョン 2.3.1.6に同期

### 2005/02/21 2.3.1.3-jp-2

* 検索でクラッシュすることがある問題の修正
* ファイル比較で文字コードが違っていたらUTF-8に変換して比較するようにした。(ディレクトリ比較は未対応)

### 2005/02/18 2.3.1.3-jp-1

* 差異のある行内の差異のある部分を単語単位で色付けするようにしてみた。
* 「ファイルまたはフォルダの選択」ダイアログのパスを指定するコンボボックスでオートコンプリートがきくようにした。

### 2005/01/23 2.3.1.2-jp-1

* 2.3.1.1-jp-1で埋め込んでしまった、ロケーションペインをアクティブにしてファイルを閉じると二度とファイルが開けなくなる悲惨なバグの修正。
* シンタックスハイライトを高速化。とくにバッチファイルのものが遅かったのを改善。
* 「自動的に再スキャンする」にチェックを入れた場合にDelキーで文字を削除するとBSキーとは違い即時再スキャンしていたのを遅延再スキャンするように変更。

### 2005/01/10 2.3.1.1-jp-1

* WinCVSやTortoiseCVS等からWinMergeを連続して沢山起動するとたまに異常終了することがある問題の修正
* 1行スクロールを少し早くしてみた。
* Shift+F3で逆方向検索ができるようにした。
* 前回アクティブだったペインを記録し、次回に再現するようにした。
* マージを行ったあと、F3を押下すると再び検索ダイアログがでてしまうのを直してみた。
* バックアップファイルの保存先を指定できるようにした。

### 2004/11/28 2.2-jp-1

* 2.2-jp-1のインストーラなし版を用意

### 2004/11/14 2.2-jp-1

* 本家で2.2がリリースされたので更新
* カーソル移動が遅い理由がわかったので修正。(カーソル移動する度に全行再描画していた...)
* ディレクトリ比較結果ビューでファイルの削除をDelキーでできるようにした。

### 2004/10/03 2.2RC1-jp-1

* 前バージョンで入れた文字コードの自動判定機能がかなり文字コードを誤認識するのでやり方を変えてみた。

### 2004/09/07 2.1.7.13-jp-1

* mlang.dllを使った文字コードの自動判定機能を入れてみた。なんとか機能しているっぽい。
* 文字コードの自動判定を有効にするには[編集]メニュー→[設定]メニュー→[コードページ]タブで指定してください。
* ただ、ディレクトリスキャンがすごく遅くなるので通常は使用しないほうがいいかも。

### 2004/07/19 2.1.7.9-jp-1

* ファイルを表示するときカクカクするので、ちょっと直してみた。 (うまいやり方が見つからなかったのでかなり強引なやり方になってしまった。ChildFrm.cpp、DirFrame.cppのあたり)
* 不必要な再描画がたくさんおこるので、おこらないようccrystaltextview.cppのある一行をコメントにしてみた。 (軽くなったけど、なにか不具合が起きるかも)
* ついでに2.1.7.9に更新。

### 2004/05/16 2.1.7.2-jp-1

* Unicode文字の文字幅を計算するところで恥ずかしいミスをしてたので修正。
* Unicodeビルド版で単語選択がうまくいかないことがある問題の修正。
* ついでに2.1.7.2に更新。

### 2004/04/01 2.1.5.16-jp-1

* Unicodeビルド版でもそれなりに日本語表示ができるようになったような気がするのと、スプラッシュ画面が かっこよくなったので更新。
* WinMergeのインストーラは、本家に合わせて9x系OSの場合にノーマルビルド版(WinMerge.exe)、NT系OSの場合に Unicodeビルド版(WinMergeU.exe)をインストールするようになりました。 Unicode版は実行ファイル名がWinMergeU.exeになっていることに注意してください。
* Unicodeビルド版はちょっと動作を速くしてみましたが、それでもまだ若干ノーマルビルド版にくらべて遅いようなので 不評ならばインストーラの動作を変えてみるかもしれません。

### 2004/03/14 2.1.5.15-jp-1

* まだ、開発版だけれどもWinMerge2.1.5.15の日本語版をアップロード。
* 2.1.xxになって追加された圧縮機能(要7-Zipインストール)とDiffペイン表示が便利。
* BOMがついてればUnicodeファイルも扱える。
* 2.0.2ではUndo/Redoで異常終了することがあったけど2.1.xxで直っているので、これで困っていた人は 乗り換えてみるのもいいかも。

### 2004/02/28 2.0.3-jp-4

* ソースコードの圧縮ファイルの中身がインストーラになっていたので上げ直し。ソースが必要だった人はごめんなさい。

### 2004/02/08 2.0.3-jp-4

* 検索・置換でマルチバイト文字を考慮していなかったので修正
* (正規表現のマルチバイト文字対応は、なんとなくうまくいってそうだけど自信なし)

### 2004/02/04 2.0.3-jp-3

* 2/1版で修正した問題が完全に直しきれてなかったので修正。

### 2004/02/01 2.0.3-jp-2

* 行全てが可視領域に入らない場合に日本語が正しく表示されないことがある問題の修正。
* ダブルクリックで正しく単語を選択できない問題の修正。
