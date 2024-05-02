---
title: Fixing DNS for a Gandi subdomain when using Github Pages
date: 2024-05-02
tags:
  - hosting
  - github
  - random
---

When trying to point a subdomain to Github Pages from a Gandi DNS, I managed to get the domain working but Pages wouldn't allow me to enable the SSL option. When using the Github assistant to troubleshoot the issue it told me that an A record existed, when in fact I had only added a CNAME record.

After some searching I [found this gist](https://gist.github.com/matt-bailey/bbbc181d5234c618e4dfe0642ad80297) which proved to be the answer — the default Gandi live DNS includes some items that _need to be deleted_ before Github Pages will be able to use SSL.
