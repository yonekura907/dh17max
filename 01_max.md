# Maxプログラミング
## プログラミングの流れ

インレットからアウトレットへ上から下へ値が送られていく

![](https://yonekura907.github.io/myMax/basic01.png)

&nbsp;

### bang プログラミングの流れ
メッセージや値を押し出す。弾丸の様な役割

![](https://yonekura907.github.io/myMax/bang.png)
 
&nbsp;
&nbsp;
&nbsp;

## オブジェクトボックス

###  インレット/アウトレット

オブジェクトにはインレット（受信側）とアウトレット（送信側）がある。
アウトレットからインレットで繋いでプログラミングを形成していく。


![](https://yonekura907.github.io/myMax/inletoutlet.png)


### アーギュメント
引数の役割をする。オブジェクトの第2インレットで値を上書きできる

![](https://yonekura907.github.io/myMax/basic02.png)
![](https://yonekura907.github.io/myMax/arg01.png)

&nbsp;
&nbsp;
&nbsp;



## インターフィエイス

&nbsp;
&nbsp;
&nbsp;

### button
Bangを出力する
[B]

![](https://yonekura907.github.io/myMax/button.png)

&nbsp;

### toggle
オンとオフ（0と1）で切り替える
[T]

![](https://yonekura907.github.io/myMax/toggle.png)

&nbsp;

### number
整数の数値。int型
[I]

![](https://yonekura907.github.io/myMax/number.png)

&nbsp;

### float
小数点以下を含む数値。float型
[F]

![](https://yonekura907.github.io/myMax/float.png)

&nbsp;
&nbsp;
&nbsp;
&nbsp;


#### int型とfloat型の型変換

![](https://yonekura907.github.io/myMax/cast.png)


&nbsp;
&nbsp;

## メッセージボックス

メッセージボックスの種類

### 値の受け渡し / マウスでオブジェクト自身をクリック

![](https://yonekura907.github.io/myMax/message01.png)

&nbsp;
&nbsp;

### bangメッセージ

![](https://yonekura907.github.io/myMax/message02.png)

&nbsp;
&nbsp;

### メッセージボックスの変数の受け渡し


「$1」という表記を使い「$」が変数を表し、後につづく番号で値を保存管理する。

* int(整数)
* float(実数)
* list(リスト)
* bang
* symbol(文字列)
* message

&nbsp;
&nbsp;

![](https://yonekura907.github.io/myMax/message03.png)

メッセージボックスは右インレットに値を受け取るとボックス内に表示される。


&nbsp;
&nbsp;

#### set

setは、出力は行わずに、 メッセージ ・ボックス の内容を新しいメッセージに設定します。 set メッセージだけであれば、 メッセージ ・ボックスの内容を消去します。

![](https://yonekura907.github.io/myMax/set01.png)


&nbsp;
&nbsp;

#### list

アーギュメントに $ と番号が含まれている場合は、一致する番号の$アーギュメントを、リストのそれぞれの項目に置き換えた上で、 メッセージ ・ボックスの内容を出力します。
第4インレット：出力せず メッセージ ・ボックスの内容を設定します。

![](https://yonekura907.github.io/myMax/list01.png)



&nbsp;
&nbsp;
&nbsp;
&nbsp;

## メソッド



### metro

ミリ秒でBangを出力する

![](https://yonekura907.github.io/myMax/metro.png)

&nbsp;
&nbsp;


### pak/unpack
* pack (pak) 受け取った値からリストを作る
* unpack リストから値を取り出す

![](https://yonekura907.github.io/myMax/pack01.png)



&nbsp;

### random / urn / drunk / decide
* random ランダムな数値
* urn 重複しないランダム数値
* drunk 直前の値を基準に増減する数値
* decide 0か1のランダム数値


![](https://yonekura907.github.io/myMax/random01.png)



&nbsp;

### expr
演算子や関数を記述することができる


![](https://yonekura907.github.io/myMax/expr01.png)


&nbsp;

### vexpr
リストの演算子や関数を記述することができる


![](https://yonekura907.github.io/myMax/vexpr01.png)


&nbsp;

### loadbang / loadmess
* loadbang
	* パッチを立ち上げた時にbangする
* loadmess
	* パッチを立ち上げた時にアーギュメントをbangする

![](https://yonekura907.github.io/myMax/loadbang01.png)


&nbsp;

### counter
カウンタ

* アーギュメント
	1. 増減の方向 (0なら増加、1なら減少、2なら増減)
	2. 最小値
	3. 最大値


![](https://yonekura907.github.io/myMax/counter01.png)


&nbsp;



### Ggate / gate
メッセージの流れを制御する

* アーギュメント
	1. 出力 (0なら閉じた状態、1なら第1インレットから出力、2なら第2インレットから出力)
	2. 最小値
	3. 最大値


![](https://yonekura907.github.io/myMax/gate01.png)


&nbsp;
&nbsp;



### 条件分岐


![](https://yonekura907.github.io/myMax/if01.png)


&nbsp;
&nbsp;


### if

条件式

```
if 条件式 then 出力1
if 条件式 then 出力1 else 出力2
```

* int型 $i1
* float型 $f1
* symbol $s1

![](https://yonekura907.github.io/myMax/if02.png)


&nbsp;
&nbsp;



### select

入力されたメッセージがアーギュメントに一致するかどうか調べる。
アーギュメント1が第1アウトレット、アーギュメント2が第2アウトレットへ流れていき、
いずれにも該当しない場合は最後のアウトレットに流れる。

![](https://yonekura907.github.io/myMax/select01.png)


&nbsp;
&nbsp;


### scale

値を出力の範囲にマッピングする

![](https://yonekura907.github.io/myMax/scale.png)


&nbsp;
&nbsp;
&nbsp;
&nbsp;



## Right to Left Order

右側のインレットから先にBangされる

![](https://yonekura907.github.io/myMax/righttoleft.png)

&nbsp;
&nbsp;

右に配置したものから先にBangされる

![](https://yonekura907.github.io/myMax/righttoleft2.png)


&nbsp;
&nbsp;

#### Bottom to Top Order

同じ位置なら下のものから先にBangされる

![](https://yonekura907.github.io/myMax/bottomtotop.png)


&nbsp;
&nbsp;


### trigger 

位置に依存されずBangを出力する。ただし右から順番に出力される

![](https://yonekura907.github.io/myMax/trigger.png)