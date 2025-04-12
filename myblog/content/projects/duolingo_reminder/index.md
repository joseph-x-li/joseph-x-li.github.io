---
title: Duolingo Reminder System
description: "Use Facebook Messenger to remind my friends to do their Duolingo Lessons."
date: 2020-11-20
extra: {"featured_image": "/projects/duolingo_reminder/duogun.jpg"}
---

## about

{{ github() }}[Github⇗](https://github.com/joseph-x-li/fb-duolingo)  

Just do your Duolingo lessons so Duo won't come for your family.

I originally made this because my friend Konwoo had trouble keeping his streak.

<img src="/projects/duolingo_reminder/kimdead.png" width="700"/>


## how it works

The script is run daily using a cronjob. It calls Duolingo and Fbchat APIs to check streaks and send messages. Extendible to multiple users.

Random time delays are incorporated to prevent Facebook logging me out of my account.