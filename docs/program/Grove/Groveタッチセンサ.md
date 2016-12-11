# Groveタッチセンサ

![5v](../../img/ic/5v.png) ![3.3v](../../img/ic/3.3v.png) ![digital](../../img/ic/digital.png)


![Touch Senser](groveimg/grovetouch.jpg)


タッチセンサはスイッチの代わりに指を近づけることで反応します。
静電容量方式で動いており、直接触らなくても近づいたことを検知することができます。

このセンサーはデジタル出力で、タッチした時HIGHを出力します。


## 仕様

|||
|:--:|:--:|
|動作電圧|2.0v-5.5v|
|動作電流(VCC=3v)|1.5 - 3.0μA|
|動作電流(VCC=5V)|3.5 - 7.0μA|
|出力応答時間|60 - 220ms|
|IC|TTP223-BA6|

## 動作確認

|Nefry|
|:---:|
|![NefryOK](../../img/ic/nefry-ok.png)|

##サンプルプログラム

![Nefry Touch Senser](groveimg/nefrytouch.jpg)

<script src="http://gist-it.appspot.com/github/Nefry-Community/Arduino/blob/master/libraries/Nefry/examples/Nefry_Digital_IN_OUT/Nefry_Digital_IN_OUT.ino">
</script>

詳細データ 
http://wiki.seeed.cc/Grove-Touch_Sensor/
