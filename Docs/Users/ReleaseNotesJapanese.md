# WinMerge 2.16.50 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.50 の新機能](#what-is-new-in-21650)
- [2.16.49 beta の新機能](#what-is-new-in-21649-beta)
- [既知の問題](#known-issues)

2025年7月

## このリリースについて

WinMerge の 2.16.50 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21650"></a>2.16.50 の新機能

### 一般

- 最大化状態でタイトルバーの最上端をクリックした場合に、それをタブボタン内のクリックとして扱うようにした。（[PR #2828](https://github.com/WinMerge/winmerge/pull/2828)）(PRをいただきました。ありがとうございます。)

### 翻訳

* 不具合修正: 4つの「Disabled」をそれぞれ別々に翻訳できるようにし、All rights reserved も翻訳可能にした。（[#2852](https://github.com/WinMerge/winmerge/issues/2852)）
* 翻訳の更新:

  * Brazilian (PR #2849)
  * Chinese Simplified (PR #2856)
  * Hungarian (PR #2857,#2859)
  * Italian (PR #2850,#2851,#2858)
  * Japanese
  * Swedish
  * Russian (PR #2847)

## <a name="what-is-new-in-21649-beta"></a>2.16.49 Beta の新機能

### 全般

- Shift+マウスホイールでタブが切り替えられるようにした。（[PR #2821](https://github.com/WinMerge/winmerge/pull/2821)）(PRをいただきました。ありがとうございます。)

### 外観

- テーマ付きサイズグリップを使用し、ツールバーのツールチップをコントロールバーの代わりに使用するようにした。（[PR #2769](https://github.com/WinMerge/winmerge/pull/2769)）(PRをいただきました。ありがとうございます。)

### ファイル比較

- 不具合修正：複数の差異ブロックをコピーする際にクラッシュすることがあるのを修正した。
- シンタックスハイライト: Delphi のコンパイラディレクティブをサポートした。（[#2814](https://github.com/WinMerge/winmerge/issues/2814)）
- ロケーションパネルをクリックしたときに自動的に該当行へ移動するかどうかを切り替えるオプションを追加した。（[PR #2827](https://github.com/WinMerge/winmerge/pull/2827)）(PRをいただきました。ありがとうございます。)

### フォルダー比較

- 不具合修正：存在しないファイルのタイムスタンプが表示される問題（[#2764](https://github.com/WinMerge/winmerge/issues/2764)）
- 不具合修正：ファイルフィルターを使用している場合、フォルダーを選択しての[選択項目を最新に更新]を選択するとフォルダーの比較結果がランダムに失われる問題を修正した。（[#2792](https://github.com/WinMerge/winmerge/issues/2792)）
- フォルダー比較ウィンドウで複数ファイルを一括で比較できる機能を追加した。（[#324](https://github.com/WinMerge/winmerge/issues/324), [PR #2825](https://github.com/WinMerge/winmerge/pull/2825)）(PRをいただきました。ありがとうございます。)
- フィルターシステムの改善：式のサポートとUIの強化。(フィルター式の例:`*.cpp;*.h|fe:Size<10KB` ・・・拡張子cppとhのファイルでファイルサイズが10KBのファイルを比較) （[PR #2802](https://github.com/WinMerge/winmerge/pull/2802)）

### オプションダイアログ

- 不具合修正：比較 > フォルダー ページの「～切替閾値」オプションが正しく有効/無効にならない問題を修正した。（[PR #2819](https://github.com/WinMerge/winmerge/pull/2819)）(PRをいただきました。ありがとうございます。)

### コマンドライン

- 不具合修正：異なるカレントディレクトリのWinMergeが実行中のまま、別のカレントディレクトリで`/s` オプションを指定して相対パスでファイルを比較するとファイル比較に失敗する問題を修正した。

### アーカイブサポート

- 7-Zip をバージョン25.00 に更新した。

### インストーラー

- インストーラー：Windowsの「プログラムと機能」に表示される名前にバージョン番号が含まれないようにした。（[#2798](https://github.com/WinMerge/winmerge/issues/2798)）

### 翻訳

- 翻訳の更新:
  - Brazilian (PR #2829)
  - Bulgarian (PR #2763)
  - Chinese Simplified (PR #2831)
  - Chinese Traditional (PR #2838)
  - Corsican (PR #2844)
  - French (PR #2754,#2761,#2762)
  - Hungarian (PR #2836)
  - Italian (PR #2832)
  - Japanese
  - Korean (PR #2766,#2845)
  - Lithuanian (PR #2799,#2805,#2826,#2830)
  - Portuguese (PR #2768)
  - Russian (PR #2760,#2840)
  - Swedish
  - Tamil (PR #2812,#2813)
  - Turkish (PR #2782)

### その他

- GetTranslationsStatus.py の文法警告を修正した。(PR #2751)（[PR #2751](https://github.com/WinMerge/winmerge/pull/2751)）(PRをいただきました。ありがとうございます。)

## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。（[#2685](https://github.com/WinMerge/winmerge/issues/2685)）
 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
