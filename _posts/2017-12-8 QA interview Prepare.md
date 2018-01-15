---
layout:     post
title:      prepare for QA interview
subtitle:   
date:       2017-12-1
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up

---
# first phone interview
### glassdoor question

1. very based on resume
2. javascript knowledge

### E-commerace Platform

this project is what i am doing now and have't finished yet.
this semester I have seleceted network structure and cloud computing
so I do this project during this whole semester.
: how to worte shell file  and cloudformation to  how to setting security group and policy to authorization and set up environment.
I also use shell file to automatic deploy the application to aws, EC2 instance(port 80)，

TravisCI: this is kind of  continuous integration service ,used to build and test software projects hosted at GitHub,
we wrote the .travis.yml(gradlew.war) and when we change the

trabisCI can find the root.war and before depoy, greate file and zip it to S3(in aws) and configure other .yml file to use it
<!-- travisCI 找到 Root.war zip to s3,
cloud play Root， aws 配置文件apppp,---， -->

How to do this one:


JMeter for Performance Testing of a RESTful API.

Request GET all uer, add many thread and show the Performance.

Request GET Post

and jmx file is automatic generate when we greate the spring boot applictions. and we should open it at jmeter and http request sample

most difficult:
I think this class is very challage for me, because i learn many amny new things and I konw that how to  profesinal deploy a appliction to aws, has many process, and we should take care every things,and configure every thing right.

during this project， I think how to deal with hard code is very deffiuclt things, when we wrote the cloudformation file, we know that every different uses havs different datbase password and database name ,how to solve this problem when we use cloudformation to automatic deploy the




### share payments.

this applictaion is very similar to vemon, very popular money payment application.

i use spring mvc as framework to develop it,

this applictaion has 3 parts,
front end: use css html javascript to design web page,

back end : use spring mvc to ontrol data flow, how to get date from front end page to store in database.

database design:
BankAccount, TransferData, UserAccount, AdminsterInfo four tables,

the most difficult one database design, table relationship design cost me long time, because every users can trnsform money to other uses, I think this is user table selfjoin many to many relationship. use spring annotion, it will automaict generate a  bridge table, connect it.

mvc：
he model is the central component of the pattern. It expresses the application's behavior in terms of the problem domain, independent of the user interface.[6] It directly manages the data, logic and rules of the application.
A view can be any output representation of information, such as a chart or a diagram. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.
The third part or section, the controller, accepts input and converts it to commands for the model or view.[7]

从你给的例子来看，查询的结果是model，显示的页面是view，在view中点击查询按钮后执行什么具体操作，以及查询结果model如何通过view展示则是control的功能。所有mvx的设计模式都是通过x实现model和view的解耦。在mvc中这个x是control。

作者：durow
链接：https://www.zhihu.com/question/27897315/answer/38593209
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

### Alternative Queue Management in Amusement Parks

I design a antroid application that user can use it to queue different rides online, they can save many times,

this proejct i use jfinal framework to make a develop, although this framework created by chinese people and it is very popular in china in 2016.



why i use this framwork:

this is also a kind of mvc framework
less code, simple to learn, powerful functionalities(easier to do validation and ), lightweight, easy of extend and Restful

* Convention over configuration, zero configuration, no XML
* MVC architecture, ingenious design, simple to use
Original Db + Record model,which is flexible and convenient

Support for Active Record pattern ,making database development ultimate fast.

Reloading modified java files automatically, with no need to restart web server during development process

Support for AOP , flexible configuration of interceptors ,powerful functionality

Plugin architecture with strong scalability

Support for multi-views ,such as FreeMarker, JSP, Velocity

Powerful Validator back-end verification

Complete functionality with most features of struts2

Small size ,only 248K ,without any third-party dependence

Baidu map API:
bacause done this proeject in china, so I use baidu map Api to do nevigation and android SDK to write it

when you mobile phone open the GPS, Baidu API can do nevigation to the ride's locations

NFC: if you open the NFC function in a antroid phone, in this project, extand and interface , when you device close to the NFC chip，chips will detect signal， the app will show that if they detect it , it will show you have payed. this is not a really pay functions, just a prototype. can dispaly NFC technology extends a interface.

check password,





when you click apply on the line, they will begin to caculate the time you should waiting, if other people use it, to apply, maybe you are the 5th people, you should  waiting for 4min*5, 20 mins, when the 20mins run out of , it's to you.

Baidu API and SDK to complete the navigation function.

### discount:  this is recommend,


### Car Park Control System
this project our teams used agile method to manage this project.

three phases in scrum :
first outline planing: every team member must design project the backlog and plan the scrum meeting

Black box test done in component level and system level.
Park System, Management system and staff information system.

* Black box test we just try it Park systems, Manage system and staff system weather can use

component level test we just design the different test cases to test it function.

for example, we just design test case to test admintration login function.

one test case for correct password to login

one test case for incorrect passoword to login

but all this test case just wrote in eclipse and not the automatic test.

this project we don't use the database, we just use the txt file to read, write and save file.

Behavioral Testing, is a software testing method in which the internal structure/ design/ implementation of the item being tested is not known to the tester.
 for example： click this button and know wheather this function is good  


 unit test
 if the password is not right, can I login,


### how to test video player.
1. first you can do a unit test to test different function
2. Manual test:


  load video player in browser, whether can show all the detail,
  such as you can click play pause /pɔz/ button to paly and stop the video,

  and pause a video and go to full screen and show the video whetehr go full screen.

  Time elapsed in watching the video should be shown on the left hand side of the end-user beside the progress bar

  volume can control

  change the different web browse and show this vido player's performance

Check if the buffering is being done while the video is paused
While buffering, loading component in clockwise direction should be shown between elapsed time component and progress bar

although I don't test it , but i realize that you can use automatic test tool to compete the performance test and stress test, such as Selenium /sə'linɪəm/  tool.
