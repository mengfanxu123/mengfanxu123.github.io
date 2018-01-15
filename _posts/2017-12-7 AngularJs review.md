---
layout:     post
title:      AngularJS Review
subtitle:   
date:       2017-12-7
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up
---
# introduction
AngularJS is a JavaScript framework. It can be added to an HTML page with a  tag.

AngularJS extends HTML attributes with Directives, and binds data to HTML with Expressions.

ng-app: define AngularJS application.<strong > one html file should only use one time

ng-model: binds the vaule of html controls

ng-bind: binds application data to html Review

```JavaScript
<div ng-app="myApp" ng-controller="myCtrl">

firstName: <input type="text" ng-model="firstName"><br>
lastName: <input type="text" ng-model="lastName"><br>
<br>
姓名: {{firstName + " " + lastName}}

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.firstName= "John";
    $scope.lastName= "Doe";
});
</script>



```
* angularjs Object

```JavaScript
<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">

<p>The name is {{ person.lastName }}</p>

</div>
//witch is same as ng-bind

<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">

<p>The name is <span ng-bind="person.lastName"></span></p>

</div>

```
## ng-model
将输入的值与js 绑定
two side binds

```JavaScript
<!DOCTYPE html>
<html>
<head>
<script src="http://cdn.static.runoob.com/libs/angular.js/1.4.6/angular.min.js"></script>
</head>
<body>
<div ng-app="myApp" ng-controller="myController">
name:<input ng-model="name">
<h1>you input:{{name}}</h1>
</div>
<script>
var app=angular.module('myApp',[]);
app.controller('myCtrl',function($scope){
  $scope.name="john Doe";
})
</script>
</body>
</html>
```
ng-dirty:布尔值属性，表示用户是否修改了表单。如果为 ture，表示有修改过；false 表示修没有修改过

### filter
currency Format a number to a currency format.<br>
date Format a date to a specified format.
currency Format a number to a currency format.<br>
filter Select a subset of items from an array.

json Format an object to a JSON string.
limitTo Limits an array/string, into a
 specified number of elements/characters.
lowercase Format a string to lower case.
number Format a number to a string.
orderBy Orders an array by an expression.
uppercase Format a string to upper case.

```JavaScript
<div ng-app="myApp" ng-controller="namesCtrl">

<ul>
  <li ng-repeat="x in names | filter : 'i'">
    {{ x }}
  </li>
</ul>

</div>

```
use http service to read json file

```JavaScript
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<script src="https://cdn.bootcss.com/angular.js/1.6.3/angular.min.js"></script>
</head>
<body>

<div ng-app="myApp" ng-controller="siteCtrl">

<ul>
  <li ng-repeat="x in names">
    {{ x.Name + ', ' + x.Country }}
  </li>
</ul>

</div>

<script>
var app = angular.module('myApp', []);

app.controller('siteCtrl', function($scope, $http) {
	$http({
		method: 'GET',
		url: 'http://www.runoob.com/try/angularjs/data/sites.php'
	}).then(function successCallback(response) {
			$scope.names = response.data.sites;
		}, function errorCallback(response) {
			// 请求失败执行代码
	});

});
</script>

</body>
</html>
```
### ng-option and ng-repeat
ng-option and ng-repeat has same function that Dropdowns made with ng-options allows the selected value to be an object, while dropdowns made from ng-repeat has to be a string.

* compare

```JavaScript
// use ng-repaeat
<select ng-model="selectedCar">
<option ng-repeat="x in cars" value="{{x.model}}">{{x.model}}</option>
</select>

<h1>You selected: {{selectedCar}}</h1>
//use ng-option
<select ng-model="selectedCar" ng-options="x.model for x in cars">
</select>

<h1>You selected: {{selectedCar.model}}</h1>
<p>Its color is: {{selectedCar.color}}</p>
```
* ng-disable 设置属性是disable的
### validate

```JavaScript
<input type="text" name="user" ng-model="user" require>
<span style="color:red" ng-show="myForm.user.$dirty&&myForm.user.invalid">
<span ng-show="myForm.user.$error,required">use must<span>

````

### include

    <div ng-include="'hello.html'">
    </div>
### ngAnimate

```JavaScript
<body ng-app="ngAnimate">

Hide the DIV: <input type="checkbox" ng-model="myCheck">

<div ng-hide="myCheck"></div>

</body>
Try it Yourself »

```
* example for ng-route

```JavaScript
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular-route.js"></script>

<body ng-app="myApp">

<p><a href="#/!">Main</a></p>

<a href="#!banana">Banana</a>
<a href="#!tomato">Tomato</a>

<p>Click on the links to change the content.</p>

<p>The HTML shown in the ng-view directive are written in the template property of the $routeProvider.when method.</p>

<div ng-view></div>

<script>
var app = angular.module("myApp", ["ngRoute"]);
app.config(function($routeProvider) {
    $routeProvider
    .when("/", {
        template : "<h1>Main</h1><p>Click on the links to change this content</p>"
    })
    .when("/banana", {
        template : "<h1>Banana</h1><p>Bananas contain around 75% water.</p>"
    })
    .when("/tomato", {
        template : "<h1>Tomato</h1><p>Tomatoes contain around 95% water.</p>"
    });
});
</script>

</body>
</html>
```
* example:
[shopping cart](./)
