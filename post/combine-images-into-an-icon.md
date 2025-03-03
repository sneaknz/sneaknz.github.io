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

**Note:** since the most recent system update that uses ImageMagick 7 you now need to preface the command with 'magick' instead of 'convert': 

~~~shell
magick 16.png 32.png 48.png 256.png favicon.ico
~~~

Depending on the colour profile of the PNG files you will sometimes get the error `magick: Cannot write image with defined png:bit-depth or png:color-type`. In this case you can add the `-compress none` option:

~~~shell
magick -compress none 16.png 32.png 48.png 256.png favicon.ico
~~~