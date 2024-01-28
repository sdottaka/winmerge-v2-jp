# WinMerge 2.16.38 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.38の新機能](#what-is-new-in-21638)
- [2.16.37 beta の新機能](#what-is-new-in-21637-beta)
- [既知の問題](#known-issues)

2024年1月

## このリリースについて

WinMerge の 2.16.38 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21638"></a>2.16.38 の新機能

### ファイル比較

- 不具合修正: コードページダイアログで右側のBOMを変更しても反映されない問題を修正した。
- C++ シンタックスハイライトのキーワードを更新した。 [(PR#2166)](https://github.com/WinMerge/winmerge/pull/2166)(PRをいただきました。ありがとうございます。)

### Webページ比較

- 比較中はステータスバーに「比較しています...」を表示するようにした。
- ロケーションペインを追加した。 [(PR#2160)](https://github.com/WinMerge/winmerge/pull/2160)

### フォルダー比較

- [列の表示]ダイアログのボタンの活性/非活性制御の改善。 [(PR#2154)](https://github.com/WinMerge/winmerge/pull/2154)(PRをいただきました。ありがとうございます。)

### プラグイン

- 不具合修正: 以下のように二重引用符を文字列が `/unpacker` コマンドライン引数に指定された場合に正しく解釈されない問題を修正した。
    
    `/unpacker "Replace ""a"" ""b"""`

### 翻訳

- 翻訳の更新:
  - Brazilian (PR#2151,#2178)
  - Chinese Simplified (PR#2153,#2183)
  - Corsican (PR#2180)
  - Hungarian (PR#2156,#2157,#2158)
  - Japanese
  - Korean (PR#2152)
  - Lithuanian (PR#2155,#2177)
  - Portuguese (PR#2185)

## <a name="what-is-new-in-21637-beta"></a>2.16.37 Beta の新機能

### ファイル比較

- 不具合修正: 「行を右端で折り返す」が有効な場合、ロケーションペインをクリックしたときにスクロール位置が予期しない位置になる問題を修正した。
- 不具合修正: ステータスバーをクリックしてもエンコーディング等のメニューが表示されない問題を修正した。  [(#2129)](https://github.com/WinMerge/winmerge/issues/2129)
- 不具合修正: 正規表現検索で `\r` を使用してもCRを見つけられない問題を修正した。
- 新しい C# のキーワードを追加した。 [(PR#2136)](https://github.com/WinMerge/winmerge/pull/2136)(PRをいただきました。ありがとうございます。)

### フォルダー比較

- 不具合修正: バイナリコンテンツ比較方法でフォルダ比較した場合、空のファイルがコピーできない問題を修正した。[(#2146)](https://github.com/WinMerge/winmerge/issues/2146)

### バイナリ比較

- 不具合修正: ファイルの末尾のデータが置換できない問題を修正した。

### 画像比較

- 不具合修正: 新規作成で表示されたペインのテキストを名前を付けて保存で保存してもヘッダーにファイル名が表示されない問題を修正した。

### Webページ比較

- 不具合修正: "他のアプリケーションがファイル ... を更新しました。ファイルを開きなおしますか?"というメッセージボックスが、`file://` 形式のURLを比較する際に表示される問題を修正した。
- イベント同期機能の改善 [(winmerge/winwebdiff#4)](https://github.com/WinMerge/winwebdiff/pull/4)

### 翻訳

- 翻訳の更新:
  - Bulgarian (PR #2124)
  - French (PR #2135,#2140,#2141,#2142,winmerge/frhed#15)
  - Italian (PR #2130)
  - Korean (PR #2126,#2127,#2143)
  - Polish (PR #2128)


## <a name="known-issues"></a>既知の問題

 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
