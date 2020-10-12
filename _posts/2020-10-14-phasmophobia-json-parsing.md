---
published: false
title: JSON Parsing, Phasmophobia Email Interview
layout: post
---
# Phasmophobia Email Interview
I started the week by emailing a few people for interviews. The team behind Phasmophobia responded fairly quickly, and while they didn't have time for a zoom interview, they did give me some insight into their approach. Phasmophobia was developed in Unity and used the interface with Windows 10 Cortana. They said it was extremely easy to set it up, which I found to be interesting. However it is only usable for games on Windows 10, which limits target platforms. They also said the main issue they were facing at the moment was with permissions, which seems like an interesting issue to be having, but the wit.ai method should avoid most permission issues.

# JSON Parsing
I started this week looking into Newtonsoft's JSON parser, as recommended. After an hour I decided to use [this](https://github.com/jilleJr/Newtonsoft.Json-for-Unity) version for it based off Unity forum posts. I spent the next two hours setting up a series of classes to store the response in, extrapolating from a very basic tutorial and then solving my errors by trial. The only part of the response that might not work is the traits, but without setting that up for my own Wit app, I cannot test it and don't think it's worthwhile (for the time being anyway). I then cleaned up my code because it was a mess from all the trials.

# Forward Charge
With the mess cleaned up, I moved onward to set up a way of interacting with this input. I decided upon using a delegate to handle this. As it was my first time using delegates, it took me a bit to understand how they work, but after an hour I had it working and was able to set the delegate to a function that logs the intent and entity bodies. With the knowledge that my delegate was working, the next step was to set up a simple game that actually uses this information.

# Voice Controlled Chess
