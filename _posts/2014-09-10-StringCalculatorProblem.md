---
layout: post
title: String Calculator Challenge
tags: Useful
category: General
---

#### The Problem ####

- You are working for a new calculator company competeing with HP Calculators.  
- Business has told you that if you can get the following library done for calculating the value of a string they will make millions.  
- Write library that has a single add method that returns an integer value when called that meets the below requirements.  

----------------------------------------------------------------------------------------------

#### The Basic Requirements ####

Create a simple string calculator with a method that takes a string and returns a number. It should solve the following criteria. 

- A empty string returns zero.  
- A single number returns that number.  
- Two numbers return the sum of the numbers.  
- Any amount of numbers separated by a comma returns the sum of those numbers.  
- New line breaks and commas should be interchangeable as standard delimiters between numbers.  

~~~
Add("") > Returns 0
Add("1") > Returns 1
Add("3") > Returns 3
Add("1,2") > Returns 3
Add("3,5") > Returns 8
Add("1,2,3") > Returns 6
Add("3,5,3,9") > Returns 20
Add("1,2\n3") > Returns 6
Add("3\n5\n3,9") > Returns 20
~~~

The following is not ok but you do not need to worry about this ever being an input into the library.

~~~
Add("1,\n")
~~~

##### Intermediate Requirements #####

- Support different delimiters - to change a delimiter, the beginning of the string will contain a separate line that looks like this **"//[delimiter]\n[numbers...]"**  The first section up to the \n is optional. All existing requirements from the basic requirements section should still be supported.  
- Calling add with a negative number will throw an exception "Negatives not allowed" and the negative number that was passed.  
- Numbers bigger than 1000 should be ignored.  
- Delimiters can be of any length with the following format.  **"//[delimiter]\n"**  


~~~
Add("//;\n1;2") > Returns 3  
Add("-1,2,-3") > Throws exception with Negatives not allowed: -1, -3  
Add("1000,1001,2") > Returns 2  
Add("//[***]\n1***2***3") > Returns 6  
~~~

##### Advanced Requirements #####

- Allow multiple delimiters... **"//[delim1][delim2]\n"**
- Handle multiple delimiters with a length longer than one character.  
- Handle delimiters that have numbers as part of them, where the number cannot be on the edge of a delimiter. Note - a delimiter of 1DD or DD1 is not valid as it has a number on the edge of it. D1D is a valid delimiter)

~~~
Add("//[*][%]\n1*2%3") > Returns 6  
Add("//[***][#][%]\n1***2#3%4") > Returns 10  
Add("//[*1*][%]\n1*1*2%3") > Returns 6  
~~~


