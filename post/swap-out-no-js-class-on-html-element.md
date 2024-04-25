---
title: Swap out 'no-js' class on HTML element
date: 2016-07-27
tags:
  - javascript
---

Add this into the `<head>` of your page to replace `.no-js` with `.js` when javascript is available (similar approach to Modernizr)

~~~html
<script>
	document.documentElement.className=document.documentElement.className.replace(/\bno-js\b/,'') + ' js'; // Set approprate js class on html element
</script>
~~~
