---
title: Output slug for an object
date: 2019-07-17
tags:
  - supermodel
---

To output the Supermodel slug for any slugged object, you can use the following syntax:

~~~html
${object:slug(object)}
~~~

Where the `object` in parenthesis is the object you wish to obtain the slug for.

If you find it&rsquo;s not working, check that the following line exists in `globals.jspf`:

~~~html
<%@ taglib prefix="object" uri="http://www.supermodel.co.nz/tld/object" %>
~~~
