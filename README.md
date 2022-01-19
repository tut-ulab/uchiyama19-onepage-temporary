# about OnePage
 「OnePage」は、オンラインのポスターセッションの際に、お互いがポスターの中のどこを指して話しているかがわかりにくいという問題を解決するWebアプリケーションです。  
 また、従来のプレゼンテーションツールには存在しない「好きに見る」機能や、聴衆から発表者へ直ちに意見があることを示すことができる「マグネット」という点ポインティング機能があります。  
 
 OnePageで主に行う操作は５つあります。
 - 範囲選択
 - 拡大縮小表示
 - 「好きに見る」⇔「一緒に見る」の切り替え
 - マグネットの移動
 - マグネットの点滅

　また、OnePageの動作を補助する「OnePageRecorder」も付属しています。

# environment
 node.js v14.16+  
 npm 6.14.12+

# install
`` git clone https://github.com/KakuAmane19/OnePage2``  
または、Zipファイルをダウンロードして、解凍してください  
`` cd OnePage2``   

`` npm install`` でパッケージを読み込んでください

# How to run
OnePage2のノード直下で
``npm start``
とすると、サーバーが立ち上がります 

# How to use

## setup
ユーザー全員が同じページにアクセスします。
音声通信はZoomやGoogleMeetなど別のアプリを使います。

### 範囲選択
任意矩形範囲の選択と、枠による強調表示ができます。
左上の角になる箇所を１度クリックし、続けて右下の角となる２か所目をクリックします。
左上の角になる箇所をクリックしたあと、半透明で緑色の四角がマウスカーソルについてきます。これは、できる枠の目安となります。
範囲選択をキャンセルしたいときは、一回目のクリックの後、その座標より左上の箇所をクリックしてください。  
![範囲選択](https://github.com/KakuAmane19/imagesGarage/blob/main/OnePage-1.png)

### 拡大縮小表示
枠で囲んだ範囲を画面いっぱいに拡大表示します。
範囲選択をしたあと、左上にある拡大ボタンをクリックすると、拡大します。
拡大から戻るときは、左上にあるボタンが縮小となっているので同様にクリックします。  
![拡大縮小表示](https://github.com/KakuAmane19/imagesGarage/blob/main/OnePage-2.png)

### 「好きに見る」⇔「一緒に見る」の切り替え
画面左上、拡大（縮小）ボタンの横にあるチェックボックスです。
デフォルトはチェックが入っています。
チェックが入っている状態を「好きに見る」状態といい、青い枠でポスターの一部を囲みます。
チェックが外れている状態を「一緒に見る」状態といい、赤い枠で任意範囲を囲みます。
また、「一緒に見る」状態ならば、同じページにアクセスしており、かつ「一緒に見る」状態にしている全員が、一つの枠と、マグネット（赤い丸）を共有しており、操作することができます。  
![モードチェンジ](https://github.com/KakuAmane19/imagesGarage/blob/main/OnePage-3.png)

### マグネットの移動
「一緒に見る」状態のときのみ表示される、赤い丸をマグネットといいます。
移動させるときは、まずマグネットをクリックし、次に移動先をクリックします。  
![マグネット](https://github.com/KakuAmane19/imagesGarage/blob/main/OnePage-4.png)

### マグネットの点滅
マグネットの上で右クリックするとマグネットが点滅します。
点滅しているか否かも、「一緒に見る」状態の全員に共有されます。

# OnePageRecorder
　OnePageRecorderは、「一緒に見る」状態の枠の座標や、拡大縮小状態、マグネットの位置をひとまとめにした**Status**を保存します。  
　Statusは記録ボタンを押したときに番号を付けて記録されます。  
　再生ボタンを押すと、指定した番号のStatusをOnePageに送信します。番号は自由に指定することできます。また、ボタンをおすと自動的に番号が一つ次に進みます。
![レコーダー](https://github.com/KakuAmane19/imagesGarage/blob/main/OnePage-Ex2.png)

# about tcs branch
　現在別ブランチに、TypeScriptやwebpackなどを用いて本アプリをリファクタリングしています。可能な限りわかりやすく書き直しているつもりなので、コードを読みたい方はそちらを参照してください。
また、こちらのバージョンでは、任意のポスターファイル（pdf）をアップロードすることができます。
まだ全機能を書き直しきれていないため、このブランチをビルドしても、正しく動作しません。ご了承願います。
