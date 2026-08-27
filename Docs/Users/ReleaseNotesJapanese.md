# WinMerge 2.16.58.2 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.58.2 の更新内容](#what-is-new-in-216582)
- [2.16.58 の更新内容](#what-is-new-in-21658)
- [2.16.57 beta の更新内容](#what-is-new-in-21657-beta)
- [既知の問題](#known-issues)

2026年8月

## このリリースについて

WinMerge の 2.16.58.2 安定版リリースです。  
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は https://github.com/WinMerge/winmerge/issues で報告してください。  
日本語での報告は、https://sourceforge.net/p/winmerge-v2-jp/tickets/ でお願いします。

## 2.16.58.2 の更新内容

### 外観

* 不具合修正: 高 DPI 時のツールバーアイコン間隔が狭すぎる問題を修正した。

### ファイル比較

* 不具合修正: 表示行フィルタ適用時、単語単位の差異表示が正しく行われないことがある問題を修正した。([#3535](https://github.com/WinMerge/winmerge/issues/3535))

* 不具合修正: 単語選択後のShift+Ctrl+左/右の選択ができないことがある問題を修正した。([#3521](https://github.com/WinMerge/winmerge/issues/3521))

* 表示行フィルタ適用時の表示速度を改善した。([PR #3517](https://github.com/WinMerge/winmerge/pull/3517))

### フォルダー比較

* 不具合修正: 比較中にソートしても安全な列であれば比較中にソートできるようにした。([#3579](https://github.com/WinMerge/winmerge/issues/3579))([PR #3581](https://github.com/WinMerge/winmerge/pull/3581))

### フィルター式

* 不具合修正: `none`と`+` での文字列連結で結果が`none`にならないようにした。([#3550](https://github.com/WinMerge/winmerge/issues/3550))

### アーカイブ生成

* 不具合修正: 片方にしかないファイルを含められるように修正した。

### プラグイン

* 不具合修正: `BUFFER_PACK_UNPACK` プラグインの出力で最後のバイトが失われるオフバイワンバグを修正した。

### 翻訳

* 翻訳の更新:

  * Brazilian (PR #3508)
  * Chinese Simplified (PR #3493)
  * Chinese Traditional (PR #3505)
  * Hungarian (PR #3502)
  * Polish (PR #3501)
  * Russian (PR #3494)
  * Turkish (PR #3506)

### マニュアル

* 不具合修正: スペイン語の"Filters" ページの文法エラーを修正した。

## 2.16.58 の更新内容

### ファイル比較

* 不具合修正: ファイルが一定のしきい値を超えて外部から変更された場合にクラッシュ (Access Violation) する問題を修正した。([#3456](https://github.com/WinMerge/winmerge/issues/3456))
  ([PR #3457](https://github.com/WinMerge/winmerge/pull/3457))

* 不具合修正: 3方向マージモードで変更をコピーした後、ペインの一部が黒い背景に黒い文字で表示されることがある問題を修正した。([#3468](https://github.com/WinMerge/winmerge/issues/3468), [#3469](https://github.com/WinMerge/winmerge/issues/3469))

### フォルダー比較

* 不具合修正: アーカイブとフォルダーの比較で、誤った比較元が選択される問題を修正した。([#3449](https://github.com/WinMerge/winmerge/issues/3449))
  ([PR #3458](https://github.com/WinMerge/winmerge/pull/3458))

* 不具合修正: イメージリスト初期化時の HICON リソースリークを修正した。

### ファイルまたはフォルダーの選択ダイアログ

* 不具合修正: 共通ファイルダイアログの作成時に発生した例外を適切に処理するようにした。([#3462](https://github.com/WinMerge/winmerge/issues/3462))
  ([PR #3464](https://github.com/WinMerge/winmerge/pull/3464))

* 不具合修正: 3方向比較で MRU (最近使用した項目) が正しく処理されない問題を修正した。([#3452](https://github.com/WinMerge/winmerge/issues/3452))

### ファイル比較レポート

* 複数のファイル比較結果から 1 つの HTML レポートを生成できるようにした。([PR #3450](https://github.com/WinMerge/winmerge/pull/3450))

### パッチ生成

* パッチ生成ダイアログに、チェックボックス付きのファイル一覧を追加した。([PR #3470](https://github.com/WinMerge/winmerge/pull/3470))

### アーカイブ生成

* 比較結果をアーカイブとして作成できるようにした。([PR #3483](https://github.com/WinMerge/winmerge/pull/3483))

### コマンドライン

* シングルインスタンスグループ用の `/g` コマンドラインオプションを追加した。([PR #3472](https://github.com/WinMerge/winmerge/pull/3472))

### 翻訳

* 翻訳の更新:

  * Brazilian (PR #3459, PR #3476, PR #3489)
  * Chinese Simplified (PR #3460, PR #3479)
  * French (PR #3478, PR #3491)
  * German (PR #3480, PR #3486)
  * Italian (PR #3455, PR #3473, PR #3477, PR #3488)
  * Japanese
  * Korean (PR #3447, PR #3481, PR #3487)
  * Lithuanian (PR #3461, PR #3471, PR #3492)
  * Polish (PR #3463, PR #3490)
  * Turkish (PR #3465, PR #3474)
  * Russian (PR #3448, PR #3484)

## 2.16.57 Beta の更新内容

### 全般

* 不具合修正: ファイルマッピングに失敗した場合に、誤ってクラッシュとして扱われることがある問題を修正した。([#3412](https://github.com/WinMerge/winmerge/issues/3412))

* クラッシュログのスタックトレースにモジュール相対オフセットを追加した。

### ファイル比較

* 不具合修正: 報告されたマージ操作時のクラッシュを回避する修正をした。（未再現）([#3402](https://github.com/WinMerge/winmerge/issues/3402))

* 不具合修正: 編集後にステータスバーの行番号・列番号が正しく表示されないことがある問題を修正した。

* 不具合修正: 同期ポイント設置後、別ファイルをドラッグして再比較すると、左右の表示位置がずれることがある問題を修正した。

* 不具合修正: ペイン内のすべての行を削除した際に、空のバッファへアクセスしてアサーションに失敗する問題を修正した。

* ファイル比較ウインドウにも表示フィルターを追加した。(Ctrl+Shift+Lで表示できます) [(PR #3374)](https://github.com/WinMerge/winmerge/pull/3374)

* Tree-sitter の統合により、複数のプログラミング言語に対するシンタックスハイライトを改善した。([PR #3306](https://github.com/WinMerge/winmerge/pull/3306), [PR #3337](https://github.com/WinMerge/winmerge/pull/3337), [PR #3338](https://github.com/WinMerge/winmerge/pull/3338), [PR #3350](https://github.com/WinMerge/winmerge/pull/3350), [PR #3415](https://github.com/WinMerge/winmerge/pull/3415), [PR #3427](https://github.com/WinMerge/winmerge/pull/3427), [PR #3440](https://github.com/WinMerge/winmerge/pull/3440))

* ISyntaxParser インターフェースを導入し、シンタックス解析処理をリファクタリングした。([PR #3415](https://github.com/WinMerge/winmerge/pull/3415))

### フォルダー比較

* 不具合修正: ファイル名変更中に[マージ]→[削除]メニューを実行するとクラッシュすることがある問題を修正した。([#3411](https://github.com/WinMerge/winmerge/issues/3411))

* 不具合修正: ZIP エクスポート時に、サブフォルダー内の変更されていないファイルまで含まれてしまう問題を修正した。([#3444](https://github.com/WinMerge/winmerge/issues/3444))
  ([PR #3445](https://github.com/WinMerge/winmerge/pull/3445))

* EvalContext を導入し、フィルター評価処理をリファクタリングしてコードの保守性を向上した。([PR #3353](https://github.com/WinMerge/winmerge/pull/3353))

### アーカイブサポート

* 不具合修正: RAR4形式ファイルのファイル比較時に不要なエラーメッセージボックスが表示される問題を修正した。([#3392](https://github.com/WinMerge/winmerge/issues/3392))

* 7-Zip 26.02 に更新した。

### ファイルまたはフォルダーの選択ダイアログ

* 参照ボタンのドロップダウンメニューでクリップボード履歴を選択できるようにした。[(PR #3352)](https://github.com/WinMerge/winmerge/pull/3352)

### プラグイン

* clip:// URLハンドラーを追加した。[(PR #3352)](https://github.com/WinMerge/winmerge/pull/3352)

### プロジェクトファイル

* プラグイン引数を含む他所から提供されたプロジェクトファイルを開く際、外部コマンドが実行される可能性があるため、警告メッセージを表示するようにした。([#3396](https://github.com/WinMerge/winmerge/issues/3396))
 ([PR #3397](https://github.com/WinMerge/winmerge/issues/3397))

### 翻訳

* 翻訳の更新:

  * Brazilian (PR #3431)
  * Chinese Simplified (PR #3429, PR #3438)
  * Chinese Traditional (PR #3426)
  * Corsican (PR #3420)
  * French (PR #3393, PR #3406, PR #3408, PR #3435)
  * German (PR #3432)
  * Italian (PR #3399, PR #3434, PR #3446)
  * Korean (PR #3422, PR #3433)
  * Lithuanian (PR #3405, PR #3439)
  * Polish (PR #3418, PR #3430)
  * Portuguese (PR #3391, PR #3414)
  * Russian (PR #3395, PR #3428)
  * Spanish (PR #3421, PR #3423, PR #3424, PR #3425)
  * Turkish (PR #3403, PR #3436)

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。([#2685](https://github.com/WinMerge/winmerge/issues/2685))
- フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。([#1391](https://github.com/WinMerge/winmerge/issues/1391))
- 巨大ファイルの比較でクラッシュすることがある。([#325](https://github.com/WinMerge/winmerge/issues/325))
- 大幅に異なるフォルダの比較が非常に時間がかかる。([#322](https://github.com/WinMerge/winmerge/issues/322))
- 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。([#296](https://github.com/WinMerge/winmerge/issues/296))
