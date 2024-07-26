+++
title = "Projects"

updated = 2023-12-20
+++

This is a very much non-exhaustive list of projects I've done. Scroll down or Ctrl + F (or Cmd + F if you're using a Macbook) to "Web Dev" if you want to see the things I did in terms of web development.


# Personal Projects:

## Mochi-roid
<div>
    <a class="imglink" href="/img/jqoiview.png" target="_blank" width="100%">
        <img src="/img/jqoiview.png" width="100%">
    </a>
</div>

This is a bot that I made for the social media platform Discord, a platform that is similar to Slack but more casual and with more practical features in my personal opinion. <br>
I made this bot to game-ify the process of doing the chores to encourage my roommates to do their chores because we tend to be busy and thus postpone doing chores. <br>
Discuss with your roommates what you want the reward to be for doing their chores the most consistently. In our case, we decided that boba 🧋 would be our reward. Each user does their chores and send a picture in a dedicated channel on the discord server to receive peer approval via emoji reactions. Once the majority of the server approves, the user will earn a point. The winner will be decided monthly based on the number of points accumulated. When there is a tie for the top winners, the winner will be chosen at random within the tie. Everybody else pitches in the money for the winner's prize.<br>

# Robotics

## mARVin (autonomous robotic vehicle)
<div>
    <a class="imglink" href="/img/marvinrun.mp4" target="_blank" width="100%">
        <video width="100%" controls autoplay>
            <source src="/img/marvinrun.mp4" type="video/mp4">
        </video>
    </a>
</div>

This is mARVin, our autonomous robotic vehicle that we've been working on in the [University of Michigan Autonomous Robotic Vehicle](https://www.umarv.com/), an engineering student organization. I've worked on the integration of sensors for mARVin and used them for [SLAM (Simultaneous Localization and Mapping)](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) algorithms in ROS2. We used sensors like IMUs, wheel encoders, and LiDAR. <br>As a sensors lead, in addition to everything I've been doing, I'll be communicating with other subteam leads and getting members to meet other subteam's needs that can be achieved with background in sensors and programming. I also host meetings and mentor new members as well. <br>Lately, we've been collaborating with the navigation team to integrate SLAM algorithms so they can do path planning with the information available from sensors and computer vision. I'm also helping out some navigation team members and leads with our custom simulation software as well.


## Web Robot Simulator and Interface

<div>
    <a class="imglink" href="/img/rustsweeper.png" target="_blank" width="100%">
        <img src="/img/rustsweeper.png" width="100%">
    </a>
</div>
<!-- Let's insert a GIF here since that'll look pretty cool-->

This is a web-based robot simulator for path planning, forward kinematics, inverse kinematics, PID, and more using Three.js. It also has a feature where you can render robots by making a JSON file that is structured in a similar way to a URDF file. (It's like an XML file but for robotics that define geometries and joints of robots). I also implemented a feature that allows the software to interface with the Fetch Robot via rosbridge. I want to thank Professor Chad Jenkins for fulfilling one of my goal I had since high school (to write code that works on the actual fetch robot).

<div>
    <a class="imglink" href="/img/rustsweeper.png" target="_blank" width="100%">
        <img src="/img/rustsweeper.png" width="100%">
    </a>
</div>
<!-- Let's insert a GIF here since that'll look pretty cool-->

The background in moving simulated robots via Three.js allowed me to quickly learn how to animate things like a Finite-State-Machine on Blender using Blender's logic states. So I created a dance video for a [vocaloid](https://en.wikipedia.org/wiki/Vocaloid) song called Mesmerizer by Satsuki. The models are the based on the same characters from the [original MV](https://www.youtube.com/watch?v=19y8YTbvri8) taken from HatsuneDKaname on DevianArt. Since the movements are snappy, it is easy to define well-defined set points to do inverse kinematics with to the next set point. Thus, I was able to learn and create this animation despite having limited experience in Blender at the time. See the "Computer Graphics" section to see a brief description of one of my on-going projects that these two things inspired me to do.

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
    </a></div>
<!-- Let's insert a GIF here since that'll look pretty cool-->

Iterative Closest Point (ICP) is an perception algorithm where you do pose estimation of an object in a scene given a model. It does this by minimizing the distance between the point clouds from the original model and the detected object that corresponds to the model in the scene. By fitting the model, we know the orientation (the pose) of the object. I made the visualization with Open3D. I plan on explaining the math and how I optimized the code in detail (via a certain data structure and design decision) in a blog post soon.

# Biped Robot Locomotion
<div>
    <a class="imglink" href="/img/cassie-cardio.mov" target="_blank" width="50%">
    <video width="400" controls autoplay>
        <source src="/img/cassie-cardio.mov" type="video/mp4">
    </video>
    </a>
</div>
I was learning locomotion with biped robots through this collection of projects. I want to thank Professor Jessy Grizzle and Dr. Wami Ogunbi for mentoring me as a research assistant. I have been working on this until Wami completed her PhD. I learned optimal control things like Model Predictive Control (MPC) as well as other mathematical concepts (e.g. Lie Algebra, Manifolds, etc.) and how they're applied to robotic control as well as a bit of reinforcement learning (more of a self-studied thing). The goal was to make a robust algorithm for the robot to walk on non-stationary or inclined surfaces.  Here's the simulation of it below. 
<div>
    <a class="imglink" href="/img/incline.gif" target="_blank" width="50%">
        <img src="/img/incline.gif" width="25%">
    </a>
    <a class="imglink" href="/img/stairclimb_sim.gif" target="_blank" width="50%">
        <img src="/img/stairclimb_sim.gif" width="25%">
    </a></div>
<div>




# Web Dev

## Instagram Clone

<div>
    <a class="imglink" href="/img/jqoiview.png" target="_blank" width="100%">
        <img src="/img/jqoiview.png" width="100%">
    </a>
</div>
<!-- [Demo Video](INSERT URL)-->

I built an instagram application using client-side dynamic pages and a REST API. I also wrote a client application in JavaScript that runs in the browser and makes AJAX calls to the REST API. I briefly hosted this via AWS EC2 until my free trial expired.



# Search Engine

<div style="display: flex;">
    <a class="imglink" href="/img/santorini.png" target="_blank" width="50%">
        <img src="/img/santorini.png" width="100%">
    </a>
    <a class="imglink" href="/img/santorini_dithered.png" target="_blank" width="50%">
        <img src="/img/santorini_dithered.png" width="100%">
    </a>
</div>
<!-- [Demo Video](INSERT URL)-->

A simplified search engine I made. It utilizes a tf-idf based search algorithm and leverages a custom version of the MapReduce framework. The framework supports fault tolerance, and it is able to handle failures of both mappers and reducers. The framework is concurrent and can run multiple jobs at the same time. I also briefly hosted this via AWS EC2 until my free trial expired.


## Computer Graphics

# NeRF-viz

NeRF is a deep learning model that utilizes something called neural radiance fields to perform 3D reconstruction from 2D images. This just showcases models that my NeRF models made. Photogrammetry/3D reconstruction are things I am interested in within computer vision.<br>

github link coming soon

# Animating Like A Computer Scientist (ALACS)

ALACS, (pronounced like the name Alex but with an a instead of an e, so Alax) is an addon I am currently working on that allows people to rig their blender models and re-use poses based on the user's desired logic like a Finite-State-Machine. It also comes with a unique feature that I'll disclose once I get a working (even if not perfect) solution. But the goal is to make model rigging more accessible and affordable. <br>

github link coming soon


## Data Analytics / Non-Deep Learning ML projects

# coming soon
