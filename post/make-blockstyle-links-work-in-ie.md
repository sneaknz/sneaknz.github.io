---
title: Make block-styled links work in old IE
tags:
  - css
  - ie
  - hack
---

For when you have a link in your page styled as a block element, and the area of the link is not clickable in IE. Turns out adding a transparent background somehow makes it clickable.

~~~less
.lte9 & {
	/* Hack because IE doesn't show link as clickable */
    background: url('data:image/gif;base64,R0lGODlhAQABAPAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==');
}
~~~

A sure telltale sign is if, when you have a border added, you can click the border but not the interior area. No idea why this happens, probably because IE...