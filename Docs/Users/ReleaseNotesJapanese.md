# WinMerge 2.16.48 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.48 の新機能](#what-is-new-in-21648)
- [2.16.47 beta の新機能](#what-is-new-in-21647-beta)
- [既知の問題](#known-issues)

2025年4月

## このリリースについて

WinMerge の 2.16.48 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21648"></a>2.16.48 の新機能

### 全般

- 不具合修正: ツールバーアイコンを「特大」に設定すると、設定を保存できなかった問題を修正した。（[#2748](https://github.com/WinMerge/winmerge/issues/2748)）
- オプションダイアログを開くためのキーボードショートカット `Ctrl+,` を追加した。（[#2705](https://github.com/WinMerge/winmerge/issues/2705)）
- Merge.rc を更新した。（[PR #2711](https://github.com/WinMerge/winmerge/pull/2711)）(PRをいただきました。ありがとうございます。)

### ファイル比較

- 不具合修正: 同一のテキストブロックを貼り付けた際に、存在しない行が追加される問題を修正した。（[#2702](https://github.com/WinMerge/winmerge/issues/2702)）
- 不具合修正: 検索ダイアログを開いたまま WinMerge を終了するとクラッシュする問題を修正した。
- Pascal シンタックスハイライト: `initialization` と `finalization` を追加した。（[PR #2719](https://github.com/WinMerge/winmerge/pull/2719)）(PRをいただきました。ありがとうございます。)
- Pascal シンタックスハイライト: 複数行文字列のサポートを追加した。（[PR #2720](https://github.com/WinMerge/winmerge/pull/2720)）(PRをいただきました。ありがとうございます。)

### フォルダー比較

- 不具合修正: 「更新日時とサイズ」で比較する際に、mtime がゼロのファイルを比較できない問題を修正した。（[#2714](https://github.com/WinMerge/winmerge/issues/2714)）
- 不具合修正: ファイル削除後にクラッシュすることがある問題を修正した。（[#2746](https://github.com/WinMerge/winmerge/issues/2746)）

### Webページ比較

- 不具合修正: タブ文字が含まれると比較が失敗する問題を修正した。
- 不具合修正: 特定の HTML 要素内で行の折り返しが正しく行われない問題を修正した。
- 不具合修正: `<pre>` 要素内の差分が、本来別々の行で表示されるべきところを連結して表示されることがある問題を修正した。

### プラグイン

- 不具合修正: ApacheTika, PlantUML プラグイン: 実行に失敗してもエラーメッセージが表示されない問題を修正した。（[#715](https://github.com/WinMerge/winmerge/issues/715)）
- 不具合修正: ApacheTika プラグイン: ファイル名に英数字以外の文字が含まれていると実行に失敗する問題を修正した。(短いファイル名を使用するようにした。)（[#715](https://github.com/WinMerge/winmerge/issues/715)）
- AIConvertText プラグイン: gpt-4.1、gpt-4.1-mini、gpt-4.1-nano モデルを追加した。

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2706,#2715,#2726)
  - Chinese Simplified (PR #2710,#2730)
  - Corsican (PR #2722)
  - French (PR #2716)
  - Hungarian (PR #2703,#2713,#2724)
  - Italian (PR #2704,#2723,#2737)
  - Japanese
  - Lithuanian (PR #2708)

## <a name="what-is-new-in-21647"></a>2.16.47 Beta の新機能

### 全般

- 不具合修正: `/inifile` コマンドラインオプションに指定したINIファイルがドライブ直下にある場合にそのINIファイルが無視されてしまう問題を修正した。 ([#2635](https://github.com/WinMerge/winmerge/issues/2635))  
- 不具合修正: ウィンドウが非アクティブになるときにも「別のアプリケーションが更新しました」と表示される問題を修正した。 ([#2668](https://github.com/WinMerge/winmerge/issues/2668))  
- タイトルバーのボタンやステータスバーのちらつきを軽減した。
- メニュー、オプションウインドウ等の英語テキストの書き直しを行った。([PR #2682](https://github.com/WinMerge/winmerge/pull/2682))  (PRをいただきました。ありがとうございます。)
- エラー等のログを表示するための出力ペインを追加した。 (PR #2663)

### ファイル比較

- 不具合修正: 置換フィルターの正規表現内の `$` が「改行文字のの違いを無視する」オプション有効時に正しく動作しない問題を修正した。 ([#2640](https://github.com/WinMerge/winmerge/issues/2640))  
- 不具合修正: Python の複数行文字列の構文強調が 1 行を超えると正しく動作しない問題を修正した。 ([#2643](https://github.com/WinMerge/winmerge/issues/2643))  
- 不具合修正: 展開プラグインと比較前処理プラグインを両方使用すると、ステータスバーの `&` がアンダーラインとして表示される問題を修正した。
- 不具合修正: オプションウインドウのコードページセクションのコードページリストとファイル比較ウィンドウでコードページリストが一致していない問題を修正した。 ([#2678](https://github.com/WinMerge/winmerge/issues/2678))  
- C 言語の構文強調のキーワードリストを更新した。 ([PR #2669](https://github.com/WinMerge/winmerge/pull/2669))  (PRをいただきました。ありがとうございます。)

### 画像比較

- オプションウインドウの[比較/画像]セクションのパターンに.jxl 拡張子を追加した。(jxlファイルを開くには、Windows に JPEG XL Image Extension がインストールされている必要があります。) ([PR #2682](https://github.com/WinMerge/winmerge/pull/2682))(PRをいただきました。ありがとうございます。)

### オプションダイアログ

- 不具合修正: シェル統合オプションで「シェル拡張の登録を解除」ボタンをクリックした際に 32bit版の`ShellExtensionU.dll` が正しく登録解除されない問題を修正した。 ([#2419](https://github.com/WinMerge/winmerge/issues/2419))  
- 不具合修正: オプションウインドウの[比較/画像]セクションのデフォルトボタンを押してもすべてリセットされない問題を修正した。([PR #2655](https://github.com/WinMerge/winmerge/pull/2655))  (PRをいただきました。ありがとうございます。)

### カラースキーム

- VS Dark カラースキームを追加した。 ([PR #2634](https://github.com/WinMerge/winmerge/pull/2634))  (PRをいただきました。ありがとうございます。)
- Twilight カラースキームを追加した。 ([PR #1430](https://github.com/WinMerge/winmerge/pull/1430))  (PRをいただきました。ありがとうございます。)

### インストーラー

- 不具合修正: Windows 10 x64 で管理者権限なしのユーザーがインストールするとコンテキストメニューが表示されない問題を修正した。 ([#2638](https://github.com/WinMerge/winmerge/issues/2638)) ([PR #2639](https://github.com/WinMerge/winmerge/pull/2639))  

### マニュアル

- ヘルプページ → 付録 A. ショートカットキーを更新した。 ([#2659](https://github.com/WinMerge/winmerge/issues/2659))  

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2675,#2688,#2697)
  - Chinese Simplified (PR #2700) 
  - Corsican (PR #2632,#2676)
  - Hebrew (PR #2673)
  - Italian (PR #2689,#2689)
  - Japanese
  - Polish (PR #2671)
  - Portuguese (PR #2650,#2695)
  - Swedish (PR #2679)
  - Turkish (PR #2636)

### その他

- 不具合修正: VS2022 17.13.0 でのビルドエラーを修正した。 ([PR #2645](https://github.com/WinMerge/winmerge/pull/2645))  (PRをいただきました。ありがとうございます。)
- 不具合修正: `zopflipng` を使用して `splash.png` のサイズを削減した。 ([PR #2646](https://github.com/WinMerge/winmerge/pull/2646))  (PRをいただきました。ありがとうございます。)
- `README` を更新した。([PR #2696](https://github.com/WinMerge/winmerge/pull/2696))  (PRをいただきました。ありがとうございます。)

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。（[#2685](https://github.com/WinMerge/winmerge/issues/2685)）
 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
