---
layout: post
title: Soccer Challenge
tags: Useful
category: General
---

#### Soccer Challenge ####

Write an application that will use the information in the two files to display the soccer clubs that correspond to a set of comma-delimited country codes that the user enters. You need to create the two files from the Country (country.csv) and Soccer Clubs (clubs.csv) sample data below.

##### Country Sample Data #####

~~~
South Africa, ZA
Brazil, BR
United Kingdom, UK
~~~

##### Soccer Clubs Sample Data #####

~~~
Pirates, ZA
Sundowns, ZA
Chiefs, ZA
Coruripe, BR
Commercial, BR
Man Utd, UK
Chelsea, UK
~~~

##### Example 1 #####

For example:

When the suer enters the comma-delimited set of codes "ZA,BR", the program will display all the clubs corresonding to both South Africa and Brazil.

~~~
Pirates
Sundowns
Chiefs
Coruripe
Comercial
~~~

If there are no clubs that correspond to the country codes entered, the program will display **No Results**.  


##### Things to note #####
1. The order of the results is not important.  
2. You can assume that the comma-delimited list of country codes entered by the user never contains whitespace, and that the country codes entered are always upper case.  
3. You can assume that Countries.txt will never contain any repeats of country names and codes.
4. You can assume that Clubs.txt file will never contain any repats of club names.  
5. You can assume that both text files will always be encoded as US-ASCII;  
6. Your implementation doesn't need to worry about performance.  
