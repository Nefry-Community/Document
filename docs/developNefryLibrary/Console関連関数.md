# Console関連関数

Consoleに関連する関数をまとめてみました。  
Nefryのwebconsoleとserialに文字を表示します。Serialはデフォルトでは115200bpsで通信します。

## print

Nefryのwebconsoleとserialに文字を表示します。  
**改行なし** です。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|float,double,char,int,long,unsigned char,unsigned int,unsigned long,String|void（なし）|Nefry.print("NefryWorld");//NefryWorldと表示されます。|


## println


Nefryのwebconsoleとserialに文字を表示します。  
**改行あり** です。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|float,double,char,int,long,unsigned char,unsigned int,unsigned long,String|void（なし）|Nefry.print("NefryWorld");//NefryWorldと表示されます。|

## available


Nefryのwebconsoleで入力された文字数を返します。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|int（入力された文字数）|Nefry.available();|

## read

Nefryのwebconsoleで入力された文字を返します。

|引数|返り値|具体例|
|:---:|:---:|:---:|
|void（なし）|String（入力された文字）|Nefry.read();|
