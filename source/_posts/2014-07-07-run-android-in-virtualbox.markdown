---
layout: post
title: "Run Android in VirtualBox"
date: 2014-07-07 17:48
comments: true
categories: Android
---
Android emulator is VERY slow, because it emulates an ARM processor. 
## Install VirtualBox
Install VirtualBox if you have not. Download the binary [here](https://www.virtualbox.org/wiki/Downloads).
## Download the Android x86 ISO file
Download an ISO file [here](http://www.android-x86.org/download)
## Create Your Android vm in VirtualBox Manager
 Create a vm with 2G+ hard disk, from storage options mount the iso as the cd/dvd. Use bridged network.

## Add custom screen sizes
If you want to android in portrait mode (i.e., a phone), use the following command to add a custom resolution to the .vbox file.
```
VBoxManage setextradata "YourVMName" "CustomVideoMode1" "480x800x16"
```
If the vm is running, you must poweroff and start the virtual machine to load the changed configuration (i.e., a simple reboot may not work)
## Boot the virtual machine and choose "Installation - Install Android-x86 to harddisk"
* Create partition, format it with ext3
* install boot loader GRUB
* mount system as readwrite 

## Edit the grub menu
Boot the vm and start in debug mode.
If /dev/sda1 is not mount in rw mode, ```mount -o remount,rw /mnt```
edit the /mnt/grub/menu.lst file, append the following to the kernel parameters.
```
DPI=240 UVESA_MODE=480x800 
```
or
```
DPI=240 vga=ask 
``` (you can choose the screen size on boot)

## Get the IP address of the emulator
Press Alt<+F1, you will get a console. Type ```netcfg``` and write down the ip address. Press Alt+F4 to go back to GUI.
## Connect with adb
```adb connect [ip of the emulator]```
Then the emulator will show up in ```adb devices```

Host+U is the sleep/awake button.