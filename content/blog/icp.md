+++
title = "ICP explained"
date = 2024-08-17
weight = 1
draft = false
+++


Check out the visualization I made in the <a href="/projects"> Projects</a> page.

I'll be explaining the math and possible optimizations you can make with your implementation.
I haven't finished it but I'll try to work on it during my free time.


<h2> Formalizing the Problem</h2>

Let's suppose we're given the original scene below:

<div>
<a class="imglink" href="/img/icp_scene.png" target="_blank" width="100%">
        <img src="/img/icp_scene.png" width="100%">
    </a>
<div>
This scene has been reconstructed in 3D from multiple camera view points.<br>
We want to estimate the pose of the block M in the scene.<br>
We do this by fitting the 3D point clouds of the object in the scene and try to fit our 3D point clouds from the original model we know to the cluster of point clouds of the object in the scene. We will be minimizing the euclidean distance between our scene point clouds and the known model point clouds.<br>

We do this by iteratively solving the following problem:
$$
\begin{array}{ll}
\min _{R, t, c} & \sum_i\left\|R s_i+t-m_{c_i}\right\|_2^2 \\
\text { s.t. } & R^T=R^{-1}, \operatorname{det}(R)=1
\end{array}
$$

where $s_i$ are the points in the scene point cloud, $m_i$ are the points in the model point cloud, and $c_i$ is the integer index of the point in the $m$ that corresponds most closely with the $i$-th point in the scene.

This is a very hard and non-convex problem, so instead of solving the optimization in one step, the algorithm alternates between solving for ${\ R,t\}$ and c separately.

But that's a pretty slow to brute force-through, especially when you can have very dense 3D point clouds. 
- It's generally a relatively slow algorithm.
- There are point clouds in the raw data that are not relevant to the model.
- Our error function grows quadratically
- It's sensitive to outliers

<div>
<h2>KD Trees + Closest Point Heuristic</h2>
<a href="https://link.springer.com/article/10.1007/BF01427149">Zhang et al.</a> proposes a solution: why not use a modified version of KD-trees? The nice thing about this approach is that it's robust to occulusions and outliers. Conveniently, both SciPy and Open3D have KD-trees as an available data structure after importing the library, so I decided to use KD trees.
<div>

<h2>Coherent Point Drift (CPD)</h2>
This is quite a clever probabilistic approach. So in CPD,


<h2>Filtering based on Color</h2>


<h2>Another thing I could've done for a potentially faster solution: RANSAC</h2>
Note for self: don't forget to credit <a href="https://people.eecs.berkeley.edu/~pabbeel/cs287-fa11/slides/perception-for-robotics-instance-detection.pdf">Pieter Abbeel (CS287 slides from Berkeley)</a>