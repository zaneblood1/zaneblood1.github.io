---
layout: page
title: Sorting Algorithms
description: A Graphical User Interface written in Processing which allows the user to shuffle a random array of columns and then visualize different sorting algorithms in real time.
img: assets/img/sorting.png
importance: 2
category: fun
---

In this project I built a GUI in the Processing language which animates 9 classical sorting algorithms. I was inspired by the Coding Train's YouTube video about Mergesort, so I decided to expand upon it. The repository can be found <a href = "https://github.com/zaneblood1/sorting-algorithms-animation">here</a> so feel free to give it a try for yourself. When the program is up and running the user can press down on the shuffle button to generate a new random sequence of array elements. Then different sorting algorithms such as Quicksort, Mergesort, Selection Sort, etc. can be selected from and the algorithm is animated in real time with a red bar indicating the element currently being processed in the array.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/mergesort.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/shakersort.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Mergesort is visualized on the left and cocktail shaker sort on the right. Cocktail shaker sort is one of my favorite algorithms to watch even if it is not as efficient as Mergesort, and I think it is clear to see why it was given the name it has!
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/insertionsort.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/heapsort.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A brute force insertion sort method is shown on the left and heap sort is animated on the right. Notice how the other algorithms can go through multiple sorting cycles in the same amount of time it takes insertion sort to complete just one loop. This is related to the fact that insertion sort is an order N-squared operation. 
</div>

Besides the 4 algorithms shown here on this page, the GUI also let's the user play around with some less familiar options like Gnome sort or Pancake sort. However, I think the 4 shown here are the most visually unique. Note that animating an iterative algorithm such as selection sort is straight-forward since each frame in the animation just corresponds to a single iteration of the for-loop; however, animating a recursive algorithm is a little less intuitive. Doing so requires using a multi-threaded approach to store the state of the array at any given level in the recursive call. 

