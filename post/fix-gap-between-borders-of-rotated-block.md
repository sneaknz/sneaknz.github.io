---
title: Fix gap between borders of a rotated block element
date: 2016-08-09
tags:
  - css
---

When rotating a block element with borders on two edges by 45º (e.g. to create a chevron shape), sometimes where the borders meet there is a white gap. Adding a `translate3D` value (in particular having the Z value) seems to fix this.

~~~css
transform: translate3D(0, 0, 0) rotate(45deg);
~~~
