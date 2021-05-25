## 練習問題
より実務よりの難しい問題集となっております。  
実行環境ですが結果が確認できればなんでも良いです。  
下記のpaiza ioはブラウザ上で実行できるのでおすすめです！  
https://paiza.io/ja/projects/new <br>  

<br>

### 問題01
文字列が全て平仮名の場合、「全てひらがなです。」と返すプログラムを作成してください  
preg_match関数を使用してください

<details><summary>サンプルの答えを表示</summary><div>

```
$str = 'あいうえおかきくけこ';
if(!preg_match('/[^ぁ-んー]/u',$str)) { 
    echo '全てひらがなです。';
}
```
</div></details><br>

### 問題02
urlのプロトコルがhttpで渡ってきた場合、httpsに変換するプログラムを作成してください
```
$url = 'http://example.com';  

->https://example.com
```

<details><summary>サンプルの答えを表示</summary><div>

```
$url = 'http://example.com';
$protcol = parse_url($url, PHP_URL_SCHEME);
if($protcol === 'http') {
    $url = str_replace("http","https",$url);
}
echo $url;
```
</div></details><br>

### 問題03
本日の曜日を漢字で返すプログラムを作成してください  
さらに週末の場合、「weekend!!」と出力してください

<details><summary>サンプルの答えを表示</summary><div>

```
$week = array('日', '月', '火', '水', '木', '金', '土');
$w = date('w');
echo $week[$w];
if($w === 0 || $w === 6) {
    echo "\n";
    echo 'weekend!!';
}
```
</div></details><br>

### 問題04
自分が生まれてから何日経っているか確認するプログラムを作成してください

<details><summary>サンプルの答えを表示</summary><div>

```
$today    = date("Y-m-d");
$birthday = '1996-12-09';
$day1 = new DateTime($today);
$day2 = new DateTime($birthday);
 
$interval = $day1->diff($day2);
 
echo $interval->format('%a日');
```
</div></details><br>

### 問題05
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

### 問題06
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

### 問題07
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

### 問題08
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

### 問題09
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

### 問題10
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