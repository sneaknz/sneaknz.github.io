---
title: Convert images to an animated GIF
date: 2019-10-02
tags:
  - terminal
---

If you have ImageMagick installed you can use Terminal to convert a folder of images into an animated GIF. In Terminal, `cd` into the folder where your images are kept and then run the following script (modifying to suit):

~~~shell
convert -delay 10 -loop 0 *.png animated.gif
~~~

You can adjust the delay value to speed up or slow down the animation, and edit `*.png` to match your image naming/type (e.g it may be something like `source-*.jpg`). It can be a good idea to number your frame images to ensure proper ordering.

Note: the script above will layer each successive image on top of the previous, so if you are working with transparent images you may want to adjust it slightly so that the frame is wiped on each pass first:

~~~shell
convert -delay 10 -loop 0 *.png -set dispose background animated.gif
~~~
