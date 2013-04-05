---
layout: post
title: "Rename Multiple Files At Once"
date: 2013-04-05 12:46
comments: true
categories: 
---
As an iOS developer, sometimes you may want to rename the following files

- header02.png
- header02@2x.png
- header02_down.png
- header02_down@2x.png

to

- header-backbtn.png
- header-backbtn@2x.png
- header-backbtn_down.png
- header-backbtn_down@2x.png

Try this command:
```
for file in header02*; do mv $file ${file/header02/header-backbtn}; done
```

