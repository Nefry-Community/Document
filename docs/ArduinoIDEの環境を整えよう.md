#ArduinoIDEのインストール
Arduinoとは、電子工作に興味を持った方やハードウエアを使って簡単に作品を作ってみたい方におすすめする電子工作のプラットフォームです。
Arduinoを使うメリットは、ハードウエアの難解なところを簡単な Arduino 言語と呼ばれるもので開発できるようになるところです。ArduinoIDEとはそのArduino言語を書くことができるツールのことです。
NefryもArduinoIDEをつかってプログラムします。
##ダウンロード
Arduinoの[公式サイト](https://www.arduino.cc/)からDownloadをクリックしてArduinoIDEをダウンロードします。
![](https://wamisnet.github.io/pic/ren/pic000.png)

どのバージョンをダウンロードするか選択します、現在(2016/11/22)最新の1.6.12をお勧めします。
適切なものを選んでダウンロードしてください。
Windowsであれば、**Windows　Installer**のものをオススメします。
Macであれば、**Mac OS X**をインストールしてください。  
![](https://wamisnet.github.io/pic/ren/pic001.png)

クリックするとこのようなページが表示されます。JustDownloadをクリックするとダウンロードが開始されます。  
![](https://wamisnet.github.io/pic/ren/pic102.png)
無事にダウンロードができれば次はインストールしていきます。
##インストール
Windows、Macとも少し画面構成は異なりますが、基本的には同じ流れでインストールしていきます。

###インストール
これからArduinoIDEのインストールを進めていきます。
ライセンス表示があるので問題なければ**I　Agree**をクリックして次に進みます。  
![](https://wamisnet.github.io/pic/ren/pic008.png)  
オプション設定をどのようにするのか選択できますが、このままで問題ないのでそのまま**Next**をクリックして次に進みます。  
![](https://wamisnet.github.io/pic/ren/pic009.png)  
インストール先を指定できますが、そのままで問題ないので**Next**をクリックして次に進みます。  
![](https://wamisnet.github.io/pic/ren/pic010.png)  
インストールが始まりますのでしばらくお待ちください。  
![](https://wamisnet.github.io/pic/ren/pic011.png)  
インストールが完了すると**Completed**と表示されたらインストール完了です！  
![](https://wamisnet.github.io/pic/ren/pic012.png)  

インストール完了したので次の作業に進みます！

##ArduinoIDEを触ってみよう
インストール完了するとデスクトップにこのようなアイコンができていると思います。
このアイコンをクリックしてArduinoIDEが起動させてください。  
![](https://wamisnet.github.io/pic/ren/pic014.png)  
クリックするとこのような画面が出てArduinoIDEの起動準備が始まりますのでしばらくお待ちください。  
![](https://wamisnet.github.io/pic/ren/pic013.png)  
このような画面が表示されると準備完了です。
この画面でNefryで動かすプログラムを書いていきます。
![](https://wamisnet.github.io/pic/ren/pic015.png)  
これでArduinoIDEのインストール完了です。お疲れ様でした。  
次はNefryボードのインストールをしていきます。
##Nefryを追加するための初期設定
ArduinoIDEにもともとNefryはインストールされていないので、ArduinoIDEでプログラムを書けるようにボードのインストール作業をしていきます。

それでは早速インストールしていきます。
ArduinoIDEのファイル内にある環境設定の項目を開きます。  
![](https://wamisnet.github.io/pic/ren/pic016.png)  
環境設定を開いて**追加のボードマネージャーのURL** に次のURL を入力します。

```
http://wamisnet.github.io/package_nefry_index.json
```

入力が終わったら OK をクリックします。  
![](https://wamisnet.github.io/pic/ren/pic017.png)  
入力が終わったら、ツール内にあるボード選択のボードマネージャーをクリックします。  
![](https://wamisnet.github.io/pic/ren/pic022.png)  
ボードマネージャーを開くとこのような画面が出てきます。
おそらくNefryが下の方に追加されていると思います。検索欄もあるのでそこに**Nefry**と入力するといいかもしれません。

もしNefryが見つからない場合、もう一度先ほどのURLを正しく入力できているか確認してください。
##Nefryを新規インストールする
現在(2016/7/26)の最新バージョン(1.4.0)のボードが選択されているので、そのままインストールをクリックしてください。  
![](https://wamisnet.github.io/pic/ren/pic019.png)  
必要なファイルをインターネットからダウンロードしています。回線状態によっては時間が掛かる場合があります、しばらくお待ちください。  
![](https://wamisnet.github.io/pic/ren/pic020.png)  
インストールが完了すると**INSRALLED**と表示されインストールが完了します。  
![](https://wamisnet.github.io/pic/ren/pic021.png)  
インストールが完了すると、ツール内にあるボードからNefryが選択できるようになっているはずです！  
![](https://wamisnet.github.io/pic/ren/pic023.png)  
これでボードのインストールも完了ですので、次はついにプログラムを書いていきます。
基本的にはここまでの設定は初回のみですので次回から使う時はプログラムを書くところから初めてもらうことができます。
##Nefryのライブラリを更新する
更新する場合、古いバージョンのボードが残っていると不具合が発生するので、先にアンインストールをします。

Nefryのボードを選択した時に**削除**というボタンがあるのでそこをクリックします。
そのまましばらく待つとアンインストールが完了します。
それから上に書いてある新規インストールの手順に従いボードのインストールをしてください。  
![](https://wamisnet.github.io/pic/ren/pic018.png)  


