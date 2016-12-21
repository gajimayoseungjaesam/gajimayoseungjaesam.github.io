---
layout: post
title:  "Overlay Tricks"
categories: Advanced Bluebeam
---

Batch overlay is a great Bluebeam tool but it merely just overlays pages as they are with out selecting line up points. This works fine when the Architect has not shifted anything around, but this is not always the case. 

Here we will learn how to fix this issues manually after having done a batch overlay. For practical purposes, I simply did a two page overlay with out selecting any points. As you can see the building was shifted therefore, we must fix the issues. 

{% include image.html image="overlay-tricks_1.gif" class="img-xlarge" %}

## The Fix

1. Hide one of the layers by going to the layers tab in the left panel
2. Take a snapshot of the building. 
3. Paste In Place 'cnt + shift + v'
4. Hide the current visible layer and unhide the hidden layer
5. Delete the layer on which we took the snapshot. This layer is not needed anymore since we have a snapshot of the layer already
6. Move the snapshot markup to line up with the layer below. Use the up and down arrow keys for extra precision 
    {% include image.html image="overlay-tricks_2.gif" class="img-xlarge" %}