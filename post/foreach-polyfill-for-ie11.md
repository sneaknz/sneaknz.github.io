---
title: forEach polyfill for IE11
date: 2020-10-26
tags:
  - javascript
---

~~~js
if (window.NodeList && !NodeList.prototype.forEach) {
  NodeList.prototype.forEach = Array.prototype.forEach;
}
~~~
