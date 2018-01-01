---
date: "2017-12-30T13:52:53-06:00"
title: "Dowloading all presentations from Kubecon 2017 "
authors: []
categories:
  - Conferences
tags:
  - KubeCon
  - presentations
draft: false
cover: 
  image: https://raw.githubusercontent.com/cncf/landscape/master/landscape/CloudNativeLandscape_latest.jpg
  caption: CNCF landscape as of December 2017
  style: full
---

North American part of Kubecon 2017 was held in Austin, TX on December 4-6.
Below are some useful links related to the event.


https://lwn.net/Articles/741301/ - event report from LWN.

https://lwn.net/Articles/741897/ - short overview of  different container runtimes

Videos from the conference are available on official CNCF [YouTube channel] (https://www.youtube.com/watch?v=Z3aBWkNXnhw&list=PLj6h78yzYM2P-3-xqvmWaZbbI1sW-ulZb)

[KubeCon + CloudNativeCon North America schedule]
(https://kccncna17.sched.com/) has links to presentations for about half of the talks.
 
Below are the steps to download all available PDF:
<pre>
  <code class="language-bash">
lynx -cache=0 -dump -listonly https://kccncna17.sched.com/list/descriptions/ > links.txt
cat links.list | grep pdf | cut -d '.' -f2-  >> pdf.txt
wget -i pdf.txt
  </code>
</pre>

and PPT files:

<pre>
  <code class="language-bash">
lynx -cache=0 -dump -listonly https://kccncna17.sched.com/list/descriptions/ > links.txt 
cat links.list | grep ppt | cut -d '.' -f2-  >> ppt.txt
wget -i ppt.txt 
  </code>
</pre>

The commands are self-explanatory, another option would be to use browser's javascript console to generate same list.
(*No idea how to do that, though*)
