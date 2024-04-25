---
title: Using a test to restrict forEach results
date: 2016-05-31
tags:
  - supermodel
---
 
~~~html
<sm:forEach field="things" var="_thing" test="!empty _thing.values.fieldname">
    ...
</sm:forEach>
~~~

Note that the test does not require `${ }` wrappers like you would usually use in test attributes.
