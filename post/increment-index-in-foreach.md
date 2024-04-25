---
title: Increment index inside sm:forEach
date: 2016-04-30
tags:
  - supermodel
---

~~~html
<sm:forEach name="whatever" varStatus="_status">
  New index is: <sm:out value="${_status.index+1}" />
</sm:forEach>
~~~                
