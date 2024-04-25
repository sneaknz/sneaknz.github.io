---
title: Redirect to first page in section
date: 2016-07-28
tags:
  - supermodel
---

~~~html
<%@include file="/WEB-INF/templates/frag/global.jspf" %>
<sm:url var="_url" name="object" field="pages" index="0" addContextPath="false"><sm:attribute name="section" value="${object}" /></sm:url>
<c:redirect url="${_url}" />
~~~

Where `section` in this instance is the variable set up by the routing rules.
