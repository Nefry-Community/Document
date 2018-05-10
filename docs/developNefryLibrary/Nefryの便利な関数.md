# Nefryの便利な関数

Nefryの便利な関数をまとめました。

## reset

Nefryをリセットし、プログラムを初めからやり直します。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|void（なし）|Nefry.reset();|


## sleep

Nefryを省電力モードのスリープモードにします。  

**スリープモードに入ると処理ができません。**  

スリープが終わった後はプログラムを初めからやり直します。  
スリープモードを強制的終了させるにはNefry本体のリセットボタンを押してください。  

0を入力することで、無期限スリープモードになります。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|int（ここにスリープする秒数を入力します。単位は秒です。）|void（なし）|Nefry.sleep(30);|

## getWebServer

WebServerを扱うことができます。  
Webページを追加することができます。  
Nefryのメインページにそのリンクを貼りたいときは```setIndexLink```関数を使ってください。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|WebServer*（WebServerのポインタで返ってきます。）|Nefry.getWebServer();|

## setIndexLink

Nefryのメインページにリンクを貼ることができます。

|引数1|引数2|返り値|具体例|
|:---:|:---:|:---:|
|const char[32]（メインページに表示したいリンク文字をいれてください。）|const char[32]（追加ページのURLを入力してください。）|void（なし）|Nefry.setIndexLink("Nefryの秘密","/secret");|


## setProgramName

Nefryのトップページで表示されるプログラム名を設定できます。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|const char*（プログラム名を設定できます。）|void（なし）|Nefry.setProgramName("Nefry Display");|

## getProgramName

Nefryのトップページで表示されるプログラム名を取得することができます。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|String（プログラム名を取得することができます。）|Nefry.getProgramName();|

## getVersion

Nefryライブラリのバージョンを取得することができます。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|String（Nefryライブラリのバージョンを取得することができます。）|Nefry.getVersion();|


## getModuleName

NefryのModule名を取得することができます。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|char* （NefryのModule名を取得することができます。）|Nefry.getModuleName();|

## ndelay

**廃止予定**

delayではすべての処理が止まってしまいますがこちらを選ぶことで停止時間にNefryのWeb表示などの様々な機能を継続することができます。
基本的に500ミリ秒以上の待ち時間になる場合はこちらを選んでください。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|unsigned long（ミリ秒で時間を指定します。1000ミリ秒＝1秒）|void（なし）|Nefry.ndelay(1000);//一秒待つ|
