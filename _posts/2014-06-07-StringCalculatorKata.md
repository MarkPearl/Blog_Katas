---
layout: post
title: String Calculator Kata
tags: Useful
category: General
---
Roy Osherove's String Calculator Kata is a great kata as for some practices like TDD, Code Navigation and Refactoring.  

With some practice you should be able to complete entire Kata in under [25 minutes](https://www.youtube.com/watch?v=tBt3O43sk0k).  

#### The Process ####

- Try not to read ahead.  
- Do one task at a time - work incrementally.  
- Make sure you only test for correct inputs - there is no need to test for invalid inputs for this kata  

#### The Steps ####

##### Step 1 #####

Create a simple String calculator with a method int Add(string numbers).  
An empty string returns zero, example Add("") return 0;  






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
