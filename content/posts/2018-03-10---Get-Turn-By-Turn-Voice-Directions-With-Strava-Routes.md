---
title: Get turn by turn bicycling directions from Strava Routes on Android
date: "2018-03-10T09:00:00.121Z"
template: "post"
draft: true
slug: "/blog/strava-android-turn-by-turn-directions/"
category: "Bikes"
tags:
  - "Bike touring"
  - "Bikepacking"
  - "Strava"
  - "Android"
description: "Build bike-friendly routes in Strava and get a friendly voice to guide you through your adventure."
---

Last summer I went on a nice 360 mile or so jaunt from Brooklyn to Somerville Mass, just outside of Boston where I got to hang out with my friend Colin and his 1.8 lb. kitten Bao bao. It was gorgeous, most of the ride was rural, totally isolated. I enjoyed the scenery and the audio book that I was able to devour in the two and a half days that the ride took. 

In preparation, I had to find some way to navigate without having to stare at a phone all the time, which is unsafe and a total buzzkill, so I looked for ways to make this happen. One can use Google Maps but in my experience, their suggestions for cycling routes aren't always safe or sensible. Google even cautions that it doesn't really know for sure whether it is sending you into a scary situation.

Most of this advice is a modified version of what [this guide](https://jeroenmols.com/blog/2016/07/21/cyclinggps/) by Jeroen Mols already posted, with some tweaks. 

## Making routes

Firstly, it's such a self own that Strava doesn't offer turn by turn navigation. The whole point of touring is to get out of the city and push into territory that you don't know. If you have to constantly check cue sheets or your phone, what's the point? As a software developer, I am sure that the people at Strava have a very good reason why this is not available on Android. It's definitely not a technical constraint, probably a legal one but who knows!

Strava's routes are excellent because they suggest good cycling routes based on popularity of it's large user base. You can reason that if a lot of users go one way rather than another, it might be for a good reason like a nice view, low traffic, or even that rare bicycling infrastructure! 

Before your ride, create a route on [Strava's route creator](https://www.strava.com/routes/new) and save. Once you save, you should see [something like this](https://www.strava.com/routes/10894406). Export it as a `.gpx` file and locate it wherever you leave your downloads. Upload that file into Google Drive in a folder called "Cycling" or whatever you like.



## Getting the route into Osmand for text to speech navigation

> **Quick interlude of nerd time** _Feel free to ignore!_
>
> A `.gpx` file is just XML. After a little metadata, its just a bunch of lat/long points plus elevation. I haven't yet figured out how this all turns into actual instructions to turn left onto a certain street but I welcome feedback. My guess is that if I use the [Source](https://github.com/osmandapp/Osmand) and learned Java I could figure it out. It would be cool if it was a series of turns rather than gps coords but there are way too many. Some day I will figure out what that is and think of something to scrape out of that.

[Osmand](https://play.google.com/store/apps/details?id=net.osmand&hl=en) is an open source turn by turn navigation app for Android. It works really well, but requires a bit of monkeying around to feed it GPX data and get the voice to turn on. In the process of getting this to work originally, I tried the Dropbox syncing trick that the aforementioned blog mentioned, then went down a nerd rabbit hole digging around the file system on my phone. Fortunately it's easier now. 

Take the 



First, [download Osmand on Google Play](https://play.google.com/store/apps/details?id=net.osmand). 



change to shared memory

download maps

open hamburger

click GPX files, pick the one in your google drive



Open and click `Get started`. 

change to shared memory

download your area

skip


Skip downloading the maps for now. Hit the hamburger menu in the bottom left and tap `Settings`, then `General Settings`. 

Look for the `Data Storage Folder` option and click that. Click the pencil edit icon and choose `Shared memory`. You will see a prompt to allow Osmand elevated access, hit `Allow`.

Now hit back until you are at the main screen and click the hamburger again and go to `Download Maps` and download the areas you plan to explore. When it's done, you should see a map of your city. Hit the crosshairs icon to allow Osmand access your location.

Now click the globe icon in the upper left. You should see a `GPX files` option to switch on. It will say 'You do not have any GPX files yet'. Click `Add more` and select Google Drive's 

sometimes there are turns announced that arent really turns so much as bends in the road. 

project fi data only sim

Boombot





