+++
title = "Projects"

updated = 2024-08-17
+++

This is a list of projects I've done that I think are quite notable. Scroll down or Ctrl + F (or Cmd + F if you're using a Macbook) to "Web Dev" if you want to see the things I did in terms of web development.<br>
If you want to see what I've done in terms of other things like "Robotics" you can Ctrl+F / Cmd+F that too.


# Projects I made to make your lives easier:

## Mochi-roid
<div>
    <a class="imglink" href="/img/jtracer.png" target="_blank" width="50%" height="50%">
        <img src="/img/jtracer.png" width="50%" height="50%">
    </a>
</div>

(note this is a filler image for now until I deploy the bot and start using the bots with my roomates)

description coming soon

# Robotics

## mARVin (autonomous robotic vehicle)
<div>
    <a class="imglink" href="/img/marvinrun.mp4" target="_blank" width="75%" height="75%">
        <video width="75%" height="75%" controls autoplay>
            <source src="/img/marvinrun.mp4" type="video/mp4">
        </video>
    </a>
</div>

This is mARVin, our autonomous robotic vehicle that we've been working on in the [University of Michigan Autonomous Robotic Vehicle](https://www.umarv.com/), an engineering student organization. I've worked on the integration of sensors for mARVin and used them for [SLAM (Simultaneous Localization and Mapping)](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) algorithms in ROS2. We used sensors like IMUs, wheel encoders, and LiDAR. 
<div>
<a class="imglink" href="/img/slam.png" target="_blank" width="75%" height="75%">
        <img src="/img/slam.png" width="75%" height="75%">
    </a>
<div><br>As a sensors lead, in addition to everything I've been doing, I'll be communicating with other subteam leads and getting members to meet other subteam's needs that can be achieved with background in sensors and programming. I also host meetings and mentor new members as well. 
<br>Lately, we've been collaborating with the navigation team to integrate SLAM algorithms so they can do path planning with the information available from sensors and computer vision. I'm also helping out some navigation team members and leads with our custom simulation software as well.


## Web Robot Simulator and Interface

<div>
    <a class="imglink" href="/img/ik_viz.png" target="_blank" width="75%" height="75%">
        <img src="/img/ik_viz.png" width="75%" height="75%">
    </a>
</div>
<!-- Let's insert a GIF here since that'll look pretty cool-->

This is a web-based robot simulator for path planning, forward kinematics, inverse kinematics, PID, and more using Three.js. It also has a feature where you can render robots by making a JSON file that is structured in a similar way to a URDF file. (It's like an XML file but for robotics that define geometries and joints of robots). I also implemented a feature that allows the software to interface with the Fetch Robot via rosbridge. I want to thank Professor Chad Jenkins for fulfilling one of my goals I had since high school (to write code that works on the actual fetch robot, the first lab robot I've seen in-person).


<div>
    <a class="imglink" href="/img/rrt-planner.mp4" target="_blank" width="100%">
        <video width="100%" controls autoplay>
            <source src="/img/rrt-planner.mp4" type="video/mp4">
        </video>
    </a>
</div>

This is an extension of the robot simulator where it does path-planning via RRT (Rapidly exploring random trees). The reason why I chose to do RRT over A* is because while A* can produce a more optimal path, it's quite computationally expensive due to how exhaustive it is, so it can be slow in large/complex/higher dimensions (e.g. in 3D vs 2D). Path-planning via RRT could be faster due to its nature of being a sampling-based algorithm that searches through nonconvex, high-dimensional spaces such as the Three.js scene as shown above in the video.


## stacking blocks with a Kuka LBR iiwa
<div>
<a class="imglink" href="/img/stacking.gif" target="_blank" width="100%">
        <img src="/img/stacking.gif" width="100%">
    </a>
<div>
Stacked objects on top of each other with a Kuka LBR iiwa robot arm. I ensured force closure of 
object when picked up with the arm and precisely stacked them on top of each other. The simulation
was done on PyBullet.

## point cloud ICP

<div>
    <a class="imglink" href="/img/icp.gif" target="_blank" width="100%">
        <img src="/img/icp.gif" width="100%">
    </a>
</div>
<!-- Let's insert a GIF here since that'll look pretty cool-->

Iterative Closest Point (ICP) is an perception algorithm where you do pose estimation of an object in a scene given a model. It does this by minimizing the distance between the point clouds from the original model and the detected object that corresponds to the model in the scene. By fitting the model, we know the orientation (the pose) of the object. I made the visualization with Open3D. I plan on explaining the math and how I optimized the code in detail (via a certain data structure and design decision) in a blog post soon.

## Biped Robot Locomotion
<div>
    <a class="imglink" href="/img/cassie-cardio.mp4" target="_blank" width="50%">
    <video width="400" controls autoplay>
        <source src="/img/cassie-cardio.mp4" type="video/mp4">
    </video>
    </a>
</div>
I was learning locomotion with biped robots through this collection of projects. I want to thank Professor Jessy Grizzle and Dr. Wami Ogunbi for mentoring me as a research assistant. I have been working on this until Wami completed her PhD. I learned optimal control things like Model Predictive Control (MPC) as well as other mathematical concepts (e.g. Lie Algebra, Manifolds, etc.) and control concepts (e.g. feedback linearization, PID, etc.) and how they're applied to robotic control as well as a bit of reinforcement learning (more of a self-studied thing) via Deep Deterministic Policy Gradients. I did this to <br>
1.&#41; Audit the "Biped Bootcamp" a paper by Dr. Wami Ogunbi, a paper now incorporated into the University of Michigan’s Robotics Department curriculum for undergraduate instruction<br>
2.&#41; Have enough background to work on some sort of reinforcement learning for bipedal robots as a side project<br>
3.&#41; Make a robust algorithm for the robot to walk on non-stationary or inclined surfaces. Here's the simulation of the robot walking on inclines and stairs:

<div style="display: flex;">
    <a class="imglink" href="/img/incline.gif" target="_blank" width="40%">
        <img src="/img/incline.gif" width="100%">
    </a>
    <a class="imglink" href="/img/stairclimb_sim.gif" target="_blank" width="40%">
        <img src="/img/stairclimb_sim.gif" width="100%">
    </a></div>
</div>


# Web Dev

## Instagram Clone
(screen recording coming soon)
<div>
    <a class="imglink" href="/img/jtracer.png" target="_blank" width="100%">
        <img src="/img/jtracer.png" width="100%">
    </a>
</div>

I built an instagram application using client-side dynamic pages and a REST API. I also wrote a client application in JavaScript that runs in the browser and makes AJAX calls to the REST API. I briefly hosted this via AWS EC2 until my free trial expired.



## Search Engine
(screen recording coming soon)
<div>
    <a class="imglink" href="/img/jtracer.png" target="_blank" width="100%">
        <img src="/img/jtracer.png" width="100%">
    </a>
</div>

A simplified search engine I made. It utilizes a tf-idf based search algorithm and leverages a custom version of the MapReduce framework. The framework supports fault tolerance, and it is able to handle failures of both mappers and reducers. The framework is concurrent and can run multiple jobs at the same time. I also briefly hosted this via AWS EC2 until my free trial expired.


## A* visualizer

This is a visualization of the A* search algorithm. The heuristic I used is based on the euclidian distance from the goal coordinate. It's just a simple 2D map, so A* works for this purpose. 
I think I'll eventually make it so you can select various algorithms (DFS, BFS, Djikstra, RRT, D*, etc.)
But this is one thing I used to brush up on my data structures and algorithms skills. The screen recording below is a demo of the A* algorithm being used for path planning.

<div>
    <a class="imglink" href="/img/a-star.mp4" target="_blank" width="100%">
        <video width="100%" controls autoplay>
            <source src="/img/a-star.mp4" type="video/mp4">
        </video>
    </a>
</div>




# Computer Graphics, Animation, Simulations

basically anything that's relevant to graphics and simulations. That includes anything where
I use numerical analysis concepts too.

## Numerical Methods concepts applied to PID control

I made a simple PID pendulum simulator using various type of numerical analysis algorithms including Euler, Verlet, Velocity Verlet, and Runge–Kutta (4th-Order) to approximate the integration (the I in PID) term.

<div>
    <a class="imglink" href="/img/pid_and_integrator.mp4" target="_blank" width="100%">
        <video width="100%" controls autoplay>
            <source src="/img/pid_and_integrator.mp4" type="video/mp4">
        </video>
    </a>
</div>

It's made to be stable at the x_desired point.


## Linear Complementarity Problem Simulation

I simulated collision and bouncing of a box by rewriting the constraints and the dynamics for contact resolution as a [linear complementarity problem (LCP)](https://en.wikipedia.org/wiki/Linear_complementarity_problem). <br>
I know the Bullet and NVIDIA PhysX physics engines uses LCP whereas the NVIDIA Isaac Sim uses some sort of penalty based approach to the problem. By changing the coefficient of restitude, you can adjust the bounciness of the box. <br>
I can also explain the math that makes this work if enough people request it.

<div>
<a class="imglink" href="/img/LCP_bounce.gif" target="_blank" width="100%">
        <img src="/img/LCP_bounce.gif" width="100%">
    </a>
<div>


## Data Analytics / Non-Deep Learning ML projects

# coming soon

I'll be putting in more notable data analytics projects both serious and somewhat non-serious (as long as it's done rigorously)