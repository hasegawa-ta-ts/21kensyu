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
if(!preg_match('/[^ぁ-ん]/u',$str)) { 
    echo '全てひらがなです。';
}

/*
    
   [^...] = 角括弧に含まれる文字以外にマッチします(trueを返す）。
    
    上の例の場合、平仮名以外でマッチすると、preg_matchでtrueを返し、
    !で反転するのでfalseを返します。つまり、trueの場合の処理は行われません。
    
    逆に、平仮名以外ににマッチしない （＝全て平仮名の場合） と、falseを返します。
    そして、!で結果が反転するので、trueを返します。つまり、trueの処理が行われます。
    
*/
  
元の例だと、すごく分かりづらいのでこっちの方が良いですね。。
    
$str = 'あいうえおかきくけこ';
if(preg_match('/[^ぁ-ん]/u',$str)) { 
    echo '全てひらがなではありません';
} else {
    echo '全てひらがなです。';
}
    
また、下記の表現の方が分かりやすいですね。

if(preg_match('/^[ぁ-ん]+$/u', $str)){
 　echo '全て平仮名です';
}
    
/*
    
    
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
$result = false;
if(preg_match('/^[0-9][0-9][0-9][-][0-9][0-9][0-9][0-9]$/', $zipCode)) {
    $result = true;
}
var_dump()($result);

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
バブルソートを行う関数を作成してください。  

<details><summary>サンプルの答えを表示</summary><div>

```

```
</div></details><br>

### 問題10
nameのみ入れた、$nameArrayを作成してください。  
多次元連想配列は結構扱う機会があるので、いくつか練習問題を解くことをお勧めします。
```
$members = [
  ['name' => 'Tom', 'age' => 30, 'country' => 'USA'],
  ['name' => 'John', 'age' => 25,'country' => 'UK'],
  ['name' => 'Marry', 'age' => 22,'country' => 'Canada']
];
```

<details><summary>サンプルの答えを表示</summary><div>

```
$nameArray = array();
foreach($members as $member) {
    $nameArray[] = $member['name'];
}
var_dump($nameArray);
```
</div></details><br>
