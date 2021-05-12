## 練習問題（初級者向け）
---
一問一答形式の比較的な簡単な問題集となっております。  
実行環境ですが結果が確認できればなんでも良いです。  
下記のpaiza ioはブラウザ上で実行できるのでおすすめです！  
https://paiza.io/ja/projects/new <br>  

<br>


### 問題01
下記の変数を数値型->文字列型にしてください。  
（プログラミングでは型変換のことを"キャスト"と言います。）
```
$num = 1;
```

<details><summary>サンプルの答えを表示</summary><div>

```
$num = (string) $num;
```
</div></details><br>

### 問題02
整数値を入力させ、値が0ならzero、0でなければnot zeroと表示するプログラムを作成せよ。

<details><summary>サンプルの答えを表示</summary><div>
```
$num = 0;
if($num === 0) {
    echo 'zero';
} else {
    echo 'not zero';
}
```
</div></details>

### 問題03
整数値を入力させ、その値を絶対値にして表示するプログラムを作成せよ。

<details><summary>サンプルの答えを表示</summary><div>
```
$num = 0;
if($num < 0) {
    echo $num * -1;
} else {
    echo $num;
}
```
</div></details>

### 問題04
$a, $bの値を予測してください。

```
$a = 1;
$b = 1;

print 'aは' . ++$a;
print "\n";
print 'bは' . $b++;
```

<details><summary>サンプルの答えを表示</summary><div>

```
aは2
bは1
```
参考記事：https://wepicks.net/phpref-operators_increment/  

</div></details>

### 問題04
Hello World!を10回繰り返して表示するプログラムを作成せよ。

```
$greet = 'Hello World!';
for($i=0;$i<10;$i++) {
    echo $greet;
    echo "\n";
}
```

<details><summary>サンプルの答えを表示</summary><div>

```
aは2
bは1
```
参考記事：https://wepicks.net/phpref-operators_increment/  

</div></details>

### 問題05
$oldHouseから、太郎さん、次郎さんを$newHouseに移動させてください。

```
$oldHouse = ['太郎','次郎','三郎','四郎'];
$newHouse = [];
```

<details><summary>サンプルの答えを表示</summary><div>

```
aは2
bは1
```
</div></details>


### 問題02
下記の二つの配列を結合し、一つの配列として出力してください。
```
$strArray = ['A','B','C'];
$numArray = [1,2,3];
```

<details><summary>サンプルの答えを表示</summary><div>

```
$strArray = ['A','B','C'];
$numArray = [1,2,3];

$joinArray = array_merge($strArray, $numArray);
print_r($joinArray);
```
</div></details>