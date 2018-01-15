---
layout:     post
title:      interview propare for BI
subtitle:   
date:       2017-12-1
author:     Mengfan
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - set up

---
50,000 shoppers with a 0.5% conversion rate for a chair that costs $250. Wayfair makes a 27% profit. Next, 50,000 shoppers will get a 10% discount. What is the conversion rate they must achieve to achieve the same profits as before?

* Your conversion rate is the percentage of visitors to your website that complete a desired goal (a conversion) out of the total number of visitors. A high conversion rate is indicative of successful marketing and web design: It means people want what you're offering, and they're easily able to get it!

* take care:
每个椅子的利润 profit 是一样的
所以 根据这个进行计算
profit=0.27X250=67.5
cost=250-67.5=182.5
50000x0.005*67.5=50000*(225-182.5)XC
C=0.79



* Wayfair is going to send 2 different catalogs to their  customers. One of the catalogs costs 50 cents to make and is 50 pages long. The conversion rate for the catalog is 5% and each customer brings in 315 dollars. The second catalog costs 95 cents to make, is 100 pages long and each customer brings in 300 dollars from it. The profit margin is 30%. What should the conversion rate for the second catalog be to make at least the same amount of profit as the first one.

* After you find the conversion rate for the second one, there is a second part of the problem. Wayfair is planning to make a new catalog which is going to cost 10 cents more than the 100 page one. The more expensive catalog is going to be sent out to 20% of the customers while the remaining 80% are going to get the 100 page one. Assume the same 30% profit margin and 300 dollar profit from each customer. What should the conversion rate for the new catalog be in order to receive the same profit at the end?

* <strong> profit 不变
假设有100人，
profit=100x.05X315X0.3-0.5X100
CX100X0.3X300-0.95X100
C=0.075

第二问：
保持利润不变：

profitX.2=0.2X100XC1X300-1.05X100X0.2
C1=0.586

 ## 准备：
 SQL:
 different union and union all:

 What is the difference between union and union all
what is the difference between left outer join and inner join

If we used to promote our products by small catalogs and we want to change to larger ones, how can we decide our target consumers

Given the former transaction rate, profit and cost, what will be the number of large catalogs if we want to create the same profit  

* Introduce yourself. Talk more about your project.  

They asked two question in the first case study. One was about if they get x amount of views on a website, y amount of people click on the ad, then z amount of people enter their names after ( x,y,z values are given. Gave a price of how much it cost to acquire a customer and a percentage on conversion rate and you were to calculate Would it make sense to run the campaign comparing the value of customer acquisition to the revenue gained from conversion rate. The other question was a reverse of this to find the conversion rate.  
