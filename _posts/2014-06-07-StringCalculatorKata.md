---
layout: post
title: String Calculator Kata
tags: Useful
category: General
---
Roy Osherove's String Calculator Kata is a great way to learn practices like test driven development, code navigation and refactoring.  

With some practice you should be able to complete entire Kata in under [25 minutes](https://www.youtube.com/watch?v=tBt3O43sk0k).  

#### The Process ####

- Try not to read ahead.  
- Do one step at a time - work incrementally.  
- Make sure you only test for correct inputs - there is no need to test for invalid inputs

----------------------------------------------------------------------------------------------

#### Steps ####

##### Step 1 #####

Create a simple String calculator with a method that takes a string and returns a number
i.e. int Add(string numbers)  

**Add("") > Returns 0**

##### Step 2 #####

A single number returns that number

**Add("1") > Returns 1**
**Add("3") > Returns 3**

##### Step 3 #####

A two numbers returns the sum  

**Add("1,2") > Returns 3**
**Add("3,5") > Returns 8**

##### Step 4 #####

Any unknown amount of numbers returns the sum of those numbers 

**Add("1,2,3") > Returns 6**
**Add("3,5,3,9") > Returns 20**

##### Step 5 #####

New line breaks and commas should be interchangeable between numbers   

**Add("1,2\n3") > Returns 6**
**Add("3\n5\n3,9") > Returns 20**

The following is not ok, don't write a test but be aware... 

**Add("1,\n")**

##### Step 6 #####

Support different delimiters. To change a delimiter, the beginning of the string will contain a separate line that looks like this:   

"//[delimiter]\n[numbers...]"  

**Add("//;\n1;2") > Returns 3**  

The first section is optional. All existing steps should still be supported.  

##### Step 7 #####

Calling add with a negative number will throw an exception "Negatives not allowed" and the negative number that was passed.  

**Add("-1,2,-3") > Throws exception with Negatives not allowed: -1, -3**  

##### Step 8 #####

Numbers bigger than 1000 should be ignored.  

**Add("1000,1001,2") > Returns 2**  

##### Step 9 #####

Delimiters can be of any length with the following format...  

**"//[delimiter]\n"**  

**Add("//[***]\n1***2***3") > Returns 6**  


##### Step 10 #####

Allow multiple delimiters...  

"//[delim1][delim2]\n"

**Add("//[*][%]\n1*2%3") > Returns 6**  

##### Step 11 #####

Handle multiple delimiters with a length longer than one character...  

**Add("//[***][#][%]\n1***2#3") > Returns 6**  

##### Step 12 #####

Handle delimiters that have numbers as part of them, where the number cannot be on the edge of a delimiter...  

**Add("//[*1*][%]\n1*1*2%3") > Returns 6**  

----------------------------------------------------------------------------------------------

#### Quick Summary of the rules ####

- Empty String Returns 0  
- Two Numbers returns Sum  
- X Numbers Returns Sum  
- Custom Delimiter "//;\n1;2" = 3  
- Handle new line as delimiter  
- Cannot add negative numbers  
- Number bigger than 1000 are ignored  
- Delimiter of any length "//[dd]\n|[dd]2"=3  
- Allow multiple delimiter "//[%][;]\n1%2;3"=6  
- Multiple delimiter of any length  

#### Notes on some sections ####

Split string 

~~~
const string input = "1,2;3";
var result = input.Split(new string[]{",", ";"},StringSplitOptions.RemoveEmptyEntries);
Assert.That(result.Count(), Is.EqualTo(3));
~~~

Get denominator from string 

~~~
return new (input.Skip(20)Take(1).ToArray());  
~~~

#### References ####

[Original Post](http://osherove.com/tdd-kata-1/)
[For a list of other kata check here](http://stackoverflow.com/questions/2150702/tdd-bdd-screencast-video-resources)  
