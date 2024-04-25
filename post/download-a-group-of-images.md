---
title: Download a group of images
date: 2016-08-22
tags:
  - terminal
---

Use Terminal to download images from a group of URLs specified in a carriage-returned list within a text file. Open Terminal, navigate into the folder containing the text file, then run this command:

~~~shell
xargs -n1 curl -O textfilename
~~~

The above hasn&rsquo;t always worked for me, but in those cases the following did the same trick:

~~~shell
cat textfilename | xargs -n 1 curl -O
~~~
