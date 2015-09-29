---
layout: post
title: "Getting Better Tracking Results"
date: 2009-06-08T03:22:38+02:00
comments: true
---

So you’ve got a bad track, or one that’s not even bad, it’s far worse than that. This can be due to numerous things like bad lighting, missing contrast etc. A bad track is usually just a track that didn’t work out. We’re going to stay with the basic After Effects point tracker here, just so you know.

When you analyze your footage, and the tracker jumps around wildly or fails to stay on the spot you want it to, you’re dealing with one of the reasons that cause a bad track.

So what can we do?

Well, there’s three really simple solutions to this problem. We’ll go through them step by step.

### Number 1 – Pre-Shoot

What I’m trying to say with the title is that these changes can be made before you actually shoot the video. They’re simple and pretty obvious. Get some good lighting! It can be anything, a desktop lamp, a flashlight or some professional studio lighting. All that matters is that you get some more detail in the object that you’re filming. For demonstration purposes we’re going to be talking about an open hand. A specific spot in the middle of a hand is hard to track, there’s not a lot of difference there. So what do you say about creating our own differences? It’s easy, just take a small (really small) piece of colored paper and place it in the middle of your hand. Or even take a marker (preferably a color that’s actually visible -> black for example) and draw a small dot in your palm.
Tracking that will almost always work perfectly! When editing you can then cover it up, mask it away or leave it, depending on your desires.

### Number 2 – While editing

This one’s a bit more difficult, but you should be able to manage it nonetheless. The idea is to create more contrast digitally, so the tracker can then find better points. After Effects however won’t recognize any effects you’ve applied to the video when tracking, so we’re going to have to trick it into thinking that the effects were there already. This is easily achievable with pre-composing.
So, we’re going to apply some crazy effects to our hand footage. Levels, Curves, Noise, etc. Just play around with the settings until you find something that makes the hand a lot more distinct. Where you think the tracker will be able to differentiate that certain point better from others. And don’t worry, we’re not going to leave these effects on our video.
Once you’ve got something interesting down, go ahead and pre-compose that layer by selecting it and going into Layer -> Pre-Compose. Be sure to move all the attributes to the new composition, it’s important here. Now you can just go and track it again. Not the video layer in the new composition, but the new composition in your original composition!
You should get some better results this time.

### Number 3 – A different tracker

Yes, there are different trackers out there. However, I just wanted to say this option exists, I’m not going to be describing anything here. In case you’ve got After Effects CS4 you should already have a program called Mocha installed on your PC as well. Mocha is a far more powerful tracker than the built-in point tracker After Effects offers you.
If you google a bit you’re bound to find some interesting tutorials that help you better understand Mocha and how it works, I can tell you that it’s a gem!

So there you go, this information should definitely help you out with some of the popular tracking problems people keep on experiencing.
