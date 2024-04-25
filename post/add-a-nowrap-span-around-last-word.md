---
title: Add a ‘nowrap’ span around last word and following element
date: 2014-05-13
tags:
  - supermodel
  - formatting
---

This is useful for times where there may be a count value at the end of a title, and you don’t ever want the count to be split from the last word (where it can wrap down to the next line all by itself).

~~~html
<h2>
    <set var="_encoded"><out name="_item"></out></set><out name="_encoded" format="none"><sm:transform pattern="^(.*\s)?([^\s]+)$" replaceFirst="$1<span class='nowrap'>$2" /></out><small class="count">${fn:length(_item.value)}</small>
</h2>
~~~

The accompanying CSS style needs to be added for the .nowrap class.