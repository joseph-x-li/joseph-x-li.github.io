---
title: "duolingo reminder system"
description: "Use Facebook Messenger to remind my friends to do their Duolingo Lessons."
extra: {"featured_image": "/projects/2020-11-20_duolingo_reminder/duogun.jpg"}
---

## about

{{ github() }}[Github⇗](https://github.com/joseph-x-li/fb-duolingo)  

Just do your Duolingo lessons so Duo won't come for your family.

I originally made this because my friend Konwoo had trouble keeping his streak.

{{ image(path="/projects/2020-11-20_duolingo_reminder/kimdead.png") }}


## how it works

The script is run daily using a cronjob. It calls Duolingo and Fbchat APIs to check streaks and send messages. Extendible to multiple users.

Random time delays are incorporated to prevent Facebook from logging me out of my account.