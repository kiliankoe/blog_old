---
layout: post
title: "PyCharm and Java 8"
subtitle: "How to fix a flickering bug on OS X."
permalink: "pycharmjava8/"
date: 2014-12-19T15:23:59+02:00
comments: true
---

There's been a [bug](https://youtrack.jetbrains.com/issue/IDEA-131632) with current versions of Jetbrains products (not just Pycharm, but also IntelliJ IDEA, Android Studio, AppCode and surely the others as well) on OS X 10.10 Yosemite where the editor screen flickers uncontrollably when you scroll the view. It's been making my workflow increasingly difficult and was generally unpleasing, but there is a way around this!

Kudos goes to [Justus](http://justusadam.com) for pointing this one out.

All you have to do is set your favorite Jetbrains IDE to use the JVM version 1.8 instead of the default 1.6. This is easily done on OS X by editing the `Info.plist` found at `/Applications/<PyCharm.app or something else>/Contents/Info.plist` like this.

![screenshot](https://i.imgur.com/MVsLBn3.png)

Interestingly enough this will also make your Darcula theme a little darker (very pretty) and the font rendering gets a lot better as well. Perfect fix!
