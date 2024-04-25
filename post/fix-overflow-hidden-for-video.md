---
title: Fix overflow:hidden for video
date: 2017-11-29
tags:
  - css
---

This fixes issues where overflow hidden doesn&rsquo;t work on elements in Webkit browsers (e.g. using border-radius to crop the edges of a video). Apply this mask to the containing `overflow:hidden` element.

~~~css
-webkit-mask-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAIAAACQd1PeAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAA5JREFUeNpiYGBgAAgwAAAEAAGbA+oJAAAAAElFTkSuQmCC);
~~~
