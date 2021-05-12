## 練習問題
より実務よりの難しい問題集となっております。  
実行環境ですが結果が確認できればなんでも良いです。  
下記のpaiza ioはブラウザ上で実行できるのでおすすめです！  
https://paiza.io/ja/projects/new <br>  

<br>

### 問題01
$numArrayの各要素を2倍にした$doubleArrayを出力するプログラムを作成してください。

```
$numArray = [1,2,3,4,5];
```

<details><summary>サンプルの答えを表示</summary><div>

```
$doubleArray = array();
foreach($numArray as $num) {
    $doubledNum = $num * 2;
    array_push($doubleArray, $doubledNum);
}
print_r($doubleArray);
```
</div></details><br>

### 問題02
1~100までの配列を用意し、偶数のみ取り出す関数を作成してください。

<details><summary>サンプルの答えを表示</summary><div>

```
$numArray = range(1,100);
$evenNumArray = array();
foreach($numArray as $num) {
    if($num % 2 === 0) {
        array_push($evenNumArray, $num);
    }
}
print_r($evenNumArray);
```
</div></details><br>

### 問題03
$numに整数値をセットし、その値が偶数ならばeven、奇数ならばoddと表示するプログラムを作成せよ。  
0もしくは負の数がセットされた場合は、'正の数で入力してください' と出力してください。

<details><summary>サンプルの答えを表示</summary><div>

```
$num = N;
if ($num < 1) {
    echo '正の数で入力してください';
} elseif ($num % 2 === 0) {
    echo 'even';
} else {
    echo 'odd';
}
```
</div></details><br>

### 問題03
$numArray配列に数値をセットし、それが小さい順に並んでいればOK、そうなっていない場合はNGと出力するプログラムを作成してください

<details><summary>サンプルの答えを表示</summary><div>

```
$numArray = [];

```
</div></details><br>

### 問題03
1~100までの配列を用意し、素数のみ格納した新しい配列を作成してください。

<details><summary>サンプルの答えを表示</summary><div>

```
$numArray = range(1,100);
$primeArray = array();
foreach($numArray as $num) {
    if($num === 1 || $num === 2) {
        continue;
    }
    $flg = true;
    for($i=2;$i<$num;$i++) {
        if($num % $i == 0) {
            $flg = false;
            break;
        }
    }
    if ($flg) {
        array_push($primeArray,$num);
    } 
}
print_r($primeArray);
```
</div></details><br>

### 問題04（評価式or）
下記の出力結果を予想してください  
引用：https://qiita.com/yamamoto_hiroya/items/ea050a8347f4a2a3e75e
```
function trueFn(){
    echo "trueFn関数が実行されました\n";
    return true;
}
function falseFn(){
    echo "return_false関数が実行されました\n";
    return false;
}

if(trueFn() || falseFn()){
    echo "trueです\n";
} else {
    echo "falseです\n";
}
```
<details><summary>サンプルの答えを表示</summary><div>

```
trueFn関数が実行されました
trueです

// --------------------
// foo() は決してコールされることはありません。これらの演算子は短絡評価を行うからです。

$a = (false && foo());
$b = (true  || foo());
```
</div></details><br>


### 問題05（評価式and）
下記の出力結果を予想してください。
```
function trueFn(){
    echo "trueFn関数が実行されました\n";
    return true;
}
function falseFn(){
    echo "return_false関数が実行されました\n";
    return false;
}

if(falseFn() && trueFn()){
    echo "trueです\n";
} else {
    echo "falseです\n";
}
```
<details><summary>サンプルの答えを表示</summary><div>

```
falseFn関数が実行されました
falseです

// --------------------
// foo() は決してコールされることはありません。これらの演算子は短絡評価を行うからです。

$a = (false && foo());
$b = (true  || foo());
```
</div></details><br>

### 問題06
以下のコードの出力を答えよ  
引用：https://qiita.com/yamamoto_hiroya/items/ea050a8347f4a2a3e75e
```
$test1 = '';
if(!!$test1){
    echo "test1: 評価式はtrueでした\n";
} else {
    echo "test1: 評価式はfalseでした\n";
}

$test2 = 'test';
if(!!$test2){
    echo "test2: 評価式はtrueでした\n";
} else {
    echo "test2: 評価式はfalseでした\n";
}
```
<details><summary>サンプルの答えを表示</summary><div>

```
test1: 評価式はfalseでした
test2: 評価式はtrueでした
```
</div></details><br>


### 問題07
以下の文字列から正規表現を用いて数値のみを取り出してください。
```
'beenos2021新卒'
```
<details><summary>サンプルの答えを表示</summary><div>

```
$string = 'beenos2021新卒';

$num = preg_replace('/[^0-9]/', '', $string);
```
</div></details><br>

### 問題08 
$zipCodeに値が正しく入っている場合はtrue 正しくない場合はfalseを返却してください。  
正しい郵便番号の形は NNN-NNNN （Nは数字）とする。  
preg_match関数を使用してください

<details><summary>サンプルの答えを表示</summary><div>

```
$zipCode = '111-1111';
function checkZip($zipCode) {
 if(preg_match('/^[0-9][0-9][0-9][-][0-9][0-9][0-9][0-9]$/', $zipCode)) {
     return true;
 }
 return false;
 }
}
```
</div></details><br>

### 問題09
初乗り料金が1700mまで610円、それ以降は313mごとに80円のタクシーがある。  
このタクシーに乗った距離をm単位で入力し、料金を計算するプログラムを作成せよ。

<details><summary>サンプルの答えを表示</summary><div>

```
$dist = ; //距離を入力
$price = 0;
if($dist <= 1700) {
    $price = 610;
} else {
    $overDist = $dist - 1700; #延長距離の算出
    $a = $overDist / 313; #
    $b = ceil($a); #繰り上げ
    $price = 610 + (80 * $b);
}
```
</div></details><br>

### 問題10
BEENOS美術館の入場料金は、一人600円であるが、5人以上のグループなら一人550円、20人以上の団体なら一人500円である。  
人数を入力し、入場料の合計を計算するプログラムを作成せよ。

<details><summary>サンプルの答えを表示</summary><div>

```
$memberCount = ;
$price = 0;
if ($memberCount >= 20) {
    $price = 500 * $memberCount;
} elseif ($memberCount >= 5) {
    $price = 550 * $memberCount;
} else {
    $price = 600 * $memberCount;
}
```
</div></details><br>

### 問題11
1から100までの値を繰り返しで表示するが、3の倍数の時はfizz、5の倍数の時はbuzzと数字の代わりに表示するプログラムを作成せよ。  
なお、3と5の両方の倍数の時はfizzbuzzと表示される。

<details><summary>サンプルの答えを表示</summary><div>

```
for($i = 1; $i <= 100; $i++){    //1から100までループ
    if($i % 15 == 0){
        print "FizzBuzz";
    }else if($i % 3 == 0){
        print "Fizz";

    }else if($i % 5 == 0){
        print "Buzz";
    }else{
        print $i;
    }
    print "　";
}
```
</div></details><br>