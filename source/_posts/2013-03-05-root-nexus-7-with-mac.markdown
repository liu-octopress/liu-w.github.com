---
layout: post
title: "Root Nexus 7 with Mac"
date: 2013-03-05 15:22
comments: true
categories: [Android, rooting] 
---
* Install android SDK if you have not.
* Download [SuperSU](http://download.chainfire.eu/310/SuperSU/UPDATE-SuperSU-v1.04.zip) and copy it to the root of Nexus 7's SD card.
* Download a [recovery image](http://download2.clockworkmod.com/recoveries/recovery-clockwork-touch-6.0.2.3-grouper.img)
* Boot Nexus 7 into fast boot mode.
* Flash the recovery image using the following command.
```
fastboot flash recovery recovery-clockwork-touch-6.0.2.3-grouper.img
```
* After the command is executed, choose Recovery option from the Fastboot menu and boot the device into Recovery Mode.
*  Then navigate to Install zip from SD card option and hit Power button to select it. Then use volume keys to navigate to UPDATE-SuperSU-v1.04.zip file in tablet's SD card and select it with Power button. 
* Reboot
