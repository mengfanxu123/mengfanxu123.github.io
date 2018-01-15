---
layout:     post
title:      Javascript-- Prototype and Arrow functions
subtitle:   
date:       2017-12-7
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up

---
# introduction of Arrow function
## Description
shorter syntax than a functions of Javascript
suited for no=method functions and cannot be used as constructor

```Javascript

var materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];
//this is not use
materials.map(function(material) {
  return material.length;
}); // [8, 6, 7, 9]

materials.map((material) => {
  return material.length;
}); // [8, 6, 7, 9]

materials.map(material => material.length); // [8, 6, 7, 9]
```
1. if arrow use with method, it will show undefined
2. cannot use Prototype
3. cannot use yield keyword

## Function Body

1. two : concise body and block body

```Javascript
var func = x => x * x;                  
// concise body syntax, implied "return"

var func = (x, y) => { return x + y; };
// with block body, explicit "return" needed
```
2. return object literals cannot work

    params => {object:literal}

    {} can express to other languages,so use () it to

    ```Javascript
    var func = () => ({foo: 1});

     ```
3. cannot line breaks

## more example
```Javascript
let empty=()=>{};
var simple=a=>a>14? 14:a;
simple(16);//14
simple(10);//10

var arr = [5, 6, 13, 0, 1, 18, 23];

var sum=arr.reduce((a,b)=>a+b);
//66

var even = arr.filter(v => v % 2 == 0);
// concise promise chains

promise.then(a=>{

}).then(b=>{
  //more
});
```
# tips
