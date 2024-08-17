+++
title = "ICP explained"
date = 2024-08-17
weight = 1
draft = false
+++


Check out the visualization I made in the <a href="/projects"> Projects</a> page.

I'll be explaining the math and possible optimizations you can make with your implementation.
I haven't finished it but I'll try to work on it during my free time.


<h1> Formalizing the Problem & Curse of dimensionality</h1>

Let's suppose we're given the original scene below:

<div>
<a class="imglink" href="/img/icp_scene.png" target="_blank" width="100%">
        <img src="/img/icp_scene.png" width="100%">
    </a>
<div>
This scene has been reconstructed in 3D from multiple camera view points.<br>
We want to estimate the pose of the block M in the scene.<br>
We do this by fitting the 3D point clouds of the object in the scene and try to fit our 3D point clouds from the original model we know to the cluster of point clouds of the object in the scene. We will be minimizing the euclidean distance between our scene point clouds and the known model point clouds.<br>