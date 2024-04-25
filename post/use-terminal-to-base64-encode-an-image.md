---
title: Use Terminal to base64 encode an image
date: 2016-06-05
tags:
  - terminal
  - base64
  - images
---

Generate base64 version of an image:

~~~shell
openssl base64 < path/to/file
~~~

Do the same, but remove line breaks:

~~~shell
openssl base64 < path/to/file.png | tr -d '\n'
~~~

Do the above, but copy the result to the clipboard:

~~~shell
openssl base64 < path/to/file.png | tr -d '\n' | pbcopy
~~~
