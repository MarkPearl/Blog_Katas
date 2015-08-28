---
layout: post
title: Sql Order Shippers Kata
tags: Useful
category: General
---

You have the following tables: Orders, Shippers and Employees. We want to know how many orders each shipper has shipped. Generate the query.

#### To create the initial table ####

~~~
create table Orders (
       OrderId int primary key,
       CustomerId int,
       EmployeeId int,
       OrderDate Date,
       ShipperId int)
 
create table Shippers (
       ShipperId int,
       ShipperName varchar(255),
       Phone text)
 
create table Employees (
       EmployeeId int primary key,
       LastName text,
       FirstName text,
       BirthDate Date,
       Photo text,
       Notes text)
 
Insert into Orders (OrderId, CustomerId, EmployeeId, OrderDate, ShipperId) values
    (10248, 90, 5, '1996-07-04', 3),
    (10249, 81, 6, '1996-07-05', 1),
       (10251, 82, 3, '1996-07-04', 1),
    (10250, 34, 4, '1996-07-08', 2)
 
Insert into Shippers (ShipperId, ShipperName, Phone) values
    (1, 'Speedy Express', '503 555 9831'),
    (2, 'United Package', '503 555 3199'),
    (3, 'Federal Shipping', '503 555 9931')
 
Insert into Employees (EmployeeId, LastName, FirstName, BirthDate, Photo, Notes) values
    (1, 'Davolio', 'Nancy', '1968-12-08', 'EmpID1.pic', 'Education includes a BA...'),
    (2, 'Fuller', 'Andrew', '1952-02-19', 'EmpID2.pic', 'Andres receiv3ed his BTS'),
    (3, 'Leverling', 'Janet', '1963-08-30', 'EmpID3.pic', 'Janet has a BS degreee...')
~~~

#### Cheat sheat ####

~~~
select Shippers.ShipperName, Count(Orders.OrderId) from Orders left join Shippers on Orders.ShipperId = Shippers.ShipperId group by ShipperName
~~~
