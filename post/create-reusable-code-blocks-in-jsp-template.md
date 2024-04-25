---
title: Create re-usable code blocks within a JSP template
date: 2020-11-19
tags:
  - supermodel
---

Sometimes you may have a block of code that you would like to output in multiple places in the page, and for whatever reason don&rsquo;t want to use includes or tags. To do this you can use the <code>&lt;sm:block /&gt;</code> feature. To start you set the block as a variable:

~~~html
<sm:setBlock var="_blockname">
	...
</sm:setBlock>
~~~

Then later in the page you can output it:

~~~html
<sm:block name="_blockname" />
~~~
