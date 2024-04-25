---
title: Add namespaced routing for pages in sections
date: 2016-04-22
tags:
  - supermodel
  - routes
---

In routes.xml:

~~~xml
<route>
	<object name="object" class-code="AbstractPage" slug-parent="section" slug-space="pages"/>
	<object name="section" class-code="AbstractSection" child="object" />
	
	<route pattern="/{section}/{object}/" path="/object/default"/>
</route>
~~~

In configuration for page object in Supermodel model:

~~~shell
slug.space=pages
slug.parentClass=AbstractSection
slug.parentField=pages
~~~
