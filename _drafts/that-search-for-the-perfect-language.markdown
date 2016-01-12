---
layout: post
title: "That Search for the Perfect Language"
date: 2015-12-04T17:00:00+01:00
permalink: "perfectlanuage/"
header-img: "img/perfectlanguage.jpg"
comments: true
published: false
---

Every few months (or weeks?) I fall into this desperate state of looking for a new programming language to familiarize myself with. There's always something cool I come across, love for a while and then get bugged enough by the shortcomings that I no longer like it.

This post is going to do something you probably shouldn't do and that I'll probably regret in a few months/years. I'm going to go over a few languages I've spent a little or a little more time with and highlight what I believe to be their awesome features and weaknesses or things I dislike. Don't get me wrong, just because I don't like something doesn't mean that it's a bad thing or that it won't be the single feature bringing you to a language, all of this is just a collection of my personal opinions. If there's something you dislike about this or want to add or correct, please leave a comment, I'd love to hear your opinion 😊

I've spent as I just said at least a little time with the listed languages, fallen in love with some of them along the way, built some fun stuff, disliked some features and so, in no particular order, here they are.

### Python

**+** Extremely simple syntax\\
**+** Runs almost anywhere\\
**+** virtualenv

**-** pip\\
**-** Python2 will probably never die\\
**-** No types

That language a lot of people refer to as being straight pseudo-code. Python really does have a wonderfully simple syntax (especially the slices!) and is mostly a joy to write. Most of it stays out of your way and you can just keep on typing. The only syntactic thing *really* bugging me were the constant `self` references everywhere.

It was my scripting language of choice for quite some time. Although I don't believe I've ever touched much of Python 2, I am quite familiar with Python 3 and used it for pretty much anything I came across. Especially fun to touch were things powered by [Bottle](http://bottlepy.org/docs/dev/index.html) and [Flask](http://flask.pocoo.org). That's also why the project [ParkAPI](https://github.com/offenesdresden/ParkAPI) exists in the way that it does.
Python is definitely nice for smaller scripts and great libraries like matplotlib, but anything bigger quickly leaves you longing for missing things like types. I ❤️ types!

The tooling is rather meh as well. There's pip, which works, but not very well in my opinion[^1]. Packaging stuff for it is really rather painful and some installs leave you going almost insane. And you better hope you've got a virtual environment running beforehand (which is actually pretty sweet!), 'cause nobody likes globally installed packages. And of course don't forget to use pip3 if you're not already in said virtualenv.

Also, it can be rather slow at times. Don't get me wrong, My normal use-cases don't really leave me at a need for extremely fast execution times, but it can be rather aggravating at times. And yes, I know that there are several ways of working around this and improving it somewhat, but nothing's just perfect imho.

### Ruby

**+** Beautiful language! (blocks 😍)\\
**+** It's everywhere\\
**+** There's a gem for everything

**-** Dependencies are a pain to manage\\
**-** No types

It doesn't make much of a difference what kind of software development you do, you're going to come in contact with ruby sooner or later. Especially on OS X. The best package manager for OS X, [homebrew](http://brew.sh), is written in ruby. The most popular dependency manager for iOS, [Cocoapods](https://cocoapods.org), is as well (although I kinda prefer [Carthage](https://github.com/Carthage/Carthage), just as an aside). Lots of things are written in ruby, even this blog here is powered by [Jekyll](https://jekyllrb.com), a ruby project. Aside from that, ruby is preinstalled on a lot of systems out there, a few friends only stumbled across a ruby interpreter on their Arch Linux machines a few months ago.

The biggest 👍 is definitely the syntax. Ruby is extremely fun to write, supposedly optimized for developer happiness, and I can definitely verify that. A great example for sane and nice defaults are the `!` and `?` suffixes to a lot of functions. `!` mutates the object you're calling it on in place and `?` typically returns a bool value. Both of these are easily understandable and clean. Love it!

Another cool thing about ruby is the ecosystem. I'm not necessarily talking about those thousands of friendly devs you can meet online and afk, but the amount of gems out there that you can use to accomplish almost anything without writing much code yourself. It really seems like there's a gem for everything.
That does bring us directly to ruby's biggest downside. Dependency management. This hurts oh so very much... There's a bunch of tools willing to help you out here (see [bundler](http://bundler.io), [rvm](https://rvm.io) and [rbenv](https://github.com/rbenv/rbenv)), but it just doesn't work. It'll probably work *fine* if all you're working on is one big project where you can just install gems into a `vendor` directory with bundler or use rvm's gemsets or I don't know what, but if you have a bunch of small things with different gem requirements you're going to lose your mind. I'm definitely not a fan of installing dependencies globally on my machine somewhere, but it seems like that's the only way of working with ruby.
I recently wanted to get a <20 line ruby script with a few gems running as a cron job on a server. I literally spent a day getting that to run! And I seriously did not find a way besides having to install rvm, setting several environment variables in my crontab and moving the execution to a pointless shell script for no obvious reason. It was a *pain*!

As nice as ruby's syntax is, that really put me off it. I seriously regret that, but I can't be dealing with that over and over.

It's also missing types the same way python is and speed is a topic we won't even touch.

### Java

<!-- + ubiquitous, although that's more the JVM than Java itself, but it's also everywhere
+ *the* Android language (but check out Kotlin!)

- JVM -->

I don't think I know even a handful of people who've never written Java. Most of us go through Java at some point of our lives in school or university. Most move on to other languages, some stay because they like it. I'm not one of the latter ones.

Java's biggest plus is probably less java and more JVM. Code you write in java will probably run on your refrigerator. The language itself is incredibly verbose and typical "best-practices" will lead to (perhaps *slightly* overexagerated) examples like [FizzBuzzEnterpriseEdition](https://github.com/EnterpriseQualityCoding/FizzBuzzEnterpriseEdition). My biggest gripe are the endless classes and packages you have to spam across the place. Subclassing hierarchies quickly become ugly and non-understandable beyond belief even though the basic idea and typical examples always feel nice.

It is however that language you use when you want to develop for Android. That's not entirely true since you can use others as well (see [Kotlin](https://kotlinlang.org) as a great alternative!) or almost anything else with the NDK. But Java is definitely the most popular language on Android hands-down.


### Swift

+ Open Source
+ Optionals
+ Classes, Structs, Enums all with methods
+ build native iOS and OS X apps

- no "simple" string api
- no "simple" networking api

Before going into any detail, I ❤️ Swift! Seriously! This is definitely my language of choice for several reasons.


### Node.js

+ so much neat web stuff

- fucking async *everything*

Kolledata!

### Clojure

+ JVM
+ functional
+ *everything* is just a function. (something something), so lispy
+ can be used for Android dev

- JVM

### Go

+ simple syntax
+ compiles to a simple static binary
+ cross-compilation is *incredibly* easy
+ errors are as straight-forward as possible
+ it's *fast*
+ goroutines!

- no string interpolation
- (multiple return values make one-liners impossible)
- no warnings
- unused variables compile errors are getting in my way of debugging
- no default method params
- so much casting with interface{} json unmarshaling

Go is probably the most recent addition to this list. I've tried my hand at writing go code a few months ago, but turned away with a somewhat bitter taste in my mouth because I misunderstood a few things. Coming back to it later left me seriously impressed.

Some others worth mentioning:

#### Objective-C

+ iOS and OS X
+ nil messaging, wtf?

- ugly syntax, especially regarding string literals and blocks!
- crufty

#### C#

+ simple syntax (it's java!)

- a pain on non-windows systems

#### PHP

<!--
+ nice for quick hacky little (!) web stuff

- shitty for literally everything else -->

Writing about PHP is difficult to say the least. Almost everybody I know considers this language to be nothing more than an elaborate joke but there a lots of people out there writing software we use daily with this. And no, I'm not talking about Facebook and [Hack](http://hacklang.org).

I've touched a bit of PHP here and there, and I have to say that I dislike this language a lot, but it does have its uses. In my opinion the only one being that it's incredibly simple to throw together a few lines of PHP to do whatever it is you want to build and upload that to almost *any* server out there having it work. The example that stayed with me here being something a few friends and I recently used to accept a POST request and dump that into a SQLite db. A CGI script in any other language would've also done the job in exactly the same way, but if something extremely simple like that is all you need, PHP actually doesn't feel like a bad choice.

If I were to look for something though to actually build an actual server application that I would want to trust with anything, I would never ever choose PHP or any framework on top of this with the job. I don't like pain of frustration that much.

#### Haskell

+ so schweet and functional
+ stack, when it comes around

- cabal

#### Coffeescript

+ cool things like var? in contrast to JS
+ nice function syntax

- not really usable for the things I do

#### Crystal

+ ruby syntax \o/
+ statically compiled
+ fast!

- oh so new
- cross-compilation seems to be rather cumbersome atm
- I'd love straight usage of all rubygems, but crystal ain't ruby

Googling for "Crystal speed" is *not* a good idea.

#### Rust

Can't say that I've done much with Rust, but it looks great! And [Hendrik](http://blog.hoodie.de) won't quit talking about it 😄 (I meant that in the best possible way!)

##### ADD CODE SAMPLES!

## Summary

As stated at the beginning, all of this is just a collection of my personal opinions, feelings and so on. A lot of this will surely on apply to myself, but I nevertheless wanted to put it into words.

My (current) languages of choice are definitely Swift and a bit of Go, Ruby and Python here and there. But I do know myself and these are bound to change in the future. I'd love to move some stuff into a more functional direction and am keeping tabs on Clojure and Haskell in particular. Crystal also seems like a great language, I really hope it takes off. And who knows what other great languages might come along 😊

Header image by Ruiwen Chua on [Flickr](https://www.flickr.com/photos/ruiwen/3260095534/).

[^1]: I've heard (mostly thanks to [Lucas](http://lucaswoltmann.de)) about newer (and supposedly better) alternatives like [Anaconda](http://docs.continuum.io/anaconda/index), but I've never seen them in action or touched them, so unfortunately I can't say much about them.
