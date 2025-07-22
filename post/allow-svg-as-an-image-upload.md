---
title: Allow SVG as an image upload
date: 2025-07-26
tags:
  - supermodel
---

By default Supermodel does not allow you to upload an SVG into an `image` field type, but you can allow this by adding configuration for that field to specify all the allowed types:

~~~shell
allowedTypes=image/gif
allowedTypes=image/jpeg
allowedTypes=image/png
allowedTypes=image/svg+xml
allowedTypes=image/webp
~~~

Note that you can't only add the missing SVG type, you must include _all_ the types that you want available.
