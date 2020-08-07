---
name: Mobile Autonomous Systems Laboratory
tools: [ROS, Linux, TAMProxy, Arduino]
image: https://github.com/afangg/afangg.github.io/blob/master/images/maslab-comp.png?raw=true
description: Placed 3rd in the 6.146 MASLab 2020 competition where my team and I designed and built the hardware and software components of a robot to autonomously collet, sort, and score in a timed challenge. 
---

# Mobile Autonomous System Laboratory 2020

[MASLAB](http://maslab.mit.edu/2020/) is an annual robotics competition during MIT's Independents Activities Period in the month of January where teams of 3-5 build an autonomous robot to compete in a challenge designed for that year. This program is completely student driven, from the TAs who host it, to the students who design and build their submitions from scratch.

## The Challenge

This year, the challenge involved collecting red and green cylinders throughout the stage and placing them into goal areas to score points. Points were determined by which goal a cylinder was deposited into. They could either be pushed into marked areas on the ground or hung on pegs on the arena walls. 
<p align="center">
  <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-comp.png?raw=true" width="80%">
  <em>Our robot on the bottom left in the competition stage. You can see the cylinders and the goal posts</em>
</p>

For more information about the 2020 challenge and arena, here is the [game manual](http://maslab.mit.edu/2020/files/rules.pdf)

## Our strategy

We brainstormed designs that could maximize the amout of scorable points. Because picking up cylinders off the ground and hanging them onto pegs scores the most amount of points, we knew we had to create a mechanism that could do such a task quickly and efficently. Furthermore, if a cylinder of a certain color is placed on a peg or marked goal of the same color, it is worth more points. Therefore, we determined our robot should pick up all the cylinders at once whilst driving around the stage, and it should store them in its body whiles in motion. The cylinders must also be sorted by color already so the robot will be able to place them on the correct colored goal pegs easily.

<div class="row">
  <div class="column">
	  <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-front.png?raw=true" width="80%">
	  <em>The intake conveyer belt system on the front</em>
  </div>
  <div class="column">
	  <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-back.png?raw=true" width="80%">
	  <em>The sorting and storage system on the back</em>
  </div>
</div>

As shown in the pictures, the mechanical system of our robot is made of three main components. The first is the conveyor belt mechanism on the front of the robot that intakes cylinders off the ground when the robot drives over it. The second component is located on the back and includes the sorting and storage system. The camera determines the color of the cylinder and pushes a cylinder to the left or right side of the container because dropping it into one of the slot compartments. Finally to output the cylinders, the third part of the system is a simple motor that pushed 5 cylinders at once onto the correct pegs.

## A Recap of the Month

<p class="text-center">
{% include elements/button.html link="http://maslab.mit.edu/2020/wiki/team03" text="Official Team 3 Wiki" %}
</p>