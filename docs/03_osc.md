# OSC

## OSCとは

OpenSound Control（OSC）とは、電子楽器（特にシンセサイザー）やコンピュータなどの機器において音楽演奏データをネットワーク経由でリアルタイムに共有するための通信プロトコルである。カリフォルニア大学バークレー校にある CNMAT（The Center for New Music and Audio Technologies）が開発した。([Wikipedia](https://ja.wikipedia.org/wiki/OpenSound_Control))

&nbsp;

対応アプリケーションは多数あり、リアルタイムに同期できる。

![](https://yonekura907.github.io/myMax/osc.png)


&nbsp;
&nbsp;
&nbsp;
&nbsp;

## OSCの設定

#### ネットワークアドレスの確認

![](https://yonekura907.github.io/myMax/ipadress.png)


#### OSCの送受信

* udpsend 送り先のIPアドレスとポート番号を指定

![](https://yonekura907.github.io/myMax/udp01.png)


* udpreceive 送信元のポート番号を指定

![](https://yonekura907.github.io/myMax/udp02.png)

* コンソール

```
replay9000 hello
```


&nbsp;
&nbsp;
&nbsp;
&nbsp;

## 複数の値を識別

/識別名　で複数の値を同時に送ることができる

&nbsp;

#### OSCの送受信

* udpsend prepend と /識別名で送信

![](https://yonekura907.github.io/myMax/udp03.png)

&nbsp;

* udpreceive route と /識別名で分岐

![](https://yonekura907.github.io/myMax/udp04.png)

&nbsp;
&nbsp;
&nbsp;
&nbsp;

## OSC事例
### loop

 * Arduinoで取得した値をProcessingにシリアル通信で送る
 * ProcessingからMaxに配列とカウンターを送り演奏

![](https://yonekura907.github.io/myMax/loop.png)

&nbsp;

[loop](https://youtu.be/-GrHyL2X94E)


