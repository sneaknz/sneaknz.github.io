---
title: Generate sitemap.xml
date: 2020-08-05
tags:
  - supermodel
---

To generate an automated sitemap file, uncomment the following code in the `actions-config.xml` file and edit to suit your field structure:

~~~xml
<action class="SitemapAction">
	<mapping url-pattern="/main/sitemap.xml"/>
	<mapping url-pattern="/sitemap.xml"/>
	<init-param>
		<param-name>root</param-name>
		<param-value>im_root</param-value>
	</init-param>
	<init-param>
		<param-name>fieldCodes</param-name>
		<param-value>navigation,footerNavigation,pages,products,customers,links,posts</param-value>
	</init-param>
	<init-param>
		<param-name>classCodes</param-name>
		<param-value>AbstractNavigable,FooterLinkGroup</param-value>
	</init-param>
	<init-param>
		<param-name>hiddenClassCodes</param-name>
		<param-value>Site,FooterLinkGroup</param-value>
	</init-param>
</action>
~~~
