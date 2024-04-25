---
title: Create a list object in Supermodel
date: 2017-01-15
tags:
  - supermodel
---

Useful when you want to create a subset of values, for instance when needing to filter output and then do something with it.

~~~html
<list:empty name="listName"/>
<sm:forEach field="items" var="_item">
	<list:add list="${listName}" value="${_item}"/>
</sm:forEach>
~~~
