---
layout:     post
title:      PHP review
subtitle:   
date:       2017-12-7
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up

---
# php introduction
PHP is an acronym for "PHP: Hypertext Preprocessor"  <br>
PHP is a widely-used, open source scripting language<br>
PHP scripts are executed on the server<br>
PHP is free to download and use
# syntax
```PHP
<!DOCTYPE html>
<html>
<body>

<h1>My first PHP page</h1>

<?php
echo "Hello World!";
?>

</body>
</html>

```
## varible
$x=a(start with letter and undersocre )

## display

```PHP
<?PHP
$txt="love code"
echo "I love code $txt !"

?>
//same as
<?PHP
$txt="love code"
echo "I love code" .$txt ."!"

?>
```
static
: keep virable remain ,we need use it for futhure work

```PHP
<?php
function myTest()
{
 static $x=0;
 echo $x;
 $x++;
}

myTest();
myTest();
myTest();
?>
```
* echo no return value, take multiple parameters and it is fast

* print has return value of one

String<br>
* length strlen("hello php")
8
* the numbers of words
```PHP
<?php
echo str_word_count("Hello world!"); // outputs 2
?>t
```
Integer
Float (floating point numbers - also called double)
Boolean
Array $cars=array("a","b","c");
Object
NULL
Resource

## PHP constant
define(name, value, case-insensitive)
## calculate
```PHP
<?php
$a = "Hello";
$b = $a . " world!";
echo $b; // 输出Hello world!

$x="Hello";
$x .= " world!";
echo $x; // 输出Hello world!
?>
```
其他都一样
* === value and type must same
combined comparison operator
$c = $a <=> $b;<br>
if a=b c=0 <br>
if a>b c=1
if a<b c=-1

## Array

```PHP

$cars=new Array("1","2,"3");
$length=count(cars);
$age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");

```
print traverse is same
### superglobal

$GLOBALS


```PHP
<?php
$q=isset($_GET['q'])?htmlsepcialchars($_GET('q')):'';
if($q){
  if($q=='a'){
    echo 'a';
  }else if($q=='b'){
    echo 'b';
  }else if($q=='c'){
    echo 'c'
  }else{
    ?><form action=" " method="get">
    <input type="radio" name="q" value="a"/>a
    <input type="radio" name="q" value="b"/>b
    <input type="radio" name="q" value="c" />c
    <input type="submit" value="submit">
  }
}

?>
```
<strong>get all user can see, this method is not security</strong>
can show in url
### validate
```PHP
<?php
$name = test_input($_POST["name"]);
if (!preg_match("/^[a-zA-Z ]*$/",$name)) {
  $nameErr = "Only letters and white space allowed";
}

$email = test_input($_POST["email"]);
if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
  $emailErr = "Invalid email format";
}
?>
```
### include
```PHP
<?php
include 'vars.php';
echo "I have a $color $car"; // I have a red BMW
// use include to get previous vars.php and use it
?>
```
* load csv file

```PHP
<?php
$fh=fopen("a.csv","r");//这里我们只是读取数据，所以采用只读打开文件流
$arr=fgetcsv($fh);//这个函数就是读取CSV文件的函数，他把文本读入后转为数组存储在$arr中
fcloase($fh);
foreach($arr as $key=>$value){echo $value;}//循环输出所有的值



?>
```

### quiz
* The PHP syntax is most similar to:

Perl and C

* What is a correct way to add a comment in PHP?

/*…*/

* PHP can be run on Microsoft Windows IIS(Internet Information Server):

true

* The if statement is used to execute some code only if a specified condition is true

You answered:true
