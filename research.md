---
layout: page
permalink: /Project/index.html
title: Project
---

<section id="table-of-contents" class="toc">
  <header>
    <h3>Contents</h3>
  </header>
<div id="drawer" markdown="1">
*  Auto generated table of contents
{:toc}
</div>
</section><!-- /#table-of-contents -->

### Motion-Planning in Dynamic Environment

In this topic we try to solve a motion planning problem that for a vehicle to achieve complex tasks but assume the environment is changing during the time such as some moving targets and moving obstacles. 

Like the example video below, the task for the vehicle(red) is to reach some moving targets(yellow) in a certain order, and avoid moving obstacles(brown), also there are some doors in the environment open and close in some time. 

The basic idea is from previous projects but add another time dimension in the search space, and build a switch policy that switch searching between dynamic space and static space to save computation time. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/W46rtjU7bM8?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

###  Trajectory Generation for Nonholonomic Vehicles

Cell decomposition-based path planning gives a sequence of cells but not actual trajectory, so I developed a sampling based algorithm to converge a optimal trajectory in the sequence of cells with kinematic constraint(in the example below, the vehicle has a minimum turning radius). Based on the [Curvature-Bounded Traversability Analysis(CBTA)](http://ieeexplore.ieee.org/abstract/document/6805219/) technic, the sampling space only on the edge of cells, this way the computation reduced dramatically. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/0MAQMWObWh4?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>


###  Multiple Vehicles Task-Planning

The challenge to extend single vehicle motion planning to multiple vehicles case is to handle the computation, especially with kinematic constraint. An incremental motion planning algorithm was developed for a group of vehicles could accomplished a global task. 

In the example below, the task for the four vehicles(green) is to visit all the target regions(red) in the environment, and optimal paths(orange) are found. 

<div style="display:block;text-align:center"><img src="../images/multi.png" width='360px'></div>


### Motion-Planning with Temporal Logic Specifications for Nonholonomic Vehicles

<!-- Autonomous vehicles – aircraft, cars, rovers, over- and underwater vehicles that can move in the real world by themselves without human pilotage – have gained immense importance not only due to the broad spectrum of their potential military and civilian applications, but also due to the concurrent development of sensor technology and embedded systems that enable the realization of true autonomy. These vehicles may be assigned tasks that are dull and/or repetitive, such as mobile surveillance or cleaning and maintenance; tasks that are dangerous for humans, such as military transportation via hostile territory, large-scale fire-fighting, and repair and recovery operations in chemical plants and nuclear reactors; or tasks that are prohibitively expensive for humans to execute, such as the exploration of celestial bodies. -->
	

Major part of my PhD research. Firstly, we are interested in the optimal motion planning and control problem, which involves finding control inputs (e.g. steering, throttle) that enable the vehicle’s desired motion. Optimal control theory has been studied for over three hundred years, but new computational strategies are required to develop real-time algorithms.


Secondly, we are interested in the intelligent control problem, which involves developing and integrating artificial intelligence (AI) algorithms with control algorithms to enable the vehicle to achieve complex tasks specified in human-like language (e.g. get me to my workplace ASAP, drop my friend close to his workplace, find a cheap parking spot and wait until I need you again; also save gasoline as much as possible).  AI and automatic control have been traditionally disparate academic disciplines; furthermore, AI and control problems are formulated using fundamentally different mathematical tools, which makes their integration challenging.

Instead of point to point path search, the examples below show how a vehicle with a minimum turning radius accomplish a task. The first task requires the vehicle not only that the regions red and yellow be both visited, but also that the region red be visited first. The second task requires the vehicle returns to either one of the green regions after visiting red and yellow. 


<!-- Our preliminary approach to the solution of these problems is the H-cost motion-planning algorithm. The general idea is to modify standard workspace cell decomposition-based path-planning to accommodate constraints due to vehicle dynamics. To this end, costs on successions of edges in the workspace cell decomposition graph are considered. The image on the left shows a result of implementation of this algorithm for a particle with a constraint on the magnitude of acceleration. Compared to randomized sampling-based planning, this algorithm results in a trajectory with far lower cost, while satisfying workspace constraints (i.e. avoiding obstacles) and vehicle dynamical constraints. -->


<div style="display:block;text-align:center"><img src="../images/taskplan.png" width='550px'></div>


### Object Recognition
Course project, aim to develop a method to recognize a certain object. A frisbee as testing object, first we narrow down the domain using color filter and contour detection.
<div style="display:block;text-align:center"><img src="../images/Object Recognition.jpg" width='800px'></div>

Then apply [Speeded Up Robust Features(SURF)](https://en.wikipedia.org/wiki/Speeded_up_robust_features) algorithm for feature detection. 
<div style="display:block;text-align:center"><img src="../images/Good Matches.jpg" width='530px'></div>

### Incremental Path Repair Algorithm
Path planning with dyanmic or kinematic constraints. An incremental algorithm has been developed to find a point to point optimal path with dyanmic or kinematic constraints of the vehicle. 

In the example below, we need to find a path from green point to red point for a vehicle which has a minimum turning radius. The left is the A* algorithm solution, and it's not feasible for our vehicle model, we "repair" such path into the right one. The solution converge to optimal given enough computation time.


<div style="display:block;text-align:center">
  <img src="../images/path_repair_2.png" width='265px'>
  <img src="../images/path_repair_1.png" width='265px'>
</div>

### Game Hex AI

<!-- GZoltar is a framework for automating the testing and debugging phases of the software development life-cycle. At the moment, the framework is provided as an Eclipse plug-in and integrates seamlessly with JUnit tests.

The idea of automating this process started in 2005 as part of the PhD research of Rui Abreu working with Arjan J.C. van Gemund (back then at the Delft University of Technology). Initially, the focus was to automate the debugging phase, and the initial idea, published at TAIC-PART'07, was to generate diagnosis candidates taking as input the coverage information for each test case. Later in 2010, there was the need to provide better visualization reports, which lead to the first version of GZoltar (and was published at TOPI'11, an ICSE'11 workshop). In the same framework, developers can find techniques for test case minimization and prioritization - this way creating a perfect ecosystem for performing testing and debugging. Currently the framework is available as a library, which every developer/researcher can use the power of GZoltar to implement new techniques for fault localization or test suite minimization.

More information -- [GZoltar website](http://www.gzoltar.com) -->

