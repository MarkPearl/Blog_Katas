---
layout: post
title: Mars Rover Challenge
tags: Useful
category: General
---

#### The Problem ####

You are controlling a mars rover. You are given the initial starting point (x,y) of the rover and the direction (N,S,E,W) it is facing. You need to be able to direct the rover on where to go.

----------------------------------------------------------------------------------------------

#### The Goal ####

- Develop an api that moves a rover around on a grid.  

----------------------------------------------------------------------------------------------

#### General Information ####

- The rover receives a character array of commands.  
- You are given the initial starting point (x,y) of a rover and the direction (N,S,E,W) it is facing. 
- If you are at position (x,y) assume the block immediately north from (x,y) is (x,y-1).  
- The first line of input is the upper-right coordinates of the plateau.   
- The lower-left coordinates are assumed to be (0,0).  

----------------------------------------------------------------------------------------------

#### Basic Requirements ####

- Implement commands that move the rover forward/backward (f,b).  
- Implement commands that turn the rover left/right (l,r).  
- Implement wrapping from one edge of the grid to another. (planets are spheres after all)  
- Implement obstacle detection before each move to a new square. If a given sequence of commands encounters an obstacle, the rover moves up to the last possible point and reports the obstacle.  

----------------------------------------------------------------------------------------------

#### Examples ####

##### Simple Example 1 #####

~~~
The rover is on a 100x100 grid at location (0, 0) and facing NORTH.  
The rover is given the commands "ffrff" and should end up at (2, 2)  
~~~

##### Simple Example 2 #####

~~~
The rover is on a 5x5 grid at location (1, 2) and facing NORTH.
The rover is given the commands "lf lf lf lf f and should end up at (1, 3) facing NORTH.
~~~

##### Simple Example 3 #####

~~~ 
The rover is on a 5x5 grid at location (3,3) and facing EAST
The rover is given the commands "ffr ffr fr rf" and should end up at (5, 1) facing EAST
~~~

##### Complex Example with a Wrapping #####

~~~ 
The rover is on a 5x5 grid at location (0,0) and facing EAST
The rover is given the commands "br br" and should end up at (5, 1) facing WEST
~~~


