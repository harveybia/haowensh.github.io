---
layout: default
---

<pre class="highlight">
🔔 Check out the new <a href="#projgallery">project gallery</a>!
</pre>

# About Me

I am interested in **Robotics**, **Computer Engineering**
**System Engineering** and basically anything computer related
(except compilers, which are black magic to me).

I received a Bachelor of Science degree in [ECE][ece_link]
(Electrical and Computer Engineering) with
[Additional Major in Robotics][robo_major_link] from
[Carnegie Mellon University][cmu_link] (2015-2019).

I am currently pursuing [Master of Science in Robotics][msr_link] at CMU working
for [Howie Choset][howie_choset] under the [Biorobotics Lab][bio_link]
(2019-2021).

* * *

# Work Experiences

### Apple Inc.
* 2018 Summer Intern: macOS Performance Team
* 2019 Summer Intern: CoreOS Performance Tools & Infrastructure Team

### Carnegie Mellon University
* Research Assistant: Boeing [Blaser][blaser] Project

* * *

# Recent

## Undergraduate Capstone Design Projects

I took two capstone design classes in my senior year for ECE and Robotics
respectively. Both of the two projects came out great and I learned invalueable
experiences in project management, system engineering and teamwork along the
way.

### 18-578 Mechatronic Design

![Team JollyRoger](/assets/img/2019/capstone/jolly_roger_team.jpeg)

Project ShipBot, Team [JollyRoger][jolly_roger]

### 16-474 Robotics Capstone

![Team Monkey](/assets/img/2019/capstone/monkey_team.jpeg)

Robotic Jogging Companion (aka. robomonkey), Team [Monkey][robo_monkey]

<a name="projgallery"></a>
* * *

# Project Gallery

{% assign proj_sorted = site.projects | sort: 'rank' %}
<div class="card-group">
  {% for proj in proj_sorted %}
    <div class="card"  onclick="location.href='{{ proj.url }}#title';" style="cursor: pointer;">
      <img class="card-img-top" src="{{ proj.thumbnail }}" alt="Card image">

      <div class="card-body">
        <h2 class="card-title">{{ proj.name }}</h2>
        <p class="card-text">{{ proj.description }}</p>
      </div>
      <div class="card-footer">
        <small class="text-muted">{{ proj.time }}</small>
      </div>
    </div>
  {% endfor %}
</div>

# Resume
Last updated: *May 2020*\\
[Grab my resume here!][resume_link]

[ece_link]: https://www.ece.cmu.edu
[robo_major_link]: https://www.ri.cmu.edu/education/academic-programs/undergraduate-options/
[cmu_link]: https://www.cmu.edu
[howie_choset]: https://en.wikipedia.org/wiki/Howie_Choset
[msr_link]: https://www.ri.cmu.edu/education/academic-programs/master-of-science-robotics/
[bio_link]: http://biorobotics.ri.cmu.edu/index.php
[blaser]: http://biorobotics.ri.cmu.edu/research/ConfinedSpacePerception.php
[jolly_roger]: https://sites.google.com/view/cmu-jollyroger
[robo_monkey]: https://www.youtube.com/watch?v=4T_pGsnyUNg

[resume_link]: /assets/files/Haowen_Shi_Resume_S20.pdf
