---
title: Static images in the sm:image tag
date: 2018-07-29
tags:
  - supermodel
  - images
---

This is how you can reference a static image asset inside the `<sm:image />` tag, which can be useful when defining fallback images etc.

~~~html
<sm:image value="/static/img/home-hero-placeholder.png" staticAsset="true" ... />
~~~
