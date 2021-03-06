---
hide:
  - toc
---

2021/07/12 : ペイントソフトを作り始める。C言語(C17)

2021/09/02 : 最低限の機能のペイントソフトができたので glTF 形式による 3D 描画をやってみる。
20 日以上かかってリアルな 3D 描画はできたが問題が多いので後回しにする(今後の課題)

2022/01/15 : ペイントソフトによくある機能をある程度作った。
作ったソフトを公開するためにドキュメント(マニュアル)作りに取りかかる(このページも含めて作成開始)

この時点でできること一覧

+ 64 bit アプリ, 一部でマルチスレッド対応, WinTab API 対応,  TabletPC API 対応
+ キャンバスの機能(解像度変更, サイズ変更, キャンバスの背景変更, グリッド, キャンバス作成時のプリセット(A4 など))
+ レイヤーの種類(描画レイヤー, ドット絵レイヤー, ベクターレイヤー, テキストレイヤー, フォルダ)
+ レイヤーの機能(塗りつぶし, 複製, 転写, 結合, すべて結合, 見た目を維持したまま不透明度最大化, レイヤーの並び替え)
+ レイヤーの機能(不透明度, クリッピングマスク, 不透明度を保護, ロック, レイヤーマスク)
+ 加算(発光)や覆い焼き(発光)も含めた合成モード(全28種類)
+ レイヤーの機能(サイズ変更(拡大縮小のアルゴリズムは3種類), 移動, 変形, 数値入力で変形, メッシュ変形(ゆがみ))
+ レイヤーの変形の際は、 Ctrl, Shift, Alt を使って様々な変形(均一拡大やアンカーを中心に回転など)ができる
+ 用紙質感機能(用紙質感用の合成モード(全28種類), 用紙質感画像の拡大縮小, 用紙質感の強さ設定)
+ ドット絵レイヤーの機能(カラーインデックス機能, 共通パレットとレイヤーパレット, パレットの読込と保存)
+ ドット絵レイヤーの機能(描画内容のサイズ変更, 移動)
+ アニメーション機能(フレームの追加と設定, スピード設定, タイルモード(9分割表示), データとして読込と保存)
+ ベクターレイヤーの機能(制御点移動・追加・鋭角化・削除, カーブ複製, カーブ移動, 複数の制御点を同時に移動)
+ ベクターレイヤーの機能(制御点ごとに角度変更(形状変更), 筆圧点による筆圧調節, 筆圧点の追加と位置移動)
+ ベクターレイヤーの機能(カーブを閉じる, 閉領域を塗りつぶし, 塗りつぶしに用紙質感, カーブに沿ってブラシ機能)
+ ベクターレイヤーの機能(ブラシ機能にブラシツールとほぼ同等の機能, カーブの並び替え, データとして読込と保存)
+ テキストレイヤーの機能(フォント読込, テキスト移動, サイズ変更, 行間, 字間, アンチエイリアスかドットか)
+ テキストレイヤーの機能(太字, 斜体文字, 縦書き対応, テキストの並び替え, データとして読込と保存)
+ グラデーション機能(線形か円形か, 5色までセット可能, 移動・拡大縮小・回転, プリセットとして読込と保存)
+ フィルター(この時点で全40種類(カラー調整, ぼかし, ゆがみ, モザイク, グラデーションマップ, 煙, ノイズなど))
+ ブラシ円(ハード, ソフト, ややソフト, ドット), ブラシ円に画像を使うことも可能(ストロークに沿って画像回転可能)
+ ブラシモード(通常, マーカー, 消しゴム, 焼き込み, 覆い焼き, 加算, 指先, ぼかし, 平均色, 色混ぜ)
+ ぼかしモードではぼかす範囲を設定可能, 色混ぜモードでは混色・色延び・水分量の調節可能
+ ブラシの散布機能(ランダム位置, ランダムサイズ, ランダム濃度)
+ 手ぶれ補正, 筆圧によるサイズと濃度変更, 筆圧の柔らかさ設定
+ ブラシ円は正円のほかに楕円も可能, Shift 押しながらの直線描画
+ ブラシベース画像(テクスチャ機能, ブラシベース画像の拡大縮小, 強さ設定)
+ ブラシプリセット機能, プリセットの読込と保存, ブラシサイズウィンドウ
+ 描画用のツール(ブラシ, カーブブラシ, ボックス塗り, 枠, 円, 楕円, 多角形, 投げ縄, 塗りつぶし, ドット塗り)
+ 選択範囲用のツール(ブラシ, ボックス塗り, 円塗り, 楕円塗り, 投げ縄塗り, 塗りつぶし)
+ レイヤーマスク用のツール(ブラシ, ボックス塗り, 円塗り, 楕円塗り, 投げ縄塗り)
+ ドット絵用のツール(ブラシ, 消しゴム, ボックス塗り, 枠, 円, 楕円, 多角形, 投げ縄, 塗りつぶし)
+ その他のツール(キャンバスの移動, ズーム, 回転, アニメーションの表示を移動・ズーム, スポイト)
+ 高解像度モニターに対応するため UI の拡大率を 250 % まで対応可能, キャンバス外の背景色の変更
+ ショートカットキーの機能(割り当てできるコマンドはこの時点で約185種類)
+ Undo / Redo の機能(元に戻す / やり直す機能)
+ 独自フォーマットでのキャンバスの保存
+ psd, png, jpg, bmp, tga, webp, gif の形式のファイルの読込と保存
+ カラーサークル, カラーセット, カラーセットの読み込みと保存, 色履歴機能(ブラシで描画ごとに更新)

2022/02/07 : レイヤーの合成のやり方をすべて作り直す。
フォルダへの合成モード・フォルダへのクリッピング・フォルダの結合などができるようになる。

2022/02/12 : メッシュ変形(ゆがみ)をすべて作り直す。
以前とは全く別の方法で Photoshop のゆがみフィルターのようなものができる。

2022/02/20 : フォルダにもマスクを使えるようにする。
独自フォーマットのキャンバスファイルをエクスプローラからダブルクリックで開く機能追加。
ペイントソフト内にファイルをドロップしてキャンバスを開く機能追加。
ペイントソフトのアイコン作成。

2022/02/22 : ドキュメントを公開開始(このページも含めて)。
タブレット PC に Visual Studio をインストールして動作確認を開始。

2022/02/24 : タブレット PC で起きるバグ(vkCreateDescriptorPool 関連とボタンのタッチ判定)を修正。
キーボードのない環境(タブレット PC)で手のひらツールやズームツールに切り替えるのが面倒なので
「キャンバスビュー」ウィンドウを追加。

2022/02/27 : ドット絵の回転機能追加。ラスタライズ機能追加。 GPU 関連のエラー処理を追加。

2022/02/28 : version 1.0.0 として icpaint.exe を公開。
「キャンバスビュー」ウィンドウでのビューの一時保存機能追加。
 icsetting ファイルにカラーセットデータを保存できるようにする。描画範囲の枠の表示機能追加。

2022/03/09 : webp 形式ファイルの保存と読込機能追加。レイヤーのピクセル単位の移動機能追加。
出力ウィンドウ追加。描画内容のコピーペースト機能追加。

2022/03/11 : 選択範囲の保存と読込機能追加。レイヤーマスクの保存と読込機能追加。
選択ブラシとマスクブラシの設定内容を設定ファイルに保存するようにした。

2022/03/16 : glTF 形式ファイルの読込機能追加。 ktx 形式ファイルの読込機能追加。リアルな 3D 描画機能追加。
3D の描画内容をレイヤーに転写する機能を追加。 3D ウィンドウ追加。

2022/03/19 : 調整レイヤー機能を追加。追加した調整レイヤーは、「色相・彩度・輝度」、「色相・彩度・明度」、
「明るさ・コントラスト」、「グラデーションマップ」、「レベル補正」、「トーンマップ」、「明るいフィルター」、
「暗いフィルター」、「カラーバランス」。フィルターにも同様の効果を追加。
調整レイヤーのレイヤーマスク機能・クリッピングマスク機能追加。
輝度を透明度に変換コマンドを追加。

2022/03/22 : 前回の自由な変形(キャンバスサイズ)コマンドを追加。
調整レイヤーに「2階調化」を追加。フィルターにも同様の効果を追加。


## 開発環境

メインパソコン(デスクトップパソコン)

+ Windows 10
+ Intel Core i7-9700 CPU
+ 8コア/8スレッド
+ RAM 16.0 GB
+ NVIDIA GeForce RTX 2060
+ WinTab API


サブパソコン(タブレット PC)

+ Windows 10
+ raytrektab (DG-D10IWP)
+ Celeron N4100 (4コア)
+ Intel UHD Graphics 600
+ RAM 8.0 GB
+ TabletPC API

---

使用している液タブ(動作確認した液タブ)

+ Wacom Cintiq Pro 24
+ XP-PEN Artist Pro 16

ちなみに、この 2 つの液タブを比べた時、 Wacom Cintiq Pro 24 のほうが、はるかにきれいでなめらかな線になります。

---

このペイントソフトの制作にあたって参考にしたペイントソフト(保有しているペイントソフト)

+ CLIP STUDIO PAINT PRO Version 1.11.4 (クリスタ)
+ ペイントツール SAI Ver.2 Preview.2021.07.06
+ Adobe Photoshop CS6 (Adobe Photoshop CC は持っていません)
