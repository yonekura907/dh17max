# MSP

## 音と周波数

![](https://yonekura907.github.io/myMax/freq.png)

&nbsp;
&nbsp;
&nbsp;

## MIDI

* ノートオン/ノートオフ
	* 音を鳴らす/音を止める
	
* ベロシティ
	* 鍵盤を叩くスピート、音の強さ
	
* ノートナンバー
	
![](https://yonekura907.github.io/myMax/notenumber.jpg)


&nbsp;
&nbsp;
&nbsp;
&nbsp;


## シンセサイザー

### Oscillator


![](https://yonekura907.github.io/myMax/oscillator.png)

* cycle~ サイン波
* phasor~ ノコギリ波
* tri~ 三角波
* train~ 矩形波


&nbsp;
&nbsp;

### mtof 

Midiから周波数に変換するオブジェクト

![](https://yonekura907.github.io/myMax/mtof.png)

&nbsp;
&nbsp;


### meter~

シグナルを-1から1までの範囲内でモニターする

![](https://yonekura907.github.io/myMax/meter.png)

&nbsp;
&nbsp;

### line~

補完

<!--![](https://yonekura907.github.io/myMax/line.png)

```

```-->



&nbsp;
&nbsp;


### Envelope

![](https://yonekura907.github.io/myMax/envelope.png)


&nbsp;
&nbsp;
&nbsp;
&nbsp;


## 外部音源の取り込み

### sfplay~

HDの音源を取り込んで再生する

![](https://yonekura907.github.io/myMax/sfplay.png)

* open ファイルを開く
* start 再生
* loop 繰り返し
* pause 停止
* resume 再生
* seek 特定時間から再生



&nbsp;
&nbsp;


### play~

バッファーを使い音源を記録してから再生する

![](https://yonekura907.github.io/myMax/play.png)

* read ファイルを開く
* buffer~ バッファー
* loop 繰り返し
* start 再生
* pause 停止

