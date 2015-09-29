---
layout: post
title: "Pulling Off the Wiggle Effect"
date: 2009-06-08T03:13:05+02:00
comments: true
---

I was asked the question on how to make a video in After Effects vibrate or move randomly in a small amount of time. This is an easy task, but hard to explain in a YouTube comment.

Basically all there is to do is create a so called expression. Expressions are (simple) commands that you can use to control almost everything in After Effects. They work like programs (if you ever had the priviledge of writing even the tiniest amount of code in any programming language), you have to take care to use the correct syntax and use special commands.
Now, if you have absolutely no idea what I just said, don’t worry, you don’t have to.

So let’s get to it. First of all you have to find the layer you want to be wiggled (that sounds interesting ;)). If you have multiple layers you might want to precompose those (Layer -> Pre-Compose), so that you’re only working with one. Now open the layer’s properties (toggle the little arrow at the bottom) and look for the position attribute. Now see that little stopwatch? Hold down alt on your keyboard and click it. Something in the likes of a text field should pop up. This is where we’ll enter our expression.

![screenshot]({{ site.baseurl }}/assets/aftereffects_wiggle.jpg)

The one we’re aiming for is, if you can remember, the wiggle expression. It goes something like this wiggle(1,1). That’s it! That’s all you have to put in that box. Whatever was already in there, you can just delete that, it’s only a filler.

But we’ve got to take a quick look at the numbers and what they mean. All you have to do to understand them is to read the expression like this “Every 1 second, wiggle 1 pixel”. So the first number is the speed or time interval. It is also possible to use fractions of a second, so 0.5 or 0.1 would be perfectly fine. They would cause extremely fast movement however.
The second number is the distance the layer will move from it’s original position. I guess you could call it the amount it would wiggle. The best way to find the right number here is to play with it. Just use something, check the RAM preview and see if it worked out. If not, go for something else.

That’s it! Really, it’s wiggling like crazy now! Well, depending on your settings.

Something you might also need to look out for are the borders. If it’s moving, it can’t stay fixed to its borders of course. So for no black edges around your composition, you might need to make it smaller or your footage larger. The amount of change depends on the settings you used in the expression of course.

There you go, I hope that helped!
