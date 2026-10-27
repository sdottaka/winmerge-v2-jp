# WinMerge 2.16.60 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.60 の更新内容](#what-is-new-in-21660)
- [2.16.59 Beta の更新内容](#what-is-new-in-21659-beta)
- [既知の問題](#known-issues)

2026年10月

## このリリースについて

WinMerge の 2.16.60 安定版リリースです。  
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は https://github.com/WinMerge/winmerge/issues で報告してください。  
日本語での報告は、https://sourceforge.net/p/winmerge-v2-jp/tickets/ でお願いします。

## 2.16.60 の更新内容

### 全般

* 最近比較したファイルまたはフォルダーの履歴はWindowsの設定が無効にされていた場合に独自に保持するようにした。([PR #3663](https://github.com/WinMerge/winmerge/pull/3663))

* darkmodelib を 0.77.1 に更新し、ARM64 に対応した。

### ファイル比較

* 不具合修正: 移動行を含む差異で、行フィルターが適用されない問題を修正した。([#3680](https://github.com/WinMerge/winmerge/issues/3680), [PR #3681](https://github.com/WinMerge/winmerge/pull/3681))

* 不具合修正: 3 方向マージに関する 2 件の問題を修正した。([PR #3671](https://github.com/WinMerge/winmerge/pull/3671))

* 不具合修正: AutoIt の識別子と入れ子になったコメントの構文強調表示を修正した。([PR #3685](https://github.com/WinMerge/winmerge/pull/3685))

* 不具合修正: 出力ペインの高さを変更するとクラッシュする問題を修正した。([#3733](https://github.com/WinMerge/winmerge/issues/3733))

* RTF の構文強調表示に対応した。([PR #3686](https://github.com/WinMerge/winmerge/pull/3686))

* 不具合修正: Markdown の見出しの強調表示が正しく行われないことがある問題を修正した。([PR #3718](https://github.com/WinMerge/winmerge/pull/3718))

* 出力ペインに表示するマージ時のコピー通知を翻訳可能にした。([#2927](https://github.com/WinMerge/winmerge/issues/2927), [PR #3701](https://github.com/WinMerge/winmerge/pull/3701))

### 画像比較

* 不具合修正: 外部 FreeImage プラグインが存在しているとクラッシュするため読み込みを無効にした。([winimerge/#43](https://github.com/WinMerge/winimerge/issues/43))

* 不具合修正: 画像の貼り付けと元に戻す操作を修正した。([winimerge/#41](https://github.com/WinMerge/winimerge/issues/41))

* FreeImage を 3.19.25 に更新した。

* 画像の差異をコピーする際に、コピー先のキャンバスを拡張するようにした。([winimerge/#42](https://github.com/WinMerge/winimerge/issues/42))

### ステータスバー

* 不具合修正: ステータスバーの差異数が正しくない問題を修正した。([#3649](https://github.com/WinMerge/winmerge/issues/3649), [PR #3707](https://github.com/WinMerge/winmerge/pull/3707))

* ステータスバーがちらつくのを修正した。

### ファイルまたはフォルダーの選択ダイアログ

* 最近比較した項目の一覧を折りたたみ可能にした。([PR #3673](https://github.com/WinMerge/winmerge/pull/3673))

* フォルダー比較ビューに、左右それぞれのファイル名、フォルダー名、拡張子の列を追加した。([PR #3682](https://github.com/WinMerge/winmerge/pull/3682))

### フォルダー比較

* フォルダー比較ビューに、左右それぞれのファイル名、フォルダー名、拡張子の列を追加した。([PR #3682](https://github.com/WinMerge/winmerge/pull/3682))

### アーカイブサポート

* 7-Zip を 26.05 に更新した。

### プラグイン

* MiniMax の既定のプリセットを M3.1 Flash にした。([PR #3709](https://github.com/WinMerge/winmerge/pull/3709))

### インストーラー

* 不具合修正: Inno Setup 5 の翻訳を統一し、インドネシア語版インストーラーのパスを修正した。([#3737](https://github.com/WinMerge/winmerge/issues/3737))

### 翻訳

* 翻訳を更新した:

  * Brazilian (PR #3665, PR #3687, PR #3672, PR #3697, PR #3708, PR #3717)
  * Chinese Simplified (PR #3660, PR #3691, PR #3694, PR #3712, PR #3721)
  * Chinese Traditional (PR #3738)
  * Corsican (PR #3676)
  * French (PR #3670, PR #3693, PR #3705, PR #3722)
  * German (PR #3659, PR #3679, PR #3689, PR #3695, PR #3713, PR #3720)
  * Hungarian (PR #3669)
  * Italian (PR #3666, PR #3688, PR #3698, PR #3711, PR #3728)
  * Korean (PR #3703, PR #3704, PR #3734)
  * Lithuanian (PR #3667, PR #3690, PR #3710, PR #3715)
  * Polish (PR #3661, PR #3684, PR #3692, PR #3723, PR #3727, PR #3730, PR #3731, PR #3735)
  * Spanish (PR #3699, PR #3700)
  * Turkish (PR #3719)

### マニュアル

* 未翻訳の ReadMe ファイルを更新し、サポートへのリンクを更新した。([PR #3723](https://github.com/WinMerge/winmerge/pull/3723), [PR #3725](https://github.com/WinMerge/winmerge/pull/3725))

* 翻訳状況スクリプト内の ReadMe テンプレートのパスを修正した。([PR #3724](https://github.com/WinMerge/winmerge/pull/3724))

* Git の更新日と Inno Setup の翻訳状況を表示するようにした。([PR #3739](https://github.com/WinMerge/winmerge/pull/3739))

## 2.16.59 Beta の更新内容

### 全般

* 不具合修正: MDI ウィンドウのコントロール（最小化／最大化／閉じる）が、ホバーするまで完全に隠れる問題を修正した。([#3511](https://github.com/WinMerge/winmerge/issues/3511), [PR #3552](https://github.com/WinMerge/winmerge/pull/3552))

* テキスト、画像、Web ページ、バイナリ比較ウインドウのスプリッターの位置を記憶して復元するオプションを追加した。([ウインドウ]→[スプリッターの位置を保持]メニュー)([PR #3611](https://github.com/WinMerge/winmerge/pull/3611))

### 外観

* 不具合修正: 高 DPI 時のツールバーアイコンの間隔が狭すぎる問題を修正した。

* ツールバーとマージンのアイコンを BMP から PNG に変更した。([PR #3510](https://github.com/WinMerge/winmerge/pull/3510))

* アクティブなウィンドウに応じてツールバーの内容を変えるようにした。([PR #3631](https://github.com/WinMerge/winmerge/pull/3631))

### ファイル比較

* 2 方向の競合および 3 方向マージの確認と解決に使用する「マージ結果」ペインを追加した。([PR #3515](https://github.com/WinMerge/winmerge/pull/3515))

* 不具合修正: Shift+Insert でフィルターバーではなくファイルに貼り付けられる問題を修正した。([#3585](https://github.com/WinMerge/winmerge/issues/3585))

* 不具合修正: 表示フィルターによってできた隙間をまたぐカーソル移動を改善した。([#3601](https://github.com/WinMerge/winmerge/issues/3601), [PR #3622](https://github.com/WinMerge/winmerge/pull/3622))

* 不具合修正: ファイル比較のステータスバーが初期表示されないことがある問題を修正した。([PR #3644](https://github.com/WinMerge/winmerge/pull/3644))

* 不具合修正: 3方向ファイル比較のコンテキストメニューの「右にコピー」のキーボードショートカット表示が正しくないのを修正した。([#3645](https://github.com/WinMerge/winmerge/issues/3645))

* 不具合修正: 3方向ファイル比較でペインを入れ替えた後にアンドゥ操作ができない問題を修正した。([PR #3647](https://github.com/WinMerge/winmerge/pull/3647))

* 不具合修正: テキスト削除に失敗した場合に、元に戻す操作のグループを確定するようにした。

* 不具合修正: 「コメントの違いを無視する」と「空行を無視する」オプションが有効の場合、改行なしの1文字同士の比較で差異があるにもかかわらず一致と表示されてしまう問題を修正した。([PR #3651](https://github.com/WinMerge/winmerge/pull/3651))

* 不具合修正: ファイル末尾に改行がない場合に、無視対象の差異範囲が正しく処理されない問題を修正した。([#3653](https://github.com/WinMerge/winmerge/issues/3653), [PR #3657](https://github.com/WinMerge/winmerge/pull/3657))

* ブックマークを設置したとき、ブックマークアイコンが見えるようにマージンを自動表示するようにした。

* ファイルパスバーのコンテキストメニューに保存コマンドを追加した。([PR #3654](https://github.com/WinMerge/winmerge/pull/3654))

* Tree-sitter の PHP および F# 文法を更新した。([PR #3656](https://github.com/WinMerge/winmerge/pull/3656))

### テーブル比較

* 列範囲フィルターと、比較対象から列を無視する機能を追加した。([PR #3565](https://github.com/WinMerge/winmerge/pull/3565))

### 画像比較

* 画像比較ウインドウのスプリッターの位置を記憶できるようにした。([PR #3593](https://github.com/WinMerge/winmerge/pull/3593))

* 画像比較時の画像読み込みで WIC デコーダーを優先するオプションを追加した。([PR #3537](https://github.com/WinMerge/winmerge/pull/3537))

### フォルダー比較

* 不具合修正: 比較中にソートしても安全な列であれば比較中にソートできるようにした。([#3579](https://github.com/WinMerge/winmerge/issues/3579))([PR #3581](https://github.com/WinMerge/winmerge/pull/3581))

### フィルター式

* プラグインパイプラインにフィルター式を追加した。([PR #3530](https://github.com/WinMerge/winmerge/pull/3530))([PR #3540](https://github.com/WinMerge/winmerge/pull/3540))

* 不具合修正: contains 演算子で大文字小文字のみの違いがある文字列を検索できないことがある問題を修正した。([#3586](https://github.com/WinMerge/winmerge/issues/3586))

### ステータスバー

* マージモードインジケーターをクリック可能にし、幅を縮小した。([PR #3529](https://github.com/WinMerge/winmerge/pull/3529))

### アーカイブサポート

* 不具合修正: ZIPファイル内のフォルダーが比較できない問題を修正した。([#3588](https://github.com/WinMerge/winmerge/issues/3588))

* 不具合修正: 一時的なアーカイブ設定の復元後にアーカイブ形式が誤って判定される問題を修正した。([#3633](https://github.com/WinMerge/winmerge/issues/3633))

* 7-Zip を 26.03 に更新した。([PR #3613](https://github.com/WinMerge/winmerge/pull/3613))

### プラグイン

* 不具合修正: `BUFFER_PACK_UNPACK` プラグインの出力で最後のバイトが失われるオフバイワンバグを修正した。

* 不具合修正: 特殊な UTF-8 文字が正しく比較されない問題を修正した。([#3071](https://github.com/WinMerge/winmerge/issues/3071), [PR #3568](https://github.com/WinMerge/winmerge/pull/3568))

* ステータスバーにプラグイン選択ボタンを追加した。([PR #3518](https://github.com/WinMerge/winmerge/pull/3518))

* メニューからパイプラインにプラグインを追加できるようにした。([PR #3523](https://github.com/WinMerge/winmerge/pull/3523))

* プラグインパイプラインでフィルター式を使用できるようにした。([PR #3540](https://github.com/WinMerge/winmerge/pull/3540))

* AI プラグインに MiniMax プロバイダーのサポートを追加した。([PR #3499](https://github.com/WinMerge/winmerge/pull/3499))

* AI プラグイン: ローカル LLM とOpenAI互換APIサポートを追加([PR #3589](https://github.com/WinMerge/winmerge/pull/3589))

* プラグインパイプラインのフィルター式を検証するようにした。([PR #3578](https://github.com/WinMerge/winmerge/pull/3578))

* SelectLines プラグインに、`-F` オプションによる文字列のリテラル検索を追加した。([#3500](https://github.com/WinMerge/winmerge/issues/3500), [PR #3598](https://github.com/WinMerge/winmerge/pull/3598))

### 翻訳

* アゼルバイジャン語とインドネシア語の翻訳を追加した。([PR #3624](https://github.com/WinMerge/winmerge/pull/3624), [PR #3636](https://github.com/WinMerge/winmerge/pull/3636))

* Brazilian、Chinese Simplified、Chinese Traditional、French、German、Hungarian、Korean、Italian、Lithuanian、Polish、Spanish、Russian、Turkish の翻訳を更新した。

### マニュアル

* 不具合修正: スペイン語のヘルプがフランス語になっている問題を修正した。([#3658](https://github.com/WinMerge/winmerge/issues/3658))

* フランス語、イタリア語、スペイン語のマニュアルにローカライズ設定を追加した。([PR #3617](https://github.com/WinMerge/winmerge/pull/3617))

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。([#2685](https://github.com/WinMerge/winmerge/issues/2685))
- フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。([#1391](https://github.com/WinMerge/winmerge/issues/1391))
- 巨大ファイルの比較でクラッシュすることがある。([#325](https://github.com/WinMerge/winmerge/issues/325))
- 大幅に異なるフォルダの比較が非常に時間がかかる。([#322](https://github.com/WinMerge/winmerge/issues/322))
- 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。([#296](https://github.com/WinMerge/winmerge/issues/296))
