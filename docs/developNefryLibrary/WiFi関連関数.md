# WiFi関連関数

NefryのWiFi関連の関数をまとめました。

WiFiに必要な設定などを行うことができます。  
このページの内容は、Nefryが表示しているWebページでも扱えます。

## addWiFi

WiFiの設定を追加することができます。

5つまでのWiFiを保存することができます。  
5つを超えた場合最も古いデータから削除されます。

変更が完了したら ```saveWiFi``` 関数で保存してください。

|引数１|引数２|返り値|具体例|
|:---:|:---:|:---:|:---:|
|String（接続したい端末のSSID）|String（接続したい端末のパスワード）|void（なし）|Nefry.addWiFi("SSID","Password");|

## deleteWiFi

WiFiの設定を削除することができます。削除するデータをIDで指定します。  
getlistWifi関数でIDについて確認することができます。

変更が完了したら ```saveWiFi``` 関数で保存してください。

|引数１|引数２|返り値|具体例|
|:---:|:---:|:---:|:---:|
|int（削除ID）|bool（（指定なしOK**必ず最後のみ**保存をするかどうか）|void（なし）|Nefry.deleteWifi(1);|

## saveWiFi

WiFiの設定を保存します。追加や削除をメモリに保存します。

|引数|返り値|具体例|
|:---:|:---:|:---:|:---:|
|void（なし）|void（なし）|Nefry.saveWiFi();|

## getWiFiList

WiFiの設定を表示することができます。IDとSSIDを表示することができます。  

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|String（WiFiの保存情報）|Nefry.println(Nefry.getWiFiList());|
