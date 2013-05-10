---
layout: post
title: "Take screenshot of Android devices from command line"
date: 2013-04-19 18:11
comments: true
categories: android
---
I found that calabash-android is using [this jar file](https://github.com/calabash/calabash-android/raw/master/ruby-gem/lib/calabash-android/lib/screenshotTaker.jar) to take screenshots.

[screenshotTaker.jar](https://github.com/calabash/calabash-android/raw/master/ruby-gem/lib/calabash-android/lib/screenshotTaker.jar)

To take a screenshot:

- You need to install [android sdk tools](http://developer.android.com/sdk/index.html).
- Set ANDROID_HOME to the path of the installed sdk(or you can set it from the command line).
- Download [screenshotTaker.jar](https://github.com/calabash/calabash-android/raw/master/ruby-gem/lib/calabash-android/lib/screenshotTaker.jar).
- Turn on debug mode of your device and connect it to your machine through usb.
- Run the following command:

```
java -jar screenshotTaker.jar <screenshot-filename.png> [device-args]
```

device-args will be forward to adb command, so you can specify the serial-no when you have multiple devices connected.
For example:

```
ANDROID_HOME=/DevTools/adt-bundle-mac-x86_64/sdk/ java -jar screenshotTaker.jar a.png -s 355659040404653
```
