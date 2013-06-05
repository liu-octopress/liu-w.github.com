---
layout: post
title: "Mac ip forwarding"
date: 2013-06-05 18:38
comments: true
categories: [mac, route, ip, forward]
---
My mac's internet sharing is not working. After a few days of googling and fiddling with the command lines, I found a solution to fix it.  
en0 is the ethernet; en1 is wifi
```
sudo ipfw add divert natd all from any to any via en0
sudo ipfw add divert natd all from any to any via en1
sudo natd -interface en0 
```