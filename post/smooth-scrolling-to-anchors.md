---
title: Smooth scrolling to anchors
date: 2021-10-05
tags:
  - css
---

For a CSS-only methode to provide smooth scrolling action to anchors, you can add the following:

~~~css
html {
	scroll-behavior: smooth;
}
~~~

It is good practice to also respect the users wishes if they want to avoid fast movement, so you can disable for those users by also adding:

~~~css
@media screen and (prefers-reduced-motion: reduce) {
	html {
		scroll-behavior: auto;
	}
}
~~~
