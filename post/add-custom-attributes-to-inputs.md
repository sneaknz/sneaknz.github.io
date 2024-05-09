---
title: Add custom attributes to Supermodel inputs
date: 2024-05-10
tags:
  - supermodel
---

To add custom attributes to an `<sm:input />` field, you can use the `attributesText` property:

~~~html
<input:text className="field" id="fieldname" name="fieldname" attributesText="data-id='1234' data-another-value='blah'" />
~~~
