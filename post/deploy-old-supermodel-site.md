---
title: Deploying an old Supermodel site from an M-series Mac
date: 2024-05-08
tags:
  - supermodel
  - terminal
---

For some of our older Supermodel sites you won't be able to run the deploy script successfully because the sites require and older version of Java. To fix this issue you need to tell the deploy to use Java 8 instead of whatever more current version you are running on your machine:

~~~shell
export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)
~~~
