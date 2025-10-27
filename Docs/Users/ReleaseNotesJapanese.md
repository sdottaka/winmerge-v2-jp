# WinMerge 2.16.52 リリースノート

- [このリリースについて](#about-this-release)
- [2.16.52 の新機能](#what-is-new-in-21652)
- [2.16.51 beta の新機能](#what-is-new-in-21651-beta)
- [既知の問題](#known-issues)

2025年10月

## このリリースについて

WinMerge の 2.16.52 安定版リリースです。
このリリースは、以前の WinMerge 安定版リリースに代わる推奨リリースです。

不具合は <a href="http://github.com/WinMerge/winmerge/issues">bug-tracker</a> で報告してください。
日本語での報告は、<a href="https://sourceforge.net/p/winmerge-v2-jp/tickets/">こちら</a>でお願いします。

## <a name="what-is-new-in-21650"></a>2.16.52 の新機能

## WinMerge 2.16.52 の更新内容

### 全般

* 不具合修正: 何らかの理由で残っていた WinMerge の一時フォルダが、次回のアプリケーション終了時に正しく削除されない問題を修正した。(2.16.51からの問題)
* Ctrl+PageDown/PageUpでタブが切り替えられるようにした。([#2942](https://github.com/WinMerge/winmerge/issues/2942))
* ARM64 ビルドでクラッシュ問題が解決できなかったため、darkmodelib を無効化した。

### バイナリ比較

* 不具合修正: Hexビューで Ctrl+W を押した際にウィンドウを閉じる動作に関する問題を修正した。 ([#2294](https://github.com/WinMerge/winmerge/issues/2294))

### フォルダ比較

* 不具合修正: フォルダ比較メソッドが「更新日時のみ」または「更新日時またはサイズ」の場合に更新日時が1秒差でも一致とみなすことがあったのを修正した。 ([#2973](https://github.com/WinMerge/winmerge/issues/2973))
* toDateStr フィルタ関数を追加した。
* 追加の比較条件を指定できるオプションを追加した。 ([PR #2963](https://github.com/WinMerge/winmerge/pull/2963))
* フィルタ式で prop、leftprop、middleprop、rightprop 関数をサポートした。 ([PR #2974](https://github.com/WinMerge/winmerge/pull/2974))
* 「Existence（存在）」フォルダ比較方法を追加した。 ([PR #2980](https://github.com/WinMerge/winmerge/pull/2980))

### 翻訳

* 翻訳更新:
  * ブラジルポルトガル語 ([PR #2981](https://github.com/WinMerge/winmerge/pull/2981), [#2977](https://github.com/WinMerge/winmerge/pull/2977), [#2995](https://github.com/WinMerge/winmerge/pull/2995))
  * 簡体字中国語 ([PR #2978](https://github.com/WinMerge/winmerge/pull/2978), [#2991](https://github.com/WinMerge/winmerge/pull/2991), [#2996](https://github.com/WinMerge/winmerge/pull/2996))
  * コルシカ語 ([PR #2999](https://github.com/WinMerge/winmerge/pull/2999))
  * イタリア語 ([PR #2976](https://github.com/WinMerge/winmerge/pull/2976), [#2982](https://github.com/WinMerge/winmerge/pull/2982), [#2998](https://github.com/WinMerge/winmerge/pull/2998))
  * 日本語
  * 韓国語 ([PR #2993](https://github.com/WinMerge/winmerge/pull/2993))
  * リトアニア語 ([PR #2975](https://github.com/WinMerge/winmerge/pull/2975), [#2986](https://github.com/WinMerge/winmerge/pull/2986), [#2997](https://github.com/WinMerge/winmerge/pull/2997))
  * ポルトガル語 ([PR #2971](https://github.com/WinMerge/winmerge/pull/2971))
  * ポーランド語 ([PR #2972](https://github.com/WinMerge/winmerge/pull/2972), [#2979](https://github.com/WinMerge/winmerge/pull/2979), [#3003](https://github.com/WinMerge/winmerge/pull/3003), [#3005](https://github.com/WinMerge/winmerge/pull/3005))
  * トルコ語 ([PR #2992](https://github.com/WinMerge/winmerge/pull/2992))
  * ロシア語 ([PR #2983](https://github.com/WinMerge/winmerge/pull/2983))

## WinMerge 2.16.51 Beta の更新内容

### 全般

- 不具合修正: ウインドウ内で右クリックしながらウインドウの外にポインタを移動して右ボタンを離した後、マウスホイールで次または前の差異に移動してしまうようになる問題を修正した。([#2939](https://github.com/WinMerge/winmerge/issue/2939))

### 外観

* ダークモードに対応した。([PR #2834](https://github.com/WinMerge/winmerge/pull/2834))(PRをいただきました。ありがとうございます。)
* ハンバーガーメニューのちらつきを減らした。

### ファイル比較

* "改行を無視(空白として扱う)"比較オプションを追加した。 ([PR #2945](https://github.com/WinMerge/winmerge/pull/2945))

### フォルダー比較

* 不具合修正: [除外ファイルを追加]→[エディターのバックアップファイル]メニューで追加された除外ファイルが正しくない問題を修正した。(ほとんどのファイルが除外されてしまう)

### フィルターダイアログ

- ウインドウサイズを変更できるようにした。（[PR #2907](https://github.com/WinMerge/winmerge/pull/2907)）

### オプションダイアログ

* 変更した色を新しいスキームとして保存できるように変更 ([#1180](https://github.com/WinMerge/winmerge/issues/1180), [PR #2908](https://github.com/WinMerge/winmerge/pull/2908))

### 翻訳

* 翻訳更新:

  * ブラジルポルトガル語 ([#2886](https://github.com/WinMerge/winmerge/pull/2886), [#2910](https://github.com/WinMerge/winmerge/pull/2910), [#2951](https://github.com/WinMerge/winmerge/pull/2951))
  * 簡体字中国語 ([PR #2889](https://github.com/WinMerge/winmerge/pull/2889), [#2916](https://github.com/WinMerge/winmerge/pull/2916), [#2952](https://github.com/WinMerge/winmerge/pull/2952))
  * コルシカ語 ([PR #2915](https://github.com/WinMerge/winmerge/pull/2915))
  * フランス語 ([PR #2887](https://github.com/WinMerge/winmerge/pull/2887), [#2938](https://github.com/WinMerge/winmerge/pull/2938), [#2969](https://github.com/WinMerge/winmerge/pull/2969))
  * ハンガリー語 ([PR #2909](https://github.com/WinMerge/winmerge/pull/2909), [#2948](https://github.com/WinMerge/winmerge/pull/2948))
  * イタリア語 ([PR #2892](https://github.com/WinMerge/winmerge/pull/2892), [#2911](https://github.com/WinMerge/winmerge/pull/2911), [#2956](https://github.com/WinMerge/winmerge/pull/2956))
  * 日本語
  * 韓国語 ([PR #2913](https://github.com/WinMerge/winmerge/pull/2913), [#2934](https://github.com/WinMerge/winmerge/pull/2934), [#2950](https://github.com/WinMerge/winmerge/pull/2950))
  * リトアニア語 ([PR #2912](https://github.com/WinMerge/winmerge/pull/2912), [#2936](https://github.com/WinMerge/winmerge/pull/2936), [#2953](https://github.com/WinMerge/winmerge/pull/2953))
  * ポルトガル語 ([PR #2928](https://github.com/WinMerge/winmerge/pull/2928))
  * ポーランド語 ([PR #2929](https://github.com/WinMerge/winmerge/pull/2929), [#2930](https://github.com/WinMerge/winmerge/pull/2930), [#2931](https://github.com/WinMerge/winmerge/pull/2931))
  * ロシア語 ([PR #2890](https://github.com/WinMerge/winmerge/pull/2890), [#2919](https://github.com/WinMerge/winmerge/pull/2919), [#2920](https://github.com/WinMerge/winmerge/pull/2920), [#2933](https://github.com/WinMerge/winmerge/pull/2933), [#2944](https://github.com/WinMerge/winmerge/pull/2944), [#2949](https://github.com/WinMerge/winmerge/pull/2949))
  * スペイン語 ([PR #2961](https://github.com/WinMerge/winmerge/pull/2961))
  * スウェーデン語
  * トルコ語 ([PR #2906](https://github.com/WinMerge/winmerge/pull/2906), [#2914](https://github.com/WinMerge/winmerge/pull/2914), [#2957](https://github.com/WinMerge/winmerge/pull/2957))
  * ウクライナ語 ([PR #2932](https://github.com/WinMerge/winmerge/pull/2932), [#2937](https://github.com/WinMerge/winmerge/pull/2937), [#2954](https://github.com/WinMerge/winmerge/pull/2954))

### 内部処理

* bindoption の使用にリファクタリング ([PR #2955](https://github.com/WinMerge/winmerge/pull/2955))


## <a name="known-issues"></a>既知の問題

- `/inifile` オプションで指定された INI ファイルを WinMerge で比較中に、オプションウィンドウで OK を押すとファイルが破損する可能性がある。（[#2685](https://github.com/WinMerge/winmerge/issues/2685)）
 - フォルダ比較で画像比較を有効にした場合、比較結果が安定しない。 [(#1391)](https://github.com/WinMerge/winmerge/issues/1391)
 - 巨大ファイルの比較でクラッシュすることがある。[(#325)](https://github.com/WinMerge/winmerge/issues/325)
 - 大幅に異なるフォルダの比較が非常に時間がかかる。 [(#322)](https://github.com/WinMerge/winmerge/issues/322)
 - 新規作成で表示範囲を超えるテキストを貼り付けたとき、垂直スクロールバーでスクロールできない。 [(#296)](https://github.com/WinMerge/winmerge/issues/296)
