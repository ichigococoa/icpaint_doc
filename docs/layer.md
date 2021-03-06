---
hide:
  - toc
---

レイヤーの種類は以下の通りです。

+ 描画レイヤー
+ ドット絵レイヤー
+ ベクターレイヤー
+ テキストレイヤー
+ フォルダ
+ 調整レイヤー


## 合成モード

使用可能な合成モードは以下の通りです。

+ 通常
+ 比較(暗)
+ 乗算
+ 焼き込みカラー
+ 焼き込み(リニア)
+ 減算
+ 比較(明)
+ スクリーン
+ 覆い焼きカラー
+ 覆い焼き(発光)
+ 加算
+ 加算(発光)
+ オーバーレイ
+ ソフトライト
+ ハードライト
+ 差の絶対値
+ ビビッドライト
+ リニアライト
+ ピンライト
+ ハードミックス
+ 除外
+ カラー比較(暗)
+ カラー比較(明)
+ 除算
+ 色相
+ 彩度
+ カラー
+ 輝度

フォルダを選択している場合は、「通過」という合成モードも使用できます。

「__通過__」は、フォルダの中のレイヤーの合成モードがフォルダを貫通して動作します。
フォルダの中にない場合と同じです。
フォルダの合成モードが「通過」以外の場合は、フォルダの中のレイヤーをいったん合成して、
その結果をキャンバス内のほかのレイヤーと合成します。

「通過」にしたフォルダの上のレイヤーの「クリッピングマスク」をオンにした場合、
Photoshop ではクリッピングの効果は有効ですが、
クリスタと SAI Ver.2 ではクリッピングの効果が無効になります。
このペイントソフトでは、クリスタと SAI Ver.2 に合わせて無効になるように作りました。
これは、「通過」にしたフォルダを非表示にした場合に、
Photoshop ではフォルダの上の「クリッピングマスク」をオンにしたレイヤーも非表示扱いになりますが、
クリスタと SAI Ver.2 では非表示扱いにならないという違いがあります。


## 合成モードのほかのペイントソフトとの対応表

| このペイントソフト | CLIP STUDIO PAINT (クリスタ) | ペイントツール SAI Ver.2       | Photoshop        |
| ------------------ | ---------------------------- | ------------------------------ | ---------------- |
| 覆い焼きカラー     | 覆い焼きカラー               | [TS] 覆い焼きカラー            | 覆い焼きカラー   |
| 覆い焼き(発光)     | 覆い焼き(発光)               | 覆い焼きカラー または 覆い焼き | 覆い焼きカラー   |
| 加算               | 加算                         | [TS] 覆い焼き(リニア)          | 覆い焼き(リニア) |
| 加算(発光)         | 加算(発光)                   | 覆い焼き(リニア) または 発光   | 覆い焼き(リニア) |

「覆い焼き(発光)」は、 Photoshop で合成モードを「覆い焼きカラー」にして「レイヤースタイル」の「レイヤー効果」
で「透明シェイプレイヤー」をオフにしたレイヤーとだいたい同じになります。

「加算(発光)」は、 Photoshop で合成モードを「覆い焼き(リニア)」にして「レイヤースタイル」の「レイヤー効果」
で「透明シェイプレイヤー」をオフにしたレイヤーとだいたい同じになります。

「焼き込み(リニア)」、「焼き込みカラー」、「リニアライト」、「ビビッドライト」、「ハードミックス」、
「差の絶対値」の 6 つの合成モードは SAI Ver.2 では [TS] と名前がついている合成モードと、だいたい同じになります。
例えば、このペイントソフトで「焼き込み(リニア)」にしたレイヤーは、 SAI Ver.2 では「 [TS] 焼き込み(リニア)」
にしたレイヤーとだいたい同じになる、ということです。

このペイントソフトで psd 形式で保存したファイルを、クリスタや SAI Ver.2 や Photoshop などで開いた場合、
全く同じ見た目、全く同じ RGB 値にはなりませんので注意してください。
ある程度、同じ見た目になるようには作っています。
そもそも、クリスタと SAI Ver.2 と Photoshop も、同じ psd 形式のファイルを開いた場合、
全く同じ見た目、全く同じ RGB 値にはなっていません。

このペイントソフトが、ほかのペイントソフトと比べて、特に違う見た目になるのは「覆い焼き(発光)」です。

「覆い焼き(発光)」は、 SAI Ver.2 と Photoshop と比べて、ぼやけて光る範囲がやや狭く、白く輝く部分がやや弱めです。
ほかの合成モードと比べてずれが大きいです。
クリスタに関しては、そもそも下地の色が薄い状態での「覆い焼き(発光)」の効果が SAI Ver.2 と Photoshop
と大きく違うので、「覆い焼き(発光)」に関しては、 SAI Ver.2 と Photoshop の見た目に近くなるように作っています。

Photoshop には、レイヤーの不透明度と塗りの不透明度の 2 つの項目があります。
このペイントソフトでのレイヤーの不透明度の変更は、 Photoshop のレイヤーの不透明度の変更と同じ挙動になりますが、
「覆い焼き(発光)」と「加算(発光)」の 2 つの合成モードのみ、 Photoshop の塗りの不透明度の変更と同じ挙動になります。
例えば、このペイントソフトで「覆い焼き(発光)」の合成モードにして、レイヤーの不透明度を 70 % にしたレイヤーは、
Photoshop では、「覆い焼きカラー」で「透明シェイプレイヤー」をオフにして、塗りの不透明度を 70 %
にしたレイヤーとだいたい同じになります。


## レイヤー名

レイヤー名には絵文字や普段使わないような文字も使うことができますが、
「レイヤー」ウィンドウの中のレイヤー名には、正しく表示されない場合があります。
例えば、レイヤー名に絵文字や中国語などを設定した場合、「レイヤー」ウィンドウの中のレイヤー名には、
その文字が表示されません。

これは、このペイントソフトのウィンドウ内で表示される文字は、
内部で事前にこちらが用意した文字しか表示できない構造になっているためです。

ただし、ウィンドウ内で文字が正しく表示されていなくても、その文字自体は正しく保存しています。
psd 形式で保存してから、 Photoshop などで保存したファイルを開くと、正しくレイヤー名が保存されています。


## 用紙質感

用紙質感画像ウィンドウを開くには、
メニューの「キャンバス」をクリックし、「ウィンドウ」から「用紙質感画像ウィンドウ」をクリックします。
または、「キャンバス」ウィンドウの中の「用紙質感画像ウィンドウ」をクリックします。

「用紙質感画像」ウィンドウの中の「追加」ボタンをクリックして、用紙質感画像を読み込みます。
「用紙質感画像」ウィンドウの中の「レイヤーに設定」をクリックすることで、
選択しているレイヤーに、用紙質感を適用することができます。


## 用紙質感のパラメータ

「キャンバス」ウィンドウの中の「__拡大率__」で、用紙質感画像の効果を拡大縮小できます。

「__強さ__」で、用紙質感の効果を調節できます。

「__RGB 反転__」で、 RGB をそれぞれ反転します。

「__アルファを使用__」は、オンにすると、用紙質感画像の RGBA の A を使います。

例えば、透明な背景に小さめのイラストを描いた画像(png 形式)があったとして、
それを用紙質感画像として使う場合、
「アルファを使用」をオンにすると、画像の透明な部分は描画されない状態になります。

「__画像の取り外し__」をクリックすることで、用紙質感の適用を解除することができます。

「用紙質感画像」ウィンドウには、用紙質感の画像データは残っているので、
「用紙質感画像」ウィンドウの中の「__レイヤーに設定__」をクリックすることで、
再度、用紙質感を適用することができます。


## レイヤーマスクを使う流れ

1. 「キャンバス」ウィンドウの中の「__レイヤーマスクを作成__」をクリックし、レイヤーマスクを作成します

1. 「ツール選択」ウィンドウの中の「マスク塗り」の中の「マスクブラシ」(アイコン)をクリックします

1. キャンバス内をドラッグすると、その部分だけ描画した内容を非表示(マスク)にすることができます


## レイヤーマスクについて

「__レイヤーマスクを作成__」をクリックした段階では、マスクはないので作成前と見た目の変化はありません。

「マスクブラシ」で、ブラシモードを「消しゴム」にして塗ると、塗った部分にマスクがかかり、
その部分の描画内容が非表示になります。
ブラシモードを「通常」にして塗ると、逆にマスクがかかった非表示の部分を表示することができるようになります。

レイヤーマスクには不透明度があります。

キャンバス内でどこにマスクがあるのかは、「キャンバス」ウィンドウの中の「__マスクを緑で表示__」をクリックすることで、
確認することができます。

「マスクブラシ」で塗る時は、「色」ウィンドウの現在の色の RGBA の A と
「ツール」ウィンドウの中の「濃度」で、ブラシで塗る際の強弱が決定します。

「__マスクを無効化__」をクリックすることで、レイヤーマスクの効果を一時的に無効にすることができます。

「__マスクを反転__」をクリックすることで、キャンバス内のマスク部分を反転させることができます。
表示されている部分が非表示になり、非表示にしていた部分が表示されます。

「__レイヤーマスクを削除__」をクリックすることで、レイヤーマスクを削除します。

「__マスクを適用__」をクリックすることで、レイヤーマスクの効果を描画内容に適用した上で、
レイヤーマスクを削除します。

Photoshop・SAI Ver.2 では、レイヤーマスクで半透明にした部分は「覆い焼きカラー」「覆い焼き(リニア)」の部分は明るくなりません。

CLIP STUDIO PAINT(クリスタ) では、レイヤーマスクで半透明にした部分は「覆い焼き(発光)」
「加算(発光)」の部分は明るくなります。

このペイントソフトでは、クリスタと同じように、レイヤーマスクで半透明にした部分も「覆い焼き(発光)」
「加算(発光)」の部分は明るくなるように作っています。

マスクボックス塗りツール・マスク円塗り・マスク楕円塗り・マスク投げ縄塗りに関しては、
Alt を押しながらの場合は、必ず通常モードになります(非表示にしていた部分を表示するモードです)。

メニューの「レイヤー」をクリックし、「その他」の中の「__レイヤーマスクを保存__」をクリックすることで、
現在のレイヤーマスクの状態を保存することができます。
「__レイヤーマスクを読込__」をクリックすることで、保存したレイヤーマスクの状態を復元できます。
保存した時のキャンバスの幅と高さと、読み込む時のキャンバスの幅と高さが同じでないと、
読み込むことができませんので注意してください。


## クリッピングマスクについて

「キャンバス」ウィンドウの中の「__クリッピングマスク__」をオンにすると、
現在選択しているレイヤーの下にあるレイヤーの描画内容によって、表示のされ方が変わります。

例えば、下にあるレイヤーが丸い円だけ描画していた場合、
その上の「クリッピングマスク」をオンにしたレイヤーは、その丸い円の部分のみ表示されます。
それ以外の描画した部分は非表示になります。

下にあるレイヤーも「クリッピングマスク」がオンなら、さらにその下を見ます。


## 不透明度を保護・レイヤーのロック・レイヤーのチェックについて

「キャンバス」ウィンドウの中の「__不透明度を保護__」をオンにすると、
ブラシで塗る際、現在選択しているレイヤーの描画されている部分しか、塗りの効果が出なくなくなります。
描画内容のアルファを維持します。

「キャンバス」ウィンドウの中の「__ロック__」をオンにすると、
現在選択しているレイヤーをブラシで塗ることができなくなります。

「キャンバス」ウィンドウの中の「__チェック__」の項目は、
例えば、メニューの「レイヤー」の「ビュー」の中の「__チェックしたレイヤーの表示/非表示__」などで
使用されます。


## レイヤーの描画内容の移動

メニューの「レイヤー」の「変形」の中の「__移動__」は、
「__自由な変形__」や「__移動拡大回転__」と同じ仕組みで、操作方法を移動のみに限定したものです。
キャンバス内のどこでも自由に移動できます。
「__スタンプ__」機能や「__スナップ__」機能もあります。
ただし、レイヤーマスクは同時に移動されません。

これに対して、メニューの「レイヤー」の「移動」の中のコマンドは、移動量(ピクセル単位)を事前に指定して、
上下左右のいずれか 1 つの方向に移動できます。
選択範囲がない状態での移動は、レイヤーマスクも同時に移動されます。
選択範囲がある状態での移動は、レイヤーマスクは同時に移動されません。選択範囲自体は同時に移動されます。

メニューの「レイヤー」の「移動」の中の「__上に 1 px 移動__」は 1 px だけ移動しますが、
「__上に移動__」の場合は、「__移動量を設定__」でセットしたピクセル数だけ移動します。
「下に移動」「左に移動」「右に移動」も同様にセットしたピクセル数だけ移動します。


## 調整レイヤー

調整レイヤーとは、描画内容に手を加えずに、さまざまなカラー調節を行うことができるレイヤーです。
調整内容はいつでもあとから修正できます。

調整レイヤーは、メニューの「レイヤー」の「レイヤー作成」の中の「__新規調整レイヤー__」をクリックすることで
作成することができます。

「キャンバス」ウィンドウの中の「__調整モード__」で調整内容を変更できます。

選択できる調整モードは以下の通りです。

+ __色相・彩度・輝度__
+ __色相・彩度・明度__
+ __明るさ・コントラスト__
+ __グラデーションマップ__
+ __レベル補正__
+ __トーンマップ__
+ __明るいフィルター__
+ __暗いフィルター__
+ __カラーバランス__
+ __2階調化__


例えば、「カラーバランス」では、「ハイライト」に RGB(30, 30, 0) あたりをセットし、
「シャドウ」に RGB(30, 0, 120) あたりをセットすることで、描画内容の明るい部分に黄色を少し追加し、
暗い部分に青紫を少し追加することができます。
カラーバランスの調整項目の「2 つ目の位置」とは中間調の位置のことです。

調整レイヤーは、「キャンバス」ウィンドウの中の「不透明度」を調整することで、調整レイヤーの効果を調節できます。
不透明度を 0 にすると調整レイヤーを非表示にしている場合と同じになります。

調整レイヤーは、「クリッピングマスク」をオンにすることで、下にあるレイヤーにのみ効果を与えることができます。

調整レイヤーにレイヤーマスクを作成することで、効果を与える範囲をレイヤーマスクで指定することができます。


## そのほかのレイヤー機能

メニューの「レイヤー」の「レイヤー操作」の中の「__レイヤーを複製__」は、
レイヤーの内容を丸ごと複製できます。描画レイヤーのほかに、
フォルダ・調整レイヤー・ベクターレイヤー・テキストレイヤー・ドット絵レイヤーにも使うことができます。

メニューの「レイヤー」の「レイヤー操作」の中の「__レイヤーをコピーペースト__」は、
描画レイヤーに対して、選択範囲の部分だけ描画内容をコピーして新規レイヤーに貼り付けます。
レイヤーマスクもコピーペーストします。選択範囲がない場合、描画内容を丸ごとコピーペーストします。

メニューの「レイヤー」の「レイヤー操作」の中の「__下のレイヤーに転写__」は、
現在選択しているレイヤーの下にあるレイヤーに描画内容を移し、
現在選択しているレイヤーの描画内容を消去します。

メニューの「レイヤー」の「レイヤー操作」の中の「__下のレイヤーと結合__」は、
現在選択しているレイヤーの下にあるレイヤーと結合し、レイヤーを 1 つにします。

メニューの「レイヤー」の「レイヤー操作」の中の「__すべてのレイヤーを統合__」は、
現在のキャンバスの見た目を維持したまま、レイヤーを 1 つにします。

メニューの「レイヤー」の「レイヤー操作」の中の「__レイヤー不透明度を最大__」は、
例えば、現在選択しているレイヤーの不透明度が 50 とすると、この見た目を維持したまま、
レイヤーの不透明度を 100 に変更します。

メニューの「レイヤー」の「レイヤー操作」の中の「__輝度を透明度に変換__」は、
例えば、現在選択しているレイヤーの描画内容の各ピクセルの RGB をもとに輝度を計算して、
その値をアルファとしてセットします。 RGB は (0, 0, 0) の黒にセットされます。
例えば、スケッチブックなどに鉛筆で描いたものをスキャナーでスキャンして、
画像としてパソコンに取り込んだとします。この画像は白の背景色(下地)となっています。
「輝度を透明度に変換」を実行することで、この白い部分を透明にすることができます。

---

メニューの「レイヤー」の「レイヤーの並び替え」の中の「__前面へ(上に)(同一階層)__」は、
現在選択しているレイヤーを 1 つ上のレイヤーに並び替えます。
フォルダの中に入ったり、フォルダを越えて並び替えたりはしません。
同じ階層にいることを維持します。

メニューの「レイヤー」の「レイヤーの並び替え」の中の「__前面へ(上に)__」は、
現在選択しているレイヤーを 1 つ上のレイヤーに並び替えます。
フォルダの中に入ったり、フォルダを越えたりもします。

---

メニューの「レイヤー」の「サイズ変更」の中の「__比率サイズ変更(ボックス)__」と
「__px 単位でサイズ変更(ボックス)__」は、
例えば、「ドット塗りツール」で、ドット絵のように、ピクセル単位で色を付けた場合に、
「比率サイズ変更(ボックス)」で 200 % で拡大すると、ドット絵の見た目を維持したまま、
2 倍に拡大することができます。ぼやけずに拡大できます。

---

メニューの「レイヤー」の「フィルター」の中の「__ガウスぼかし__」は、
レイヤーの変形の自由な変形や移動拡大回転で、移動などの変形はせずに、「フィルター」ウィンドウで
「ガウスぼかし」を有効にして、完了するのと全く同じことです。
ボタン 1 つで簡単にぼかしを実行できるようにしたものです。

---

メニューの「キャンバス」の「ビュー」の中の「__描画範囲の枠の表示__」は、
現在選択しているレイヤーの描画内容がどこにあるのかを見やすくするためのものです。
この枠は、描画内容を覆う最小の枠ではありません。
例えば、ブラシで描画して、一部、消しゴムで消した、などの場合では更新されません。
この枠の中に描画内容が含まれる、程度の目安です。
