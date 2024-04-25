---
title: Combine images into an icon
date: 2018-10-23
tags:
  - terminal
---

Use Terminal to combine multiple PNG images into a single .ico icon file. Open Terminal, navigate into the folder containing the image files, then run this command:

~~~shell
convert 16.png 32.png 48.png 256.png favicon.ico
~~~
