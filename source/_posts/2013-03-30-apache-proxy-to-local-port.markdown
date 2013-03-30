---
layout: post
title: "Apache Proxy to Local Port"
date: 2013-03-30 17:11
comments: true
categories: [apache, proxy]
---
```
<VirtualHost *>
        ServerName www.example.com
        ProxyPass / http://localhost:3000/
        ProxyPassReverse / http://localhost:3000/
        ProxyPreserveHost On
</VirtualHost>
```
