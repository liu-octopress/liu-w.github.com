---
layout: post
title: "Ruby script for taking android screenshot"
date: 2013-05-10 14:57
comments: true
categories: [ruby, android, calabash]
---
[This ruby script](https://github.com/leohoo/auto-screenshot-android) takes screenshots of all connected android devices.

Prepare the environment:

- Install [android sdk](http://developer.android.com/sdk/index.html) if you have not installed it yet.
- Set ```ANDROID_HOME=<path-to-android-sdk>```
- Install the package:

```
git clone git@github.com:leohoo/auto-screenshot-android.git
cd auto-screenshot-android
bundle install
```

- Connect android devices to your machine through usb.
- Turn on debug mode of the devices, check the "Stay awake" option.

Run the following command to take screenshots of all the devices:

```
ruby browse-and-capture.rb "http://24log.jp/"
```
