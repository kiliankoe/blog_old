---
layout: post
title: "HeartBattery"
date: 2015-11-20T01:41:59+01:00
comments: true
---

A [friend](https://github.com/meepoSenpai) recently had the fun idea to write a small script for his machine running Arch displaying his current battery state as a series of hearts instead of the traditional boring percentage. He did so via a short python script and the magic of Font Awesome to integrate with Conky.

I have to admit that writing a quick script in your language of choice makes customization like this a lot easier than on OS X, but I liked the idea and wanted to follow along with something native as well. So today I wrote a little app in Swift titled HeartBattery.

![menubar gif]({{ site.baseurl }}/assets/heartbatterygif.gif)

It doesn't really do a whole lot besides pulling the state of your battery every five minutes and telling you a few things about it. The hardest part was actually getting the data and generating the image. Getting the data unfortunately isn't as easy as reading it from a file somewhere like others systems do it, but you have to interface with some rather confusing C APIs. Not really wanting to do that I eventually stumbled across [SystemKit](https://github.com/beltex/SystemKit), a Swift lib that abstracts all that away and offers an API that couldn't be much simpler. It's from the same person behind [dshb](https://github.com/beltex/dshb), that amazingly pretty ncurses powered system monitor for OS X.

Unfortunately it doesn't seem possible to set a custom font for a status item and multiple images are also not an option (afaik), so I had to resort to compositing a few icons together on every refresh of the app to generate a single wide image for the menubar representing the current battery state. Really doesn't feel like the cleanest option, but another thing learned can't be bad either I guess.

If you want to have a look you can find the source and download link on the GitHub repo [here](https://github.com/kiliankoe/HeartBattery). And as usual, if you have any ideas, suggestions or think my code sucks and want to tell me how to improve it, please put a comment below or head straight for the issue/pullrequest 😊

![app menu screenshot]({{ site.baseurl }}/assets/heartbatteryscreenshot.png)

Now all that's missing is a *bling* sound whenever you lose a heart 😄
