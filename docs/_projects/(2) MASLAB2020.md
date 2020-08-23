---
name: Mobile Autonomous Systems Laboratory
tools: [ROS, Linux, TAMProxy, Arduino]
image: https://github.com/afangg/afangg.github.io/blob/master/images/maslab-comp.png?raw=true
description: Placed 3rd in the 6.146 MASLAB 2020 competition where my team and I designed and built the hardware and software components of a robot to autonomously collet, sort, and score in a timed challenge. 
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

<br>We brainstormed designs that could maximize the amout of scorable points. Because picking up cylinders off the ground and hanging them onto pegs scores the most amount of points, we knew we had to create a mechanism that could do such a task quickly and efficently. Furthermore, if a cylinder of a certain color is placed on a peg or marked goal of the same color, it is worth more points. Therefore, we determined our robot should pick up all the cylinders at once whilst driving around the stage, and it should store them in its body whiles in motion. The cylinders must also be sorted by color already so the robot will be able to place them on the correct colored goal pegs easily.

## Design and Implementation
<br>
<div class="row">
  <div class="column">
  	<center>
	  <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-front.png?raw=true" width="80%">
	  <em>The intake conveyer belt system on the front</em>
	</center>
  </div>
  <div class="column">
  	<center>
	  <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-back.png?raw=true" width="80%">
	  <em>The sorting and storage system on the back</em>
	</center>
  </div>
</div>

<br>As shown in the pictures above, the mechanical system of our robot is made of three main components. The first is the conveyor belt mechanism on the front of the robot that intakes cylinders off the ground when the robot drives over it. The second component is located on the back and includes the sorting and storage system. The camera determines the color of the cylinder and pushes a cylinder to the left or right side of the container because dropping it into one of the slot compartments. Finally to output the cylinders, the third part of the system is a simple motor that pushed 5 cylinders at once onto the correct pegs.
<br>
<div class="row">
  <div class="column">
    <center>
    <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-schematic.png?raw=true" width="80%">
    <em>The schematic of our electrical system. What I mainly worked on!</em>
  </center>
  </div>
  <div class="column">
    <center>
    <img src="https://github.com/afangg/afangg.github.io/blob/master/images/maslab-hardware.png?raw=true" width="80%">
    <em>Here are the sensors and actuators we used in our design</em>
  </center>
  </div>
</div>


<br>We also have an electrical system of servos, motors, motor controllers, an Arduino for low-level control, and an Intel Nuc as the main computer. There are also multiple webcams mounted around the body for computer vision and a lidar on top. In terms of the software, we used ROS for foundation of our system. We set up a system to control the motion of the robot with a game controller for testing early on. Our code for autonomous driving involves locating colored cylinders on the floor using OpenCV and driving towards them, varying speed based on distance away. The motors driving the conveyor belt are continuously running and sucks up cylinders when the robot drives over them. At the top they are then sorted by color.

## A Recap of the Month 

<br>It was definitely out of my comfort zone to join a group of random students and spend a month together working, but it was a great experience! We didn't get much help from the TAs, but instead were expected to be independent. My main contribution was towards setting up and testing the electrical system, since I had experience from the MIT Robotics Team. I learned a lot about ROS and SLAM, which I was trying to implement. This was a good introduction to when I took 6.141: Robotics Science and Systems the semester after (read more about that here). 
<br>
<br>
<center>
  <iframe width="600" height="350" src="https://www.youtube.com/embed/qUfptjLSZaI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> <br>
  <em>Video of our robot following a cylinder around the game field</em>
</center>

<br>It was a hectic month, and we were still working on the robot while waiting to compete on the day of competition! My biggest take away from this was it's ok to not make deliverable process every day, but to spend a while researching and learning. Also I learned to get the hardware prototyped ASAP! What's the point of having the software if there's no hardware?! And after all that hard work we placed third! Thank you to Sabina, Erina, Chenkai, and Adrian for a great month.

We also documented our progress on a wiki for the class here:
<p class="text-center">
{% include elements/button.html link="http://maslab.mit.edu/2020/wiki/team03" text="Official Team 3 Wiki" %}
</p>