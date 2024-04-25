---
title: Basic WYSIWYG field config
date: 2023-08-02
tags:
  - supermodel
---

For adding basic configuration options so that only simple text is alowed in a field, add the following into the configuration for the field in Supermodel and adjust to suit.

~~~shell
tinyMCEConfig.height=150
tinyMCEConfig.toolbar=\"undo redo | bold italic | pastetext | link unlink | removeformat code\"
tinyMCEConfig.statusbar=false
tinyMCEConfig.valid_elements=\"p[class]\,em/i\,strong/b\,a[href|target|title]\,br\,span[class]\"
~~~

See the [previous instructions]({{ '/post/supermodel-wysiwyg-config-options' | url }}) if you need more detailed configuration.