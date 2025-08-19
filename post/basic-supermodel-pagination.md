---
title: Basic Supermodel pagination
date: 2025-08-19
tags:
  - supermodel
---

This is a simple implementation of pagination, with previous/next links and numbered pages. The `howMany` value of the `<sm:paginate />` tag determines how many items per page will be ouput, and the `windowSize` variable determines how many pages either side of the current one will be displayed in the page link list. Where there are more pages than those available, and ellipsis will be output.

The code below contains minimal CSS classes, so it will be up to you to style the output correctly.

~~~html
<sm:paginate field="items" howMany="10" sort="date desc" var="_paginator" page="${empty param.page ? 0 : param.page - 1}" />
					
<sm:forEach paginator="_paginator" var="_item">
	[ output conten items here ]
</sm:forEach>						

<sm:ifNot name="windowSize"><sm:set var="windowSize" value="3"/></sm:ifNot>
<sm:choose>
	<sm:when test="${_paginator.pageCount < (1 + ( 2 * windowSize ))}">
		<sm:set var="_firstPage" value="0"/>
		<sm:set var="_lastPage" value="${_paginator.pageCount - 1}"/>
	</sm:when>
	<sm:otherwise>
		<sm:set var="_firstPage" value="${_paginator.pageIndex - windowSize  < 0 ? 0 : _paginator.pageIndex - windowSize}"/>
		<sm:set var="_lastPage" value="${_paginator.pageIndex + windowSize < _paginator.pageCount ? _paginator.pageIndex + windowSize : _paginator.pageCount - 1}"/>
	</sm:otherwise>
</sm:choose>
<sm:if test="${_paginator.pageCount > 1}">
	<nav class="pagination">
		<a href="?page=${_paginator.pageIndex + 0}"<sm:if test="${_paginator.pageIndex eq 0}"> disabled</sm:if>>
			Previous
		</a>
		
		<div class="pages">
			<sm:if test="${_firstPage > 0}">
				<a href="?page=1">1</a>
				<sm:if test="${_firstPage > 1}">...</sm:if>
			</sm:if>
			<sm:forEach start="${_firstPage}" end="${_lastPage}" varStatus="_status">
				<sm:choose>
					<sm:when test="${_status.index == _paginator.pageIndex}">
						<span>${_status.index + 1 }</span>
					</sm:when>
					<sm:otherwise>
						<a href="?page=${_status.index + 1}">${_status.index + 1 }</a>
					</sm:otherwise>
				</sm:choose>
			</sm:forEach>
			<sm:if test="${_lastPage < _paginator.pageCount - 2}">...</sm:if>
			<sm:if test="${_lastPage < _paginator.pageCount - 1}">
				<a href="?page=${_paginator.pageCount}">${_paginator.pageCount}</a>
			</sm:if>
		</div>

		<a href="?page=${_paginator.pageIndex + 2}"<sm:if test="${!_paginator.next}"> disabled</sm:if>>
			Next
		</a>
	</nav>
</sm:if>
~~~

See the [previous instructions]({{ '/post/supermodel-wysiwyg-config-options' | url }}) if you need more detailed configuration.