---
title: Create a tag file in Supermodel
date: 2016-05-06
tags:
  - supermodel
  - templates
---

Format the tag content like this, and include any relevant attributes:

~~~html
<%@tag %>
<%@include file="/WEB-INF/templates/frag/global.jspf" %>
<%@attribute name="object" required="true" rtexprvalue="true" type="java.lang.Object" %>
<%@attribute name="something" required="false" rtexprvalue="true" type="java.lang.String" %>
<%@attribute name="test" required="false" rtexprvalue="true" type="java.lang.Boolean" %>

[ ... tag template code here, e.g. <sm:out name="something" /> ]
~~~
