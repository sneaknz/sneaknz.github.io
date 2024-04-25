---
title: Test whether you are in a dev Supermodel environment
date: 2016-10-05
tags:
  - supermodel
---

First add this import to the top of your page:

~~~html
<%@page import="com.cactuslab.supermodel.Application"%>
~~~

Then you can test against the `Application.isDevMode()` value.

~~~html
<% if (Application.isDevMode()) { ... } %>
~~~
