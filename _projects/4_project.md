---
layout: page
title: Quantum Billiards
description: A Crank-Nicholson simulation of a 2D game of quantum billiards
img: assets/img/billiards.png
importance: 3
category: fun
---

The animation below shows a simulation of a 2D Gaussian wave packet with an initial 45 degree velocity contained within an infinite square potential. As the wavepacket hits the corner it spreads out and start interacting with itself creating regions of positive and negative interference. This simulation was written in Jupyter Notebooks using the Crank-Nicholson method for evolving quantum systems numerically. You can download the repository <a href="https://github.com/zaneblood1/Schrodinger-Equation-Animated">here</a> and mess around with the code yourself.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/quantum_billiards.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

In the future I would like to make this fully 3-D and run a few simulations on different geometries such as a hard shell sphere or a cubic crystal of discrete lattice points. It would also be interesting to add multiple initial wave-packets and essentially simulate a true game of quantum pool. This is probably one of my favorite projects I have done visually, and I think it is really cool to watch the system oscillate through the various modes it cycles through. 
