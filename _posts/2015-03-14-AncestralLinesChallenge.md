---
layout: post
title: Ancestral Lines Challenge
tags: Useful
category: General
---

#### Ancestoral Lines ####

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

