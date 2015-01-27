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

#### Basic Requirements ####

- The rover receives a character array of commands.  
- You are given the initial starting point (x,y) of a rover and the direction (N,S,E,W) it is facing.  
- Implement commands that move the rover forward/backward (f,b).  
- Implement commands that turn the rover left/right (l,r).  
- Implement wrapping from one edge of the grid to another. (planets are spheres after all)  
- Implement obstacle detection before each move to a new square. If a given sequence of commands encounters an obstacle, the rover moves up to the last possible point and reports the obstacle.  


#### Example ####

~~~
The rover is on a 100x100 grid at location (0, 0) and facing NORTH.  
The rover is given the commands "ffrff" and should end up at (2, 2)  
~~~



