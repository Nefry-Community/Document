# Console関連関数

Consoleに関連する関数をまとめてみました。  
Nefryのwebconsoleとserialに文字を表示します。Serialはデフォルトでは115200bpsで通信します。

## print
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

Nefryのwebconsoleとserialに文字を表示します。**改行なし**です。

||||
|:---:|:---:|:---:|
|引数|float,double,char,int,long,unsigned char,unsigned int,unsigned long,String|
|返り値|void|なし|
|具体例||Nefry.print("NefryWorld");//NefryWorldと表示されます。|


## println
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

Nefryのwebconsoleとserialに文字を表示します。**改行あり**です。

||||
|:---:|:---:|:---:|
|引数|float,double,char,int,long,unsigned char,unsigned int,unsigned long,String|
|返り値|void|なし|
|具体例||Nefry.print("NefryWorld");//NefryWorldと表示されます。|

##available
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

Nefryのwebconsoleで入力された文字数を返します。

||||
|:---:|:---:|:---:|
|引数|void|なし|
|返り値|int|入力された文字数|
|具体例||Nefry.available();|

##read
![2.3.0u](pic/2.3.0u.png)
![nefrybt](pic/nefrybt.jpg)

Nefryのwebconsoleで入力された文字を返します。

||||
|:---:|:---:|:---:|
|引数|void|なし|
|返り値|String|入力された文字|
|具体例||Nefry.read();|
