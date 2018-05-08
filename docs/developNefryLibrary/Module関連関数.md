# Module関連関数

NefryのModule Setup関連の関数をまとめてみました。Nefryに必要な設定などを行うことができます。  
このページの内容は、Nefryが表示しているWebページでも扱えます。


##文字列管理
文字列は0-2の欄は128文字まで、3-7の欄は64文字までの入力ができます。
## getConfStr
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : getStoreStr

NefryのModule Setupで入力された文字列を取得できます。  
入力された文字列をプログラム内で使う際にこの関数が便利です。  
入力欄は初期状態では表示されないので```setConfHtmlStr```関数を使って表示させるようにしてください。

||||
|:---:|:---:|:---:|
|引数1|int|取得したい文字列を数値で指定します。0-7の範囲で指定してください。|
|返り値|char*|入力された文字列を取得できます。|
|具体例||Nefry.println(Nefry.getConfStr(0));|

## setConfHtmlStr
![2.3.0u](pic/2.3.0u.png)  
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : setStoreTitleStr

NefryのModule Setupで指定された欄を表示します。**これを呼ばないとModule Setupに表示されません。**
説明を書くことができるので、上手くつかってください。

||||
|:---:|:---:|:---:|
|引数1|const char[15]|15文字以内でこの入力欄についての説明をする。|
|引数2|int|表示したい文字列を数値で指定します。0-7の範囲で指定してください。|
|返り値|void|なし|
|具体例||Nefry.setConfHtmlStr(”Nefry ID”,0);|

## setConfStr
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : setStoreStr

NefryのModule Setupに文字列を代入することができます。  
デフォルト値として始めから文字を入れておきたいときにこの関数が便利です。  
入力欄は初期状態では表示されないので```setConfHtmlStr```関数を使って表示させるようにしてください。

||||
|:---:|:---:|:---:|
|引数1|const char*|128文字 or 64文字の入力に対応しています。|
|引数2|int|保存したい文字列の場所を数値で指定します。0-7の範囲で指定してください。|
|返り値|void|なし|
|具体例||Nefry.setConfStr(”Nefry ID”,0);|

##数値管理
-32,768 ～ 32,767の範囲で数値を扱うことができます。
## getConfValue
![2.3.0u](pic/2.3.0u.png)  
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : getStoreValue
NefryのModule Setupで入力された数値を取得できます。  
入力された数値をプログラム内で使う際にこの関数が便利です。  
入力欄は初期状態では表示されないので```setConfHtmlValue```関数を使って表示させるようにしてください。

||||
|:---:|:---:|:---:|
|引数1|int|取得したい数値を数値で指定します。0-7の範囲で指定してください。|
|返り値|int|入力された数値を取得できます。|
|具体例||Nefry.println(Nefry.getConfValue(0));|

## setConfHtmlValue
![2.3.0u](pic/2.3.0u.png)  
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : setStoreTitleValue
NefryのModule Setupで指定された欄を表示します。**これを呼ばないとModule Setupに表示されません。**
説明を書くことができるので、上手くつかってください。

||||
|:---:|:---:|:---:|
|引数1|const char[15]|15文字以内でこの入力欄についての説明をする。|
|引数2|int|表示したい数値を指定します。0-7の範囲で指定してください。|
|返り値|void|なし|
|具体例||Nefry.setConfHtmlValue(”Nefry Value”,0);|

## setConfValue
![2.3.0u](pic/2.3.0u.png)  
![nefrybt](pic/nefrybt.jpg)

###NefryBT関数 : setStoreValue
NefryのModule Setupに文字列を代入することができます。  
デフォルト値として始めから文字を入れておきたいときにこの関数が便利です。  
入力欄は初期状態では表示されないので```setConfHtmlValue```関数を使って表示させるようにしてください。

||||
|:---:|:---:|:---:|
|引数1|int|-32,768 ～ 32,767の範囲で数値の入力に対応しています。|
|引数2|int|保存したい数値の場所を数値で指定します。0-7の範囲で指定してください。|
|返り値|void|なし|
|具体例||Nefry.setConfValue(10,0);|




<!-- 
##その他の関数
setConfModul
Auth
setConfUser
login
getConfHtmlPrint
setConfHtmlPrint
setConfWifi
setConfHtml
 -->
