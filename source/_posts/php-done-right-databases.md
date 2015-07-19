
title: Databases
subtitle: "We have a thing (or two) to say about this."
date: 2014-10-15 09:26:10
tags:
categories:
    - codecademy
---
### One Database to rule them all...

In Coolblue we have a master Oracle Database, that runs all our processes. It´s being used mostly in Vanessa and all the new C# applications we´re creating every day. 

#### ...except when you have two.

But Coolblue has an exception for almost everything. And our databases are not... the exception. Well, basically, Our Oracle Database is the most important data storage we have in Coolblue, but we think it´s not advisable to use it **also** for web development. Simply put, there´s too much sensitive information there just to be able to access it. 

#### Coolsync.

So, for our web development, we´re using one MySQL master Database (for writes), along with 8 MySQL Slaves (for reads). The MySQL and Oracle databases are not directly connected to each other (how could that be, right?) but for a cool syncing script we decided to call CoolSync.

What CoolSync does is just to keep the MySQL databse up-to-date with the latest changes in Oracle, at least for those pieces of information we may need to access in the website. This syncing is done automatically every a couple of minutes and just moves the minimum amout of data that actually changed.
