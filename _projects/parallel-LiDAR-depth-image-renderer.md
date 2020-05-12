---
time: 2020
date: 12 May 2020
title: Parallel LiDAR Depth Image Renderer
tags: [CUDA, OpenMP, performance-engineering, PCL, ROS]
awards:
description: >
  Parallel implementation of a renderer projecting 3D LiDAR points to 2D image.
thumbnail: /assets/img/2020/parallel/thumbnail.png
layout: post
rank: 2
---
![Result](/assets/img/2020/parallel/thumbnail.png)

This project is done as our class project for
CMU 15-418 Parallel Computer Architecture and Programming.

## Authors

- Henry Zhang (hengruiz@andrew.cmu.edu)
- Haowen Shi (haowensh@andrew.cmu.edu)

## Abstract

In this project we implemented a LiDAR depth image rendering too which takes in
LiDAR 3D point clouds in the world frame and renders a depth image
from the camera’s field of view by transforming and projecting these points.

We implemented sequential (one process on single CPU core),
OpenMP, and CUDA versions, then benchmarked and compared their performance.

## Framework

### OpenMP

![OpenMP](/assets/img/2020/parallel/renderer_omp_arch.png)

In this implementation,
we group up the incoming lidar points and distribute them evenly across
number of designated cores.

### CUDA

![CUDA](/assets/img/2020/parallel/renderer_cuda_arch.png)

In this implementation,
we have the same workload splitting strategy but spread them across
many more GPU compute cores. Because we could not use the PCL library
on CUDA code, we designed custom data wrappers for low-overhead communication
between CPU and GPU and implemented some PCL pcocessing code ourselves.

## Results

![FrameTime](/assets/img/2020/parallel/impl_ftime_comparison.png)

![Speedup](/assets/img/2020/parallel/impl_ftime.png)

For the same dataset with constant high workload for the renderer,
We achieved on average, maximum of 2.9x speedup for OpenMP implementation
and 120x speedup for CUDA implementation.
