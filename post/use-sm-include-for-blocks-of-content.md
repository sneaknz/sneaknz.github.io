---
title: Use sm:include for blocks of content
date: 2016-05-03
tags:
  - supermodel
  - templates
---

E.g. Store templates for each content type in `/object/block/` and then add into main page like this:

~~~html
<sm:include field="blocks" page="/object/block/default" />
~~~

This will iterate through all the objects in your collection and output the content using the matching template found in the folder specified by the `page` attribute.

You can optionally pass attributes which will be used by the includded file, which means includes may be used instead of tags in some cases:

~~~html
<sm:include field="blocks" page="/object/block/default">
  <sm:attribute name="mycontent" value="..." />
</sm:include>
~~~
