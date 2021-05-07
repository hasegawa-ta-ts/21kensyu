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
下記の二つの変数を使用し、"Hello, Tom" と出力してください。
```
$greet = 'Hello';
$name = 'Tom';
```

<details><summary>サンプルの答えを表示</summary><div>

```
echo $greet . ', ' . $name;
```
</div></details><br>

### 問題03
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

### 問題04
下記の変数はそれぞれどのように表示されるか想像してください

```
$a = 'こんにちは';
print '$a';
print "$a";
print "みなさん、$a"
```

<details><summary>サンプルの答えを表示</summary><div>

```
$a
こんにちは
みなさん、こんにちは

※3つめのprint文に関してですが、変数の直後に文字を入れるとエラーが起こってしまいます。  
（変数がどこまでかがPHPエンジンが分からなくなってしまうため)  


```
</div></details>

### 問題04
消費税（tax）の定数を作成してください。（税率は10%でお願いします。）


<details><summary>サンプルの答えを表示</summary><div>

```
const Tax = 1.1;
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
</div></details>



### 問題04
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
