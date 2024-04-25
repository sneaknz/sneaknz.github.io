---
title: Imagemagick command to assemble images into a sprite
date: 2016-03-21
tags:
  - terminal
  - imagemagick
  - images
---

Change the dimensions and tile layout to suit the size of images and number of rows/columns you desire.

~~~shell
montage -background transparent -geometry 1500x344+0+0 -tile 4x13 *.png sprite3.png
~~~
