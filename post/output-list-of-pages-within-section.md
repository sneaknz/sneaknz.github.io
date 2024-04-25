---
title: Output list of pages within section
date: 2016-04-22
tags:
  - supermodel
  - navigation
---

~~~java
<ul>
    <sm:ancestor var="_section" classCodes="AbstractSection"/>
    <sm:forEach name="_section" field="pages" var="_page">
        <li<sm:if test="${object eq _page}"> class="selected"</sm:if>><a href="<sm:url name="_page"/>"><sm:out name="_page"/></a></li>
    </sm:forEach>
</ul>
~~~

Note that if you are using namespaced parent slugging then the `<sm:ancestor />` part of this is likely unnecessary, as the routing will also set up a variable for the parent which you can reference (e.g. `name="section"`).
