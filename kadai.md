## 練習問題
より実務よりの難しい問題集となっております。  
実行環境ですが結果が確認できればなんでも良いです。  
下記のpaiza ioはブラウザ上で実行できるのでおすすめです！  
https://paiza.io/ja/projects/new <br>  

<br>
### 問題01
$numArrayの各要素を2倍にした新しい配列を出力するプログラムを作成してください。
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


