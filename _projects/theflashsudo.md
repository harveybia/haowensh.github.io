---
time: 2016
date: 16 Jun 2016
title: 'Mobot "the-flash-sudo"'
tags: [planning, computer-vision, RaspberryPi, LEGO]
awards: First Place and Award Winning
description: CMU Annual Mobot Challenge
thumbnail: /assets/img/proj/theflashsudo/flash.jpg
layout: post
rank: 9999
---
![The Flash](/assets/img/proj/theflashsudo/flash.jpg)

The [Mobot Race][mobot_homepage] is a Carnegie Mellon tradition held annually
during the Spring Carnival. It's a tribute to the "hello world" of robotics -
a line following robot, but made more challenging given a tough terrain.

## Team Members

- Haowen (Harvey) Shi
- Zixu (Elias) Lu
- Yixiu (Matthew) Zhao

![Team](/assets/img/proj/theflashsudo/team.jpeg)
<small>
  From left to right: Yixiu, Haowen, Zixu. Image credit: [Justin Chu][justin_c].
</small>


## Story
In my freshman spring semester I led a team of three to build a robot and
compete in the annual Mobot Race. We started the project about four months
prior to the competition day, went through many design iterations of both
the hardware and the software. We took the project seriously and aimed for
the $1,000 first place money prize.

![Me And Matthew](/assets/img/proj/theflashsudo/hacking.jpeg)

The cramped freshman campus dorm room did not stop us from building a mini
test track as we utilized all the ground space for building and testing.
To make ourselves look cool we even designed a Hollywood-ish debugging
telemetry interface.

<div class="video-responsive">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/BKbY5qfer1A" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<br>

## Development

To have the ability to iterate quickly thorugh designs given of the
limited time we had, we chose to build our chassis using LEGO Mindstorms
EV3 kit components.

![Hardware Versions](/assets/img/proj/theflashsudo/chassis_compare.jpg)

The hardware and software development happened concurrently. Once we had
working chassis prototype we immediately
took it to the track for some field testing. We discovered early that
the wheeled chassis had problems maneuvering on the concrete ground, so
we headed back and designed a second generation chassis which greatly
improved the mobility of our robot.

![Design Render](/assets/img/proj/theflashsudo/chassis_render.png)
<small>
  Model designed in LEGO LDD (deprecated) and rendered in BrickLink
  Studio 2.0.
</small>

We realized early that the white lines on the ground have a low contrast
against grey concrete, so light sensors were not an option. We decided
to use a RaspberryPi and RGB camera to detect the lines and control the
robot. To interface with LEGO motors we used a BrickPi interface board.
For the power, we opted for a high performance LiPo battery regulated
by two DC-DC buck converter to supply two power rails (5v for RasPi
and 9v for the motors).

The project is open source and code + hardware CAD can be found in our
GitHub repository:

<a class="github-button" href="https://github.com/harveybia/the-flash-sudo" data-color-scheme="no-preference: light; light: light; dark: dark;" data-size="large" data-show-count="true" aria-label="Star harveybia/the-flash-sudo on GitHub">the-flash-sudo</a>

## Results
First place among undergraduates (we believe we beat graduate participants too
but we were placed in different brackets), completing 11 gates in 4 minutes.
We were awarded a prize of $1,000 as a team.
Watch the full competition here:

<div class="video-responsive">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/ja-ICS9NzA0?start=251" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<br>

[mobot_homepage]: https://www.cs.cmu.edu/mobot/index.html
[video_link]: https://youtu.be/ja-ICS9NzA0?t=251
[justin_c]: https://www.justinchuby.com
