---
title: Tell git to ignore changes
date: 2016-07-11
tags:
  - terminal
  - git
---

To tell git to ignore any current changes for a particular file, you can type the following command in Terminal (replacing `$FILE` with the name of the file):

~~~shell
git update-index --assume-unchanged $FILE
~~~

To reverse the change, you can alter the line as follows:

~~~shell
git update-index --no-assume-unchanged $FILE
~~~
