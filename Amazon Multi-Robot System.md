---
layout: page
title: Amazon Multi-Robot System
---

<br />

<!-- This was a project created for a year-long mechanical engineering capstone assignment in a senior design course.

As a team of four, we investigated floor robots and their application in carrying arbitrary loads. Our concept for such a system was a collection of identical collaborative robots, each similar in size to a Roomba. Combined, they would constitute a MRS that could be tasked to transport previously unknown objects of various sizes, loads, and geometries through a warehouse environment. Our MRS can be loaded with an object, and directed to an end position. Given perception and load sensing capabilities, the MRS may additionally adjust itself dynamically to best control its cargo, avoid collisions, and ensure safe transport. -->
In a team of four, we developed a multi-robot system capable of transporting loads of various shape and size in a warehouse.  We designed and built out two iterations, with the final prototype system consisting of three robots.

![bot]({{ BASE_PATH }}/public/images/bot.png)

<video muted autoplay align="left" width="45%" controls>
  <source src="{{ BASE_PATH }}/public/images/demo.mp4" type="video/mp4"></source>
</video>

<video muted autoplay align="right" width="45%" controls>
  <source src="{{ BASE_PATH }}/public/images/demo2.mp4" type="video/mp4"></source>
</video>



Much of current warehouse automation focuses on structured, repeatable tasks, often partitioned from human workers; the motivation for this project was to design a scalable, human-collaborative solution for an unstructured warehouse process.  After independent research on Amazon’s warehouse workflow, we decided to target transportation of bulky items that are handled in their ‘non-sortable’ fulfillment centers. We wrote a technical proposal, presented it to Amazon Robotics, and received funding to build out prototypes for our senior design project at Boston University.  

![mrs_couch](_portfolio/public/images/mrs_couch.png)

The primary command input of the system is compliant guidance: a human lightly pushes the loaded object, and the robot senses and moves proportional to that force vector, contributing the majority of the force necessary to transport the object. Each robot can carry up to 15 kg on level ground at approximate human walking speed of 1.5 m/s. To allow for holonomic movement of the load, and avoid overconstraining the system, the loading platform rotates freely with respect to the robot.

![compliance]({{ BASE_PATH }}/public/images/compliance.gif)




```
The compliant loading mechanism of the robot: four 20kg strain gauge  load cells resolve a push force into its vector components.
```
</br>

I took the lead on design of the drivetrain.





<!-- My role in this project was to lead the design and development of the drivetrain and chassis. -->
