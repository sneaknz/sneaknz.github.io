---
title: Start a simple server from Terminal
date: 2016-04-28
tags:
  - terminal
  - python
  - server
---

As of macOS Monterey 12.3 Python 2 no longer comes pre-installed with the OS, so you will need to install Python 3 (`brew install python`) if not already installed. You can then run a simple server by navigating to the folder in terminal and entering:

~~~shell
python3 -m http.server 8080
~~~

You can change the port number at the end to avoid clashes with any other services running. For machines running Python 2 you can use this command:

~~~shell
python -m SimpleHTTPServer 8080
~~~
