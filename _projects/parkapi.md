---
layout: page
title: ParkAPI
---

A python-powered backend for the app [ParkenDD](/projects/parkendd.html).

![image](https://github.com/offenesdresden/ParkAPI/raw/master/image.jpg)

The code is of course fully open-sourced on [GitHub](https://github.com/offenesdresden/ParkAPI) and licensed under the MIT license.

Check out the README in the repo for additional info on how to use the API, adding support for a new city or deploying it yourself.

This project was born out of the need for new infrastructure behind our ParkenDD apps. The old idea was hacked together quickly and resulted in dresden.de being scraped every time someone opens or refreshes the app. Yeah. Not cool.
ParkAPI now scrapes the pages every few minutes automatically and saves the data in a local database that is then served to anyone requesting it. This not only allows us to work with this data much more efficiently, but also led to the development of a spec that we have used to fit much more cities and support data from them as well. As long as there are people willing to periodically update the scrapers when the format of the source pages changes, we'll be serving current parking lot data to the apps for multiple cities.

There have also been some very interesting steps towards using the data gathered over several months to develop predictions on when how many free spaces will be available. This is something that wasn't possible or available before.
