---
layout: page
title: Searching Algorithms
description: A second GUI written in Processing which allows the user to shuffle a random map of blocks and then visualize different searching algorithms in real time such as Djikstra's or DFS.
img: assets/img/searching.png
importance: 4
category: fun
---

The animation below shows Djikstra's algorithm being run on a random map to find the quickest path between two points. This GUI was written in Processing and allows the user to generate random maps and visualize different searching algorithms on these maps such as Breadth First Search, Depth First Search, or Priority Queue. You can download the code for yourself <a href = "https://github.com/zaneblood1/searchingVisualized">here</a>.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/djikstra.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Black blocks are obstacles, purple blocks are available paths, the white block is the start point and the red block is the destination. The user can randomly shuffle the map and generate new terrains. 
</div>

As you can see above, Djikstra's algorithm first starts with a Breadth First Search making note of the relative "cost" of all possible paths and then finally does a backwards pass where it uses the information it gained on the first pass to reconstruct the optimal path. Just like the quantum billiards simulation, I would like to make this fully 3D in the future. I would also like to add user input so that custom maps can be drawn out, and I think it would be a nice learning experience to investigate some other algorithms such as A-star.
