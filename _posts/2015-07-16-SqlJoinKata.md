---
layout: post
title: Sql Join Kata
tags: Useful
category: General
---
This kata was inspired by the join series found [here](http://www.sqlteam.com/article/how-to-use-group-by-in-sql-server)  

Given the above data,

#### Part 1 ####

For each Customer, we want to return the total number of orders, the number of items ordered, the total order amount, and the total shipping cost.

Customer | ItemCount | OrderAmount | OrderCount
---------|-----------|-------------|-----------
ABC	     | 6	     | 725.00	   | 3
DEF	     | 3         | 475.00	   | 2

#### Part 2 ####

Now, display the total shipping cost per customer.

Customer | customerName	     | City	          | STATE | OrderCount | ShippingTotal | ItemCount | OrderAmount 
---------|-------------------|----------------|-------|------------|---------------|-----------|-------------
ABC      | ABC Corporation   |	Boston        | MA	  | 3          | 95.00         | 6	       | 725.00      
DEF      | The DEF Foundation	New York City |	NY	  | 2	       | 20.00	       | 3	       | 475.00

Code to create the data...

~~~
CREATE TABLE Orders (
	OrderID INT PRIMARY KEY
	,Customer VARCHAR(10)
	,OrderDate DATETIME
	,ShippingCost MONEY
	)

CREATE TABLE OrderDetails (
	DetailID INT PRIMARY KEY
	,OrderID INT REFERENCES Orders(OrderID)
	,Item VARCHAR(10)
	,Amount MONEY
	) 

CREATE TABLE Customers (
	Customer VARCHAR(10) PRIMARY KEY
	,CustomerName VARCHAR(100) NOT NULL
	,City VARCHAR(100) NOT NULL
	,STATE VARCHAR(2) NOT NULL
	)

go


INSERT INTO Orders  
select 1,'ABC', '2007-01-01', 40 union all 
select 2,'ABC', '2007-01-02', 30 union all 
select 3,'ABC', '2007-01-03', 25 union all 
select 4,'DEF', '2007-01-02', 10 union all
select 5,'DEF', '2007-01-04' ,10


insert into OrderDetails 
select 1, 1, 'Item A', 100 union all 
select 2, 1, 'Item B', 150 union all 
select 3, 2, 'Item C', 125 union all 
select 4, 2, 'Item B', 50 union all 
select 5, 2, 'Item H', 200 union all 
select 6, 3, 'Item X', 100 union all 
select 7, 4, 'Item Y', 50 union all 
select 8, 4, 'Item Z', 300 union all
select 9 ,5 ,'Item J', 125

INSERT INTO Customers 
SELECT 'ABC' ,'ABC Corporation' ,'Boston' ,'MA' UNION ALL 
SELECT 'DEF' ,'The DEF Foundation' ,'New York City' ,'NY'
~~~
