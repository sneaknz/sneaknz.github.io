---
title: Pass attributes to a Supermodel include
date: 2025-07-09
tags:
  - supermodel
---

When uaing `<sm:include>` to output a collection of data, it is possible to pass attributes that can be used by the included templates:

~~~html
<sm:include field="blocks" page="/object/blocks/default">
  <sm:attribute name="theme" value="dark" />
  <sm:attribute name="parent" value="${object}" />
</sm:include>
~~~
