---
title: Wrapping an unknown number of elements with CSS grid
date: 2023-11-22
tags:
  - css
---

A technique using grid layout to handle the layout of multiple blocks on a page that need to wrap at different points as the browser size changes, using only a couple of lines of code and no media queries (a technique called &rsquo;[RAM](https://medium.com/@bogdanfromkyiv/ram-technique-in-css-90f092b105ae)&rsquo;)

~~~css
display: grid;
grid-template-columns: repeat(auto-fit, minmax(15em, 1fr));
~~~
