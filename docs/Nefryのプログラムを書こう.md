#実際にコードを書いてみる
ここまでの作業お疲れ様でした。
ここからは実際にプログラムを書いてNefryを操っていきます。
## Arduinoのプログラムって？
NefryのプログラムはArduinoのプログラムと同じようにかけます。

ArduinoIDEが起動するとプログラムを入力するところに初めからこのようなプログラムが書いてあります。


```cpp
void setup(){

}

void loop(){

}
```

![](https://wamisnet.github.io/pic/ren/pic015.png)

簡単に説明していきます。

```cpp
void setup()
```
ここの部分では**起動時に一度だけ**行われる処理を書きます。
例えば、入出力ピンの設定や温度センサなどセンサ類の初期設定などを入力します。

```cpp
void loop()
```
ここの部分では**起動中ずっと繰り返し**行われる処理を書きます。
例えば、LEDの点滅やセンサーデータの取得などを入力します。

Nefryではこのsetupとloopをうまく活用してプログラムを書いていきます。
![](https://wamisnet.github.io/pic/ren/pic025.png)
##LEDを使ってみる
それでは、実際にNefryで動くプログラムを書いてみようと思います。

今回は、NefryについているフルカラーのLEDをランダムに光らせてみようと思います。
前もって、ArduinoIDEに書いてある文をすべて消しておいてください。

準備ができたら下のプログラムをコピーしてArduinoIDEの方に張り付けてください。


```cpp
#include <Nefry.h>
//フルカラーLED　ランダムにカラーが変わります。
void setup() {
  Nefry.println("フルカラーLED!");
  randomSeed(analogRead(A0));
}
int red,green,blue;
void loop() {
  red=random(255);//random関数は0-255の数値をランダムに返します。
  green=random(255);
  blue=random(255);
  Nefry.setLed(red,green,blue);//LEDがランダムに点灯します。
  String color="Red:";color+=red;
  color+=" Green:";color+=green;
  color+=" Blue:";color+=blue;
  Nefry.println(color);//Nefry consoleで色を表示
  Nefry.ndelay(1000);//1秒待つ
}
```


ところどころで使われているNefry関数については[こちら](http://qiita.com/wamisnet/items/e44812eb6d6fded7af26)にまとめてあるので興味があればご覧ください。
![](https://wamisnet.github.io/pic/ren/pic024.png)  
プログラムを保存します。
Nefryに書き込むプログラムがその指定した場所に保存されますので、保存する場所を覚えていてください。  
![](https://wamisnet.github.io/pic/ren/pic028.png)  
それではプログラムが書き終わり、保存する先も決まったら**スケッチ内のコンパイルしたバイナリを出力**をクリックしてください。
これでNefryに書き込めるようにファイルを変換しています。
少々時間が掛かりますがしばらくお待ちください  

![](https://wamisnet.github.io/pic/ren/pic026.png)  
   
プログラムに問題がないとコンパイルが完了しました。と表示されます。  
プログラムに問題があるとこの部分がおかしいとエラー表示が出ます。  
  
そのエラー表示を見てプログラムを修正します。  
よくある間違いとして、```;```がなかったり```()```が全角だったりするので見直してみてください。  
  
これでプログラムの準備は整いましたので次にNefryにプログラムを書き込んで実行します。  
  
![](https://wamisnet.github.io/pic/ren/pic027.png)

##Nefryに書き込む
ついにNefryにプログラムを書き込みます。

Nefryの便利なところを解説しつつ、プログラムを書き込んでいく流れを解説していきます。

NefryをモバイルバッテリーやPCのUSB端子に接続してください。
NefryがWiFiの信号を出しているので、そのWiFiに接続します。
しばらくしてWiFiを検索すると**Nefry-○○○○**という名前があると思うので、そのWiFiに接続してください。  
![](https://wamisnet.github.io/pic/ren/pic030.png)  
接続すると自動的にこのページに移動します。
時にうまくいかないときがあるのでその時はこちらのURLを入力してください。  
  
```http://192.168.4.1```
  
Nefryのメインページになっています。このページから他のページに移動して様々な設定などをすることができます。
それでは、プログラムを書き込むためにNefryを書き込みモードにします。
書き込みモードにすることでNefryがプログラムの書き込みの準備をします。
そのモードに変更するために**setup Module**をクリックします。  
(書き込みモードとは、NefryのCoreプログラムだけ動作し、ユーザが書き込んだプログラムを実行しないモードです。)  
![](https://wamisnet.github.io/pic/ren/pic031.png)  

setup ModuleではNefryに関する様々な設定をすることができます。
今回は書き込みモードに変更するので、**Write mode**をクリックしてください。
そうするとNefryが再起動するので、再起動が終わったら書き込みモードになっています。  
![](https://wamisnet.github.io/pic/ren/pic035.png)  
せっかくなので、setup Moduleの**Next page**をクリックするとどうなるのか説明します。

MacアドレスやIPアドレスなどインターネットにかかわる情報が表示されます。
アクセス制限かけている場合などここを見ていただくとよいかと思います。  
![](https://wamisnet.github.io/pic/ren/pic036.png)  
それではNefryが書き込みモードになったところでプログラムを書き込んでいきましょう。  
  
メインページの**upload Sketch**をクリックしてこのページを開きます。
開いたらページ中央にある**参照**となっているボタンをクリックしてファイルを選びます。
(chromeなどブラウザによっては表示が異なることがあります。)  
![](https://wamisnet.github.io/pic/ren/pic032.png)  
先ほどプログラムを保存した場所を開き、**arduino.bin**となっているファイルを選びます。
(ちゃんと確認してアップデートしてください。もし間違えた場合、最悪起動しなくなることもありえます。)  
![](https://wamisnet.github.io/pic/ren/pic033.png)  
ちゃんと選べるとファイルの場所を示す表示が出るようになります。ここまで来たらあとは**Upload**をクリックするだけです！  
![](https://wamisnet.github.io/pic/ren/pic034.png)  
アップロードが完了すると自動的にNefryが再起動してプログラムが更新されます。
これでNefryのプログラムを書きかえることができました！
おそらくLEDがカラフルに光っているはずです。

Nefryの便利な機能をあと少し紹介します。
**Nefry Console**といってNefryの状態を確認することができるページです。  
![](https://wamisnet.github.io/pic/ren/pic037.png)  
**Web Sketch Download**といってNefryのプログラムをwebからダウンロードして更新することができるページです。  
![](https://wamisnet.github.io/pic/ren/pic038.png)  
**setup WiFi**といってNefryが接続するWiFiを設定することができるページです。
設定すれば、インターネットに接続してMilkcocoaやIFTTTといったwebサービスと接続することができるようになります。  
![](https://wamisnet.github.io/pic/ren/pic039.png)  

##実際に動かしてみる
先ほどのプログラムを書き込むとLEDがランダムに光るデモです。  
![](https://wamisnet.github.io/pic/ren/led.gif)