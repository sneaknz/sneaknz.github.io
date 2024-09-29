---
title: Prevent faux bold or italics
date: 2024-09-30
tags:
  - css
  - fonts
---

The `font-synthesis` CSS property lets you specify whether or not the browser is allowed to synthesize the bold, italic, small-caps, and/or subscript and superscript typefaces when they are missing in the specified `font-family`. This is mostly important when fonts are included in a way where each weight is a separate file included using `@font-face` with the `font-weight` specified as `normal`, or if a font only has a single weight (i.e. a display font where bold and/or italics don‘t exist).

Setting `font-synthesis: none;` tells the browser not to create fake versions of bold/italics if they don‘t exist. A way to apply this across all your styles is to include this rule:

~~~shell
* {
	font-synthesis: none;	
}
~~~
