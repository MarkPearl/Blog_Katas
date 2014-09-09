---
layout: post
title: String Calculator Kata
tags: Useful
category: General
---
Roy Osherove's String Calculator Kata is a great kata as for some practices like TDD, Code Navigation.  

With some practice you should be able to complete this Kata in under 25 minutes.  

Here are some notes I have accumulated over time.  


Rules  
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
  
[For a list of other kata check here](http://stackoverflow.com/questions/2150702/tdd-bdd-screencast-video-resources)  
