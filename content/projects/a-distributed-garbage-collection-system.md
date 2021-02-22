---
title: "A Distributed Garbage Collection System"
description: "Fourth Year Design Project"
date: "2015-02-13T00:00:00-08:00"
slug: "a-distributed-garbage-collection-system"
github: "https://github.com/j43cheun/FYDP.git"
tags: [ "ATmega328P", "Bootstrap", "C", "C++", "CSS", "Google Maps", "HTML", "Java", "JSP", "JavaScript", "k-means++", "MRTA", "MySQL", "Node.js" ]
---

**A Distributed Garbage Collection System** was my group's Fourth Year Design
Project for Electrical and Computer Engineering (ECE) at the University of
Waterloo. For our project, we chose to tackle the problem of littering from an
engineering standpoint. Our rationale for the accumulation of litter was that
garbage bins are distributed suboptimally within a given area.

Our project sought to solve this littering problem through the design and
implementation of a crowd-sourced data-driven management system for allocating
garbage bins within a given area. This solution consisted of 2 components: the
garbage bin embedded system and the garbage bin management server. The garbage
bin embedded system would be used to gather sensor data about a garbage bin,
while the garbage bin management server would be used to manage the distribution
of garbage bins in the area based on garbage bin sensor data and crowd-sourced
littering GPS coordinates. Our solution was partially inspired by the cleaning
robots from [A Certain Scientific
Railgun](https://en.wikipedia.org/wiki/A_Certain_Scientific_Railgun).

In our prototype, each garbage bin was outfitted with an [Adafruit Ultimate GPS
Breakout](https://www.adafruit.com/product/746) GPS sensor, an
[HCSR04](https://www.sparkfun.com/products/15569) ultrasonic distance sensor, a
[TMP36](https://www.sparkfun.com/products/10988) temperature sensor, an
[ATMega328P](https://www.microchip.com/wwwproducts/en/ATmega328P)
microcontroller, and a [Raspberry Pi](https://www.raspberrypi.org). The GPS
sensor was used to determine the current position of the garbage bin, while the
sonar and temperature sensors were used to determine how full the garbage bin
was. These sensors were driven by the ATMega328P microcontroller, which was in
turn driven by the Raspberry Pi. The Raspberry Pi was used to send sensor data
about the garbage bin back to the garbage bin management server. It ran a
Node.js server to service GET requests for the garbage bin sensor data.

Our prototype garbage bin management server consisted of three submodules: the
[MySQL](https://www.mysql.com) database, the
[JSP](https://projects.eclipse.org/projects/ee4j.jsp) web server, and the web
frontend. The MySQL database was used to keep track of registered garbage bins
and crowd-sourced littering GPS coordinates. The JSP web server served as the
backend for the web frontend. It was used to run garbage bin allocation
algorithms (based on k-means++ clustering and multi-robot task allocation) using
crowd-sourced littering GPS coordinates and garbage bin sensor data to figure
out where to allocate each registered garbage bin in the area. The web frontend
was implemented using the [Bootstrap](https://getbootstrap.com) CSS framework
and featured a Google Maps interface and a simple form for visualizing the
distribution of crowd-sourced littering positions and the distribution of
registered garbage bins in the area, adding new littering GPS coordinates, and
managing registered garbage bins.

<div class="columns mt-5">
  <div class="column">
    <img src="/projects/a-distributed-garbage-collection-system/img/garbage-bin-embedded-system.jpg">
  </div>
</div>

<div class="columns mt-5">
  <div class="column">
    <img src="/projects/a-distributed-garbage-collection-system/img/poster.png">
  </div>
</div>
