---
layout:     post
title:      TypeScript
subtitle:   
date:       2017-12-7
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up

---
# introduction

let isDone: boolneea=false;
let why:number=6;
let st:string="mandy";
let list: number[] =[1,2,3];

var can use in loop for
but let cannot be use outside the loop for
and cannot duplicate defination
* const numLivesForCat = 9; value cannot change

### class

protected : can use in children class

#### for loop

```javascript
var j:any;
var n:any = "a b c"

for(j in n) {
   console.log(n[j])  
}
```
* special lambda function


```javascript
var foo = (x:number)=>10 + x
console.log(foo(100))      //outputs 110


var alphas:string[];
alphas = ["1","2","3","4"]
console.log(alphas[0]);
console.log(alphas[1]);
```
union

    ar val:string|number
    val = 12
    console.log("numeric value of val "+val)
    val = "This is a string"
    console.log("string value of val "+val)

interface

```javascript
interface IPerson {
   firstName:string,
   lastName:string,
   sayHi: ()=>string
}

var customer:IPerson = {
   firstName:"Tom",
   lastName:"Hanks",
   sayHi: ():string =>{return "Hi there"}
}

console.log("Customer Object ")
console.log(customer.firstName)
console.log(customer.lastName)
console.log(customer.sayHi())  

var employee:IPerson = {
   firstName:"Jim",
   lastName:"Blakes",
   sayHi: ():string =>{return "Hello!!!"}
}

console.log("Employee  Object ")
console.log(employee.firstName) console.log(employee.lastName)


```

declare class

```javascript
class Car {
   //field
   engine:string;

   //constructor
   constructor(engine:string) {
      this.engine = engine
   }  

   //function
   disp():void {
      console.log("Engine is  :   "+this.engine)
   }

   //create an object
var obj = new Car("XXSY1")

//access the field
console.log("Reading attribute value Engine as :  "+obj.engine)  

//access the function
obj.disp()
}
```
extands

```javascript
class Root {
   str:string;
}

class Child extends Root {}
class Leaf extends Child {} //indirectly inherits from Root by virtue of inheritance  

var obj = new Leaf();
obj.str ="hello"
console.log(obj.str)

// static

class StaticMem {  
   static num:number;

   static disp():void {
      console.log("The value of num is"+ StaticMem.num)
   }
}

StaticMem.num = 12     // initialize the static variable
StaticMem.disp()

//basic
class greeting{
  greet():void{
    console.log("ts");
  }
  let obj=new Greeting();
  obj.greet();
}

```
