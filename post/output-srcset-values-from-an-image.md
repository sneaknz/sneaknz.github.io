---
title: Output srcset values from an image
date: 2018-08-02
tags:
  - supermodel
---

To generate a comma-delimited list of images generated for the `srcset` of an image, loop through them with a `forEach` statement:

~~~html
<sm:image field="image" 
  maxWidths="1980, 990, 500"
  var="_img"
/>

<sm:forEach name="_img" var="_i" varStatus="_s"><sm:url name="_i"/><sm:ifNot name="_s" field="last"/>,</sm:ifNot></sm:forEach>
~~~

This would generate a list of images in the format `/img/size-1980.jpg, /img/size-990.jpg, /img/size-500jpg`, which is useful if you need to add them as data attributes for reference in javscript.
