---
layout: page
title: Bird Murmuration
description: An implementation of the Boid algorithm to simulate animal flocking behavior in 2D and 3D.
img: assets/img/boids.png
importance: 6
category: work
giscus_comments: true
---

The Boid algorithm simulates bird murmuration or other insect-like swarm behavior by giving inividual Boid-class objects a sense of cohesion (a tendency to want to group together), alignment (Boids want to fly in the same direction as the average center of mass velocity), and finally a sense of dispersion (individual Boids take up physical space and do not want to clump together into a single point). The simulation below shows two separate runs of a Boid implementation in both 2 and 3 dimensions. The code repository is linked <a href = "https://github.com/zaneblood1/Boid-Simulation">here</a> for your inspection.

<div class="row align-items-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/boids3D.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/boids2D.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
