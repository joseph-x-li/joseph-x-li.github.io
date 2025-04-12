---
title: "HackMIT 2020: Rhythmic Live"
description: Synchronous music rehersal and recording over the internet. Won NASDAQ Live Music challenge.
date: 2020-09-20
extra: {"featured_image" : "/projects/rhythmic_live/rhythmiclivesplash.png"}
---
## about

{{ github() }}[Github⇗](http://github.com/rhythmic-live)  
Teammates: Konwoo Kim, Edward Li, Mason Xiao

In a post-COVID world, rhythmic.live aims to bring individuals together through music. Our platform provides audio synchronization, interactive and browser-compatible sheet music, as well as informative analytics to improve your skills—all packaged together in a simple yet elegant design. Whether you're part of an aspiring a cappella group or just having some fun with friends, perform your next musical adventure with rhythmic.live!

## how it works

<img src='/projects/rhythmic_live/rhythmiclivesplash.png'>

Musicians can join a session that a conductor manages. When the conductor starts the recording session, separate recording sessions are started in each musician's browser. These audio streams are reconstructed in sync and stored. After each recording is finished, the conductor can browse all the recent recordings, listen to them, and get automated algorithmic feedback about tone, timbre, and rhythm.

## my contribution

I created a socket.io server using python to handle xml distribution, participant synchronization, and audio distribution and splicing. Also designed some of the javascript audio recording backend.