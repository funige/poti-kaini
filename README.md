# POTI-board改二

<img width="300" alt="0z674" src="https://user-images.githubusercontent.com/31465648/83109430-5ebf0080-a0fc-11ea-8acc-87f2fbbd2070.PNG">

phpお絵かき掲示板スクリプトPOTI-boardをさらに改良していくプロジェクトです。  
php5.5～ 対応。
  
<a href="https://github.com/funige/neo/">PaintBBS NEO</a>  
~~POTI-board改~~ POTI-board改は保守作業およびサポートを終了しました。

## ！デジタルインク(windows Ink)の機能について！

デジタルインク(Window Ink)がオンの状態でPaintBBS NEO / しぃペインターを操作すると、
例えばペンを左から右に大きくスライドさせるとブラウザが前の画面に戻る、などの誤動作が発生する可能性が大きくあります。PaintBBS NEO / しぃペインターご利用の際はデジタルインク(Window Ink)をオフにお願いいたします。

<img width="200" alt="0z676" src="https://user-images.githubusercontent.com/31465648/83109254-0c7ddf80-a0fc-11ea-9627-7b4afe5ae193.PNG">  

また、マウスジェスチャーの拡張機能とも競合する可能性があります。不具合を感じたらオフにしてみてください。
  
## 概要
POTI-board改で使用しているテンプレートエンジン「htmltemplate.inc」は老朽化が進んでいる… 
ということでなんか新しいテンプレートエンジンはないか探したところ、
  
<a href="http://skinny.sx68.net/">Skinny</a>  
  
見つけました！これに移植します！ → できました！

## サンプル/サポート

[POTI改公式サイト](https://poti-k.info/) をオープンしました。質問や動作確認にご利用ください。

## 使い方
基本的に <a href="https://github.com/sakots/poti-kai/">POTI-board改</a> と同じですが、テーマ(スキン/テンプレート機能)を置くフォルダができました。  
config.phpの設定をし、アップロードしてpotiboard.phpのあるディレクトリにアクセスするだけです。  
さとぴあさんの[詳しい記事](http://stp.sblo.jp/article/185357941.html)

## ちょっとした注意
2020/07/23以降のバージョンにはindex.phpというファイルが同梱されています。  
これは、potiboardの設置をより簡単にするためのものです。  
念のため、potiboard.phpをindex.phpにリネームしてお使いの方は、上書きしないようお願いいたします。  
また、新規設置される方はできるだけpotiboard.phpのリネームを行わないようにお願いいたします。

## 古いpotiboardから改二へのバージョンアップ
ログの形式は同じですが、config.phpが若干違います。また、テーマ(テンプレート)の形式は全く違います。configを同じように設定して、対応したテーマをテーマフォルダに入れてpotiboard.php、config.php、テーマフォルダをアップロードすればOKのはずです。質問はPOTI改公式まで！！

## テーマ(テンプレート)機能について

このスクリプトはテーマ(テンプレート)機能に対応しています。作り方（変数名）はデフォルトテーマのreadmeに詳しく書いています。  
[テーマリポジトリ](https://github.com/sakots/poti-kaini-themes)を参照ください。

---

## 履歴

### [2020/08/03] v2.9.6 lot.200803

- ソースコード整理(by きつねこ)

### [2020/08/02] v2.9.5 lot.200802

- ソースコード整理(by さとぴあ)

### [2020/08/02] v2.9.4 lot.200802

- ソースコード整理(by きつねこ)

### [2020/08/02] v2.9.3 lot.200802

- ソースコード整理(by きつねこ)
  - すべての処理が終わった後のunsetは不要
  - globalをローカル変数に置換
  - 関数内でしか使わない変数は関数内で代入するよう修正

### [2020/08/02] v2.9.2 lot.200802

- ソースコード整理(by きつねこ)
  - `switch($mode)` の場所を移動
  - 冒頭の `$mode` 取得周りの冗長性を排除

### [2020/08/01] v2.9.1 lot.200801

- updatelogのページャを微修正、カタログのページャをリファクタリング(by きつねこ)

### [2020/08/01] v2.9.0 lot.200801

- ページャのレンダリング部分をリファクタリング(by きつねこ)

### [2020/08/01] v2.8.14 lot.200801

- 新規投稿時に画像ファイルがあるときは、画像のアップロードが成功しましたとでていたが、でなくなっていたのを修正。
- オートリンク関連(by さとぴあ)

### [2020/08/01] v2.8.13 lot.200801

- ソースコード整理(by きつねこ)
  - 三項演算子化

### [2020/08/01] v2.8.12 lot.200801

- ソースコード整理(by きつねこ)
  - 関数化

### [2020/07/31] v2.8.11 lot.200731

- ソースコード整理(by さとぴあ)
  - `CleanStr()` に引数を追加して、コメントのみの時の処理もそれ以外の時の処理もひとつの関数で行えるように

### [2020/07/31] v2.8.10 lot.200731

- ソースコード整理(by さとぴあ)
  - pchファイルアップロードの位置とき書き方を変更

### [2020/07/31] v2.8.9 lot.200731

- ソースコード整理(by きつねこ)
  - if/elseを三項演算子化
  - 不要なコードを除去

### [2020/07/31] v2.8.8 lot.200731

- ソースコード整理(by きつねこ)
  - 冗長な処理を関数化

### [2020/07/31] v2.8.7 lot.200731

- ソースコード整理(by きつねこ)
  - 必ず代入される箇所を三項演算子に置換
  - 各種処理後のリダイレクトを関数化

### [2020/07/31] v2.8.6 lot.200731

- 続きを描くでneoのpchなのにしぃペインターが起動してしまうバグ修正(by さとぴあ)

### [2020/07/29] v2.8.5 lot.200729

- トリップ廃止の後方互換性確保
- `function head()` → `function basicpart()`

### [2020/07/29] v2.8.3 lot.200729

- トリップ廃止
- メールアドレスが入っていてもIDを表示。
  - ともに「何の説明もないから」

### [2020/07/29] v2.8.2 lot.200728

- コード簡略化、バグの原因になるものを除去(byさとぴあ、きつねこ)

### [2020/07/28] v2.8.1 lot.200727

- `$textonly` が画像なしの時にファイルアップロード欄に画像がセットされていた時のワークファイル削除処理を追加(by さとぴあ)
  - （ほぼ念の為）

### [2020/07/26] v2.8.0 lot.200726

- 管理者画面にアップロード欄を出す時の処理を変更(by さとぴあ)
  - 画像アップ禁止コメントのみも禁止の時は投稿フォームをださない
- テーマ

### [2020/07/25] v2.7.9 lot.200725

- 画像アップロード禁止でも管理者は許可
- コメントのみの新規投稿を拒否するしないの新規設定項目を追加。

### [2020/07/25] v2.7.8 lot.200725

- 画像アップロード機能を使う、使わないを設定可能できるように

### [2020/07/24] v2.7.7 lot.200723

- 負荷削減。カタログモードの時はpchの存在確認の処理をしない(by さとぴあ)

### [2020/07/23]

- index.php(初期動作用)を同梱
  - 設置がより簡単になりました。

### [2020/07/23]

- テーマ更新

### [2020/07/22]

- テーマ更新

### [2020/07/20]

- search.php 負荷削減

### [2020/07/18]

- search イラストの単位を「枚」コメントの単位を「件」に
- theme CSS

### [2020/07/16]

- テーマ更新、readmeを除去。（テーマのreadmeはテーマのリポジトリ参照）

### [2020/07/15]

- テーマのcss更新

### [2020/07/14] v2.7.6 lot.200714

- `<% echo (oya/encoded_name) %>` `<% echo (oya/res/encoded_name) %>`追加(by さとぴあ)
- search.phpをリポジトリに統合

### [2020/07/13] v2.7.5 lot.200712

- 文字列のエラーチェックを先に行いGDを使った画像関連の処理はそのあとで(by さとぴあ)

### [2020/07/12] v2.7.4 lot.200711

- 規定容量を超えるとJPEGに変換、JPEGとPNGを比較してファイルサイズが小さなほうを出力(by さとぴあ)
  - くわしくは[こちら](https://github.com/sakots/poti-kaini/pull/51)

### [2020/07/10]

- テーマ開発用のファイルを削除しリポジトリを分離[poti-kaini-themes](https://github.com/sakots/poti-kaini-themes)

### [2020/07/10] v2.7.3 lot.200708

- 投稿されたPNG画像が指定kbを超えた時にJPEG化する処理の調整(by さとぴあ)
  - くわしくは[こちら](https://github.com/sakots/poti-kaini/pull/50)

### [2020/07/05] v2.7.2 lot.200704

- 本文へのURLの書き込みを禁止時、通常の投稿でも削除キーが管理パスと一致すればurlの投稿ができるように
- さくらでなくても自動で作成されるため設置方法のディレクトリに関する説明を修正
- 古いurlを変更など(by さとぴあ)

### [2020/07/01] v2.7.1 lot.200701

- neoのpchかどうかの確認時に使用する関数をバイナリセーフなものに(by さとぴあ)
- neo更新

### [2020/06/30] v2.7.0 lot.200630

- 動画再生の時にNEOのpchかJavaのpchかを判定(by さとぴあ)

### [2020/06/26] v2.6.9 lot.200626

- v2.6.8で追加した箇所の修正(by さとぴあ)

### [2020/06/26] v2.6.8 lot.200625

- php5.6,php7.2の時に致命的エラーが発生していたv2.6.3以降のバージョンの文法ミスを修正。
- 画像アップロードやNEOのPNGファイルも設定したファイルサイズの上限を超過した時はJPEGに変換、そのJPEG画像がファイルサイズに違反していなければ投稿できるようにした。
- それにともないHTMLのフォームによるファイルサイズの制限を2MB、picpost.phpで受信できる画像のファイルサイズを3MBにそれぞれ緩和。

### [2020/06/23] v2.6.7 lot.200622

- 軽微なバグ修正

### [2020/06/09] v2.6.6 lot.200609

- 動画表示モード時の修正

### [2020/06/09] 

- neo更新
  - に伴ってテーマ更新

### [2020/06/08] (テーマ)

- chrome83のキャッシュが強くてneoが更新されないことがあるの対策

### [2020/06/08]

- なぜかsiihelpファイルが残っていたので削除

### [2020/06/03]

- テーマ修正

### [2020/06/03] v2.6.5 lot.200603

- コード整理

### [2020/06/02] v2.6.4 lot.200602

- 文字色選択のバグ修正
- config初期値変更
- メール通知設定整理 (by さとぴあ)

### [2020/06/02]

- loadcookie.js with文の見直し
- テーマ修正

### [2020/05/30] v2.6.3 lot.200530a

- 改行タグ関連のコードを元に戻した

### [2020/05/30] v2.6.2 lot.200530

- 改行タグ関連のコードを整理
- 安定版だと思う

### [2020/05/28]

- テーマ修正

### [2020/05/27]

- Skinny.php 設定変更（キャッシュを1時間→1日に）

### [2020/05/23]

- Skinny.php改変、またそれを明記。

### [2020/05/23] v2.6.1 lot.200523

- デバッグスイッチ実装(開発者用)

### [2020/05/22]

- suEXECを導入してあるサーバーで動かない可能性があるのを修正(Skinny.php)

### [2020/05/22] v2.6.0 lot.200522a

- `<SIIHELP>` 廃止

### [2020/05/22]

- config整理

### [2020/05/22] v2.5.2 lot.200522

- デフォルトでテーマのキャッシュを有効にした（Skinny.php）
- テーマのreadme修正
- コード整理

### [2020/05/21] v2.5.1 lot.200521

- デフォルトテーマを修正
- 安定版

### [2020/05/20] v2.5.0 lot.200520

- スキン/テンプレートの呼び名を「テーマ(テンプレート)」に
- デフォルトテーマ(テンプレート)のディレクトリ名変更

### [2020/05/19]

- リポジトリ名変更（kaizi → kaini）ご迷惑おかけします…

### [2020/05/19] v2.4.1 lot.200519a

- デフォルトスキン更新
- configに説明追加

### [2020/05/19]

- noticemailをpotiboard2ディレクトリから分離

### [2020/05/19] v2.4.0 lot.200519

- Firefox、およびcheerpJのインストールなしでもchromeでしぃペインターが使用可能に

### [2020/05/18] v2.3.4 lot.200518b

- スキンをかなり更新
- コード整理 (by さとぴあ)

### [2020/05/18] v2.3.3 lot.200518a

- 強制サムネイル機能を削除 (thumbnail_gd.phpのバージョンアップがあります)

### [2020/05/18] v2.3.2 lot.200518

- cookieを取得するだけで使用していなかった個所を削除 (by さとぴあ)

### [2020/05/17] v2.3.1 lot.200517f

- ユーザー削除の安全性向上(by さとぴあ)

### [2020/05/17] v2.3.0 lot.200517e

- ユーザー削除権限の変更(config.phpに変更があります) (by さとぴあ)
- スキンの安全性、ユーザビリティ向上。

### [2020/05/17] v2.2.8 lot.200517d

- デバッグのdumpが残っていたので削除(by さとぴあ)

### [2020/05/17] v2.2.7 lot.200517c

- 「投稿者名をコピー」機能搭載。(by さとぴあ)
- スキンをそれに対応。

### [2020/05/17] v2.2.6 lot.200517b

- デフォルトスキン修正

### [2020/05/17] 

- skinディレクトリの.htaccess設定変更
- おまけスキンnee2更新

### [2020/05/17] v2.2.5 lot.200517a

- configの説明追加、デフォルト値変更。
- アプレットのセキュリティチェックに引っかかった場合のURL用htmlファイルを同梱。
  - デフォルト設定ではお絵かき掲示板のindex.htmlに飛ばされてしまうため、なぜ投稿失敗したのかがわからないから。
  - セキュリティにヒットした場合の飛び先を define('SECURITY_URL', './security_c.html'); に設定変更してください。

### [2020/05/17] v2.2.4 lot.200517

- デフォルトでしぃペインターに対応

### [2020/05/16] v2.2.3 lot.200516e

- readme_pch.html を追加。Javaのpchビューワー配布条件に必要でした。(by さとぴあ)
- thumbnail_re.php を削除。現在のバージョンのPOTIでは使っていない。(by さとぴあ)

### [2020/05/16] v2.2.2 lot.200516d

- 対応スキン用にしぃちゃんアプレットを本体に同梱。[Readme_Shichan.html](./potiboard2/Readme_Shichan.html)

### [2020/05/16] v2.2.1 lot.200516c

- Skinnyを配布用に設定変更

### [2020/05/16] v2.2.0 lot.200516b

- ミニレスフォームを日数経過で閉じる機能追加（スキンの仕様が変わりました）
- v2.1までとconfigの互換性がなくなっていますので注意。（CRYPT_PASSが大文字になっただけです）
- configデフォルト変更

### [2020/05/16]

- config説明追加

### [2020/05/16] v2.1.1 lot.200516a

- 軽微なエラーつぶし
- configの調整

### [2020/05/16] v2.1.0 lot.200516

- スキンともども安定版

### [2020/05/15] v2.0.9 lot.200515

- 改行できなくなっていたバグに完全対応

### [2020/05/15] v2.0.8 lot.200515

- 改行できなくなっていたのを暫定対処

### [2020/05/15] v2.0.7 lot.200515

- config.phpの整理(by さとぴあ) - 時系列のものを種類別にした

### [2020/05/15]

- デフォルトスキンバージョンアップ
- スキンのreadme整理

### [2020/05/15] v2.0.6　lot.200515

- PROXY_CHECK関連のコードを削除(by さとぴあ)

### [2020/05/15] v2.0.5　lot.200515

- 改行の抑制とProxyチェックを廃止によるエラーを修正

### [2020/05/15] v2.0.4　lot.200515

- 改行の抑制とProxyチェックを廃止(by さとぴあ)
- potiboard.phpの上のほうの説明を修正

### [2020/05/15] v2.0.3　lot.200515

- 独自タグ関連エラー修正(by さとぴあ)
- palette.txtの読み込み処理修正(by さとぴあ)
- デフォルトスキン

### [2020/05/15] v2.0.2　lot.200515

- palette.txtの読み込み処理(by さとぴあ)

### [2020/05/15] v2.0.1　lot.200515

- 独自タグ廃止に関するエラー修正。(2.0.0動かないです)
- スキン修正

### [2020/05/15] v2.0.0　lot.200515

- $getで記事の編集をできないように変更(byさとぴあ)
- 独自タグ廃止
- noticemailのutf-8以外を削除
- 満を持して2.0.0として公開

### [2020/05/14] v2.0.0a8

- 管理パスをグローバル定数から変数に変更(byさとぴあ)
- スキンフォルダのcss以外へアクセスできないように.htaccessを設定

### [2020/05/14] v2.0.0a7

- DEF_FONTCOLORの設定がないテンプレートの場合を想定

### [2020/05/14]

- 動画が再生されないの、スキンの問題でした。

### [2020/05/14] v2.0.0a6

- デフォルトスキン変更、スキンフォルダ作成 (config.php要再設定！)
- palleteの問題に暫定対処

### [2020/05/14] v2.0.0a5

- htmlの生成に成功(byさとぴあ) 大感謝。
- スキンのエラー修整。

### [2020/05/13] v2.0.0a4

- htmlは生成されないが、動く。

### [2020/05/07] v2.0.0a3

- いちからつくりなおす。
- ログが生成されるのは確認、HTML生成されず

### [2018/09/16] v2.0.0a2

- 記録

### [2018/09/15] v2.0.0a1

- プロジェクト開始
- ログが生成されるのは確認、HTML生成されず
