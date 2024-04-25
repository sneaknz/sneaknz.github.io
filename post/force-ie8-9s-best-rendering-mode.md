---
title: Force IE8/9’s best rendering mode
date: 2016-10-06
tags:
  - supermodel
---

Add the following to the start of your page, after the usual global Supermodel includes.

~~~html
<%response.setHeader("X-UA-Compatible", "IE=Edge"); %>
~~~
