---
layout: page
title: Projects
permalink: /projects/
header-img: "img/projects-bg.jpg"
---

A few things I've made or contributed to that I'm particularly fond of:

# [ParkenDD](http://jkliemann.de/parkendd/)

An app for iPhone that shows how many free parking spots are left on Dresden's public parking lots.

![screenshots](http://parkendd.kilian.io/images/screenshots.png)

There's also an [Android version](http://jkliemann.de/parkendd/) and a version for Windows Phone is currently in development.

As seen in the [Sächsische Zeitung](http://www.sz-online.de/nachrichten/studenten-helfen-bei-der-parkplatzsuche-3128007.html), the [Morgenpost](https://mopo24.de/nachrichten/dresden-kilian-keoltzsch-parken-dd-app-6754) and the [Ad Rem](http://apps.ad-rem.de/epaper/DMV_ADD_20150715_gesamt.pdf) (page 12) amongst others.

Check out the source on [GitHub](https://github.com/kiliankoe/parkendd).

[![App Store badge](http://parkendd.kilian.io/images/badge_small.svg)](https://itunes.apple.com/de/app/parkendd/id957165041)


# [ParkAPI](https://github.com/offenesdresden/ParkAPI)

The flask-powered API for scraping and serving the data for the ParkenDD apps.

Check out the README in the repo for additional info on how to use the API, adding support for a new city or deploying it yourself.

This project was born out of the need for new infrastructure behind our ParkenDD apps. The old idea was hacked together quickly and resulted in dresden.de being scraped every time someone opens or refreshes the app. Yeah. Not cool.
ParkAPI now scrapes the pages every few minutes automatically and saves the data in a local database that is then served to anyone requesting it. This not only allows us to work with this data much more efficiently, but also led to the development of a spec that we have used to fit much more cities and support data from them as well. As long as there are people willing to periodically update the scrapers when the format of the source pages changes, we'll be serving current parking lot data to the apps for multiple cities.

There have also been some very interesting steps towards using the data gathered over several months to develop predictions on when how many free spaces will be available. This is something that wasn't possible or available before.
