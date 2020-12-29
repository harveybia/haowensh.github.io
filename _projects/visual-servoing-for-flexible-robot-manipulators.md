---
time: 2020
date: 11 May 2020
title: Visual Servoing for Flexible Robot Manipulators
tags: [kinematics, computer-vision, ROS, simulation]
awards:
description: >
  A method to solve the inverse kinematics problem for robot manipulators
  with flexible links
thumbnail: /assets/img/2020/kdc/thumbnail.png
layout: post
rank: 997
---
![Simulation](/assets/img/2020/kdc/frame_confirmation.png)

This project is done as our class project for
CMU 16-711 Kinematics, Dynamics and Control.

## Authors

- Haowen (Harvey) Shi (haowensh@andrew.cmu.edu)
- Daqian Cheng (daqianc@andrew.cmu.edu)
- Hengrui (Henry) Zhang (hengruiz@andrew.cmu.edu)

## Abstract

Generally, to solve the Inverse Kinematics (IK) problem of a rigid manipulator,
we first need its kinematic parameters (D-H or twists) obtained via
the mechanical specification and/or external calibration.
However, flexible robots have changing parameters and hence their IK cannot
be solved in this way.

In this project, we proposed a method to solve the IK problem for the robot
manipulators with flexible links. We formulate the problem as an IK problem for
manipulators with unknown geometry, and iteratively & numerically estimate
the twists (kinematic parameters) of our manipulator on the fly.
Our pipeline consists of two major parts: an AprilTag based end-effector pose
estimation and iterative IK solver.

## Framework

![Framework](/assets/img/2020/kdc/framework.png)

## Results

This video shows our experiment with a 9 DoF snake-like arm with flexible
links (modelled using friction joints on top of motorized joints) in
CoppeliaSim simulation environment.
<div class="video-responsive">
    <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/B46CvOQX2VM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<br>

## For more information
View our project code on GitHub:

<a class="github-button" href="https://github.com/harveybia/jacobian-visual-servo" data-color-scheme="no-preference: light; light: light; dark: dark;" data-size="large" data-show-count="true" aria-label="Star harveybia/jacobian-visual-servo on GitHub">
jacobian-visual-servo
</a>

<a href="https://github.com/harveybia/jacobian-visual-servo/blob/master/docs/16_711_Project_Report.pdf" target="_blank">
Download our project report
</a>

