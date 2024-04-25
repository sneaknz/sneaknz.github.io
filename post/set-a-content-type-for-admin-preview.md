---
title: Set a content type for admin previews
date: 2020-11-18
tags:
  - supermodel
---
                
Often when editing content in Supermodel you will be editing an object that lives inside a larger page, and so doesn&rsquo;t have its own page template for viewing. This means when you use the &lsquo;Preview&rsquo; button in Supermodel there is nothing to show and you generally get an error page, which can be confusing for users. The solution is to explicitly set content types that <em>can</em> be previewed. When this configuration is added, any time you try to preview an object it will check to see if it is one of those content types, and if not then it will look up the chain at all parents until it finds the first one that does match, and use that to display as the preview template.

To set this configuration, add the following line to your `supermodel.properties` file:

~~~shell
supermodel.displayable.class=im:Displayable
~~~

Where `im:Displayable` here would match the model type for templates you want to match. This can be a comma-separated list.
