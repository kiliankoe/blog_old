---
layout: post
title: "That Search for the Perfect Language"
date: 2015-12-04T00:41:01+01:00
permalink: "perfectlanuage/"
header-img: "img/perfectlanguage.jpg"
comments: true
---

Every few months (or weeks?) I fall into this desperate state of looking for a new programming language to familiarize myself with. There's always something cool I come across, love for a while and then get bugged enough by the shortcomings that I no longer like it. All I want to do in this post is highlight a few languages I've spent some time with, fell in love with, built some stuff with, started disliking and so on (in no particular order). I do realize that this is a *highly* subjective topic open for a lot of personal opinion, and I'm definitely open for yours in the comments, but please don't hate me for my feelings toward these languages.

### Python

That language a lot of people refer to as being straight pseudo-code. Python really does have a wonderfully simple syntax (especially the slices!) and is mostly a joy to write. Most of it stays out of your way and you can just keep on typing. The only syntactic thing *really* bugging me were the constant `self` references everywhere.

It was my scripting language of choice for quite some time. Although I don't believe I've ever touched much of Python 2, I am quite familiar with Python 3 and used it for pretty much anything I came across. Especially fun to touch were things powered by [Bottle](http://bottlepy.org/docs/dev/index.html) and [Flask](http://flask.pocoo.org). That's also why the project [ParkAPI](https://github.com/offenesdresden/ParkAPI) exists in the way that it does.
Python is definitely nice for smaller scripts and great libraries like matplotlib, but anything bigger quickly leaves you longing for missing things like types. I ❤️ types!

The tooling is rather meh as well. There's pip, which works, but not very well in my opinion[^1]. Packaging stuff for it is really rather painful and some installs leave you going almost insane. And you better hope you've got a virtual environment running beforehand (which is actually pretty sweet!), 'cause nobody likes globally installed packages. And of course don't forget to use pip3 if you're not already in said virtualenv.

Also, it can be rather slow at times. Don't get me wrong, My normal use-cases don't really leave me at a need for extremely fast execution times, but it can be rather aggravating at times. And yes, I know that there are several ways of working around this and improving it somewhat, but nothing's just perfect imho.

### Ruby

It doesn't make much of a difference what kind of software development you do, you're going to come in contact with ruby sooner or later. Especially on OS X. The best package manager for OS X, [homebrew](http://brew.sh), is written in ruby. The most popular dependency manager for iOS, [Cocoapods](https://cocoapods.org), is as well (although I kinda prefer [Carthage](https://github.com/Carthage/Carthage), just as an aside). Lots of things are written in ruby, even this blog here is powered by [Jekyll](https://jekyllrb.com), a ruby project. Aside from that, ruby is preinstalled on a lot of systems out there, a few friends only stumbled across a ruby interpreter on their Arch Linux machines a few months ago.

The biggest 👍 is definitely the syntax. Ruby is extremely fun to write, supposedly optimized for developer happiness, and I can definitely verify that.

Another cool thing about ruby is the ecosystem. I'm not necessarily talking about those thousands of friendly devs you can meet online and afk, but the amount of gems out there that you can use to accomplish almost anything without writing much code yourself. It really seems like there's a gem for everything.
That does bring us directly to ruby's biggest downside. Dependency management. This hurts oh so very much... There's a bunch of tools willing to help you out here (see [bundler](http://bundler.io), [rvm](https://rvm.io) and [rbenv](https://github.com/rbenv/rbenv)), but it just doesn't work. It'll probably work *fine* if all you're working on is one big project where you can just install gems into a `vendor` directory with bundler or use rvm's gemsets or I don't know what, but if you have a bunch of small things with different gem requirements you're going to lose your mind.
I recently wanted to get a <20 line ruby script with a few gems running as a cron job on a server. I literally spent a day getting that to run! And I seriously did not find a way besides having to install rvm, setting several environment variables in my crontab and moving the execution to a pointless shell script for no obvious reason. It was a *pain*!

As nice as ruby's syntax is, that really put me off it. I seriously regret that, but I can't be dealing with that over and over.

It's also missing types the same way python is and speed is a topic we won't even touch.

### Java

I don't think I know even a handful of people who've never written Java. Most of us go through Java at some point of our lives in school or university. Most move on to other languages, some stay because they like it. I'm not one of the latter ones.


### Swift

### Node.js

### Clojure

### Coffeescript

### Go


Some others worth mentioning:

#### Objective-C

#### C#

#### PHP

#### Crystal

##### ADD CODE SAMPLES!

Header image by Ruiwen Chua on [Flickr](https://www.flickr.com/photos/ruiwen/3260095534/)

[^1]: I've heard about newer (and supposedly better) alternatives like [Anaconda](http://docs.continuum.io/anaconda/index), but I've never seen them in action or touched them.
