---
layout: post
title: General Developer Challenge
tags: Useful
category: General
---

#### General ####

- Level of difficulty : Easy

#### Constraints ####

- You have one hour to complete the challenge  
- The challenge consists of 3 questions.  
- The intention of the challenge is not to test specific AP{Is or class libraries  

----------------------------------------------------------------------------------

#### Question 1 - Matrix Challenge ####

- Write a console application to display a square matrix of zeros and ones.  
- The matrix should be all zeros, except for the top-left to bottom-right diagonal which should be ones.  
- The program should prompt the user for the size of the matrix to display.  
- The matrix will be square.  
- Do not worry about handling invalid input.  

~~~
100000  
010000  
001000  
000100  
000010  
000001  
~~~
----------------------------------------------------------------------------------

#### Question 2 - Ancestors ####

- An ancestral relationship can exist between two people, a parent a child.  
- Given a set of parent-child relationships entered by a user, write a program that will display the ancestral line, given a particular person.  
- The parent-child relationships should be entered as a comma-delimited string, with each relationship being represented by the convention shown in the example.  
- When outputing ancestral lines, they are displayed in order from the most distant ancestor to the least distant ancestor.  
- If a user wants to see ancestors for a person who doesn't have any ancestors, the program should indicate this with the message 'No ancestors'.

##### Example 1 #####

We could say Martha is Roberts parent, and Robert is Martha's child by using the following convention to to indicate the relationship.

~~~
Martha<-Robert
~~~

##### Example 2 #####

Given the following parent-child relationships.

~~~
Claudia<-Barack,Mary<-Cynthia,Robert<-Michael,Robert<-Mary,Mary<-Claudia,Martha<-Robert
~~~

If the user were to enter **Claudia** as the person to show the ancestral line. The following is then display by the program.  

~~~
Martha  
Robert  
Mary  
~~~

##### Things to note #####
1. For the purposes of this question, you can assume that a child only has one parent.  
2. You can assume that the ancestral relationship string syntax is always correct.  
3. You can assume that the ancestral relationship string is never empty.  
4. You can assume that there's never any whitespace in the ancestral relationship string.  
5. The ancestal line displayed needs to be ordered form the most distant ancestor to least distant ancestor.  
6. You don't need to consider ancestral loops.  
7. Your implementation doesn't need to worry about performance.  

----------------------------------------------------------------------------------

#### Question 3 - Soccer ####
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
