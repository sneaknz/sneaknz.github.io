---
title: Format a 'double' field, show a single decimal if one exists
date: 2016-05-04
tags:
  - supermodel
---

Useful for working with currency in Supermodel, or when specific decimal places are required.

~~~html
<fmt:formatNumber value="${_object.values.fieldName}" pattern="#.#" />
~~~
