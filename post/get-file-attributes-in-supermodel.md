---
title: Get file attributes in Supermodel
date: 2016-04-25
tags:
  - supermodel
  - files
---

~~~html
<sm:asset var="_file" name="download" field="file"/>
<sm:if name="_file">
	<sm:set var="_filename" name="download" field="name"/>
	<sm:ifNot name="download" field="name">
		<sm:set var="_filename" value="${_file.file.name}"/>
	</sm:ifNot>
	<a href="<sm:out name="_file" field="url"/>"><sm:out name="_filename" /> (${_file.fileSizeString} ${_file.suffix})</a> 
</sm:if>
~~~
