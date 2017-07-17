# WiFi関連関数

NefryのWiFi関連の関数をまとめてみました。WiFiに必要な設定などを行うことができます。  
このページの内容は、Nefryが表示しているWebページでも扱えます。

## addWifi
![2.3.0](pic/2.3.0.png)  
![nefrybt](pic/nefrybt.jpg)

WiFiの設定を追加することができます。5つまでのWiFiを保存することができます。  
5つを超えた場合最も古いデータから削除されます。

||||
|:---:|:---:|:---:|
|引数1|String|接続したい端末のSSID|
|引数2|String|接続したい端末のパスワード|
|返り値|void|なし|
|具体例||Nefry.addWifi("SSID","Password");|

## getlistWifi
![2.3.0](pic/2.3.0.png)  
![nefrybt](pic/nefrybt.jpg)

WiFiの設定を表示することができます。IDとSSIDを表示することができます。  

||||
|:---:|:---:|:---:|
|引数||なし|
|返り値|String|WiFiの保存情報|
|具体例||Nefry.println(Nefry.getlistWifi());|


## deleteWifi
![2.3.0](pic/2.3.0.png)  
![nefrybt](pic/nefrybt.jpg)

WiFiの設定を削除することができます。削除するデータをIDで指定します。  
getlistWifi関数でIDについて確認することができます。

||||
|:---:|:---:|:---:|
|引数1|int|削除ID|
|引数2|bool|(指定なしOK)**必ず最後のみ**保存をするかどうか|
|返り値|void|なし|
|具体例||Nefry.deleteWifi(1);|

## searchWiFi
![2.3.0](pic/2.3.0.png)  

WiFiを検索します。これは、デフォルトで呼ばれるため基本的にはユーザが呼ぶ必要はありません。

||||
|:---:|:---:|:---:|
|引数||なし|
|返り値|int|0:接続済み 0以外:接続Err|
|具体例||Nefry.searchWiFi();|

## setWiifAuto
![2.3.0](pic/2.3.0.png)  

WiFiの自動接続をするかどうかを選択できます。

||||
|:---:|:---:|:---:|
|引数1|bool|true:自動接続する false:自動接続しない|
|返り値|void|なし|
|具体例||Nefry.setWiifAuto(false);|


## setWifiTimeout
![2.3.0](pic/2.3.0.png)  
![nefrybt](pic/nefrybt.jpg)

WiFiの再接続回数の上限を制限します。

||||
|:---:|:---:|:---:|
|引数1|int|再接続回数の上限を制限します。|
|返り値|void|なし|
|具体例||Nefry.setWifiTimeout(10);|

## setWifiTimeoutClear
![2.3.0](pic/2.3.0.png)  
![nefrybt](pic/nefrybt.jpg)

WiFiの再接続回数のカウントをクリアします。

||||
|:---:|:---:|:---:|
|引数||なし|
|返り値|void|なし|
|具体例||Nefry.setWifiTimeoutClear();|

## autoConnect
![2.3.0u](pic/2.3.0u.png)  
廃止予定

WiFiの自動接続をします。Nefryのライブラリで自動接続を提供するので廃止を予定しています。

||||
|:---:|:---:|:---:|
|引数||なし|
|返り値|bool|true:接続済み false:接続Err|
|具体例||Nefry.autoConnect(10);|

<!-- 
getWifiTimeout
getWifiAuto
 -->
