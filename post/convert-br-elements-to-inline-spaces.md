---
title: Convert <br> elements to inline spaces
date: 2016-11-07
tags:
  - css
---

For when you want to remove a `<br>` so text runs inline. Using `display: none;` also removes the space, so if you are collapsing sentences this method is better (found in conversation [here](http://stackoverflow.com/questions/7596647/ignore-br-with-css)).

~~~css
br {
	content: " ";
	
	&:after {
		content: " ";
	}
}
~~~
