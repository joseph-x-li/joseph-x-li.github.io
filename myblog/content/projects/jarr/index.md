---
title: "JARR (just another rescue robot) @ hackberry pi"
description: "Search and rescue robot built on a Raspberry Pi. Won Best Hardware Hack"
date: 2022-03-20
extra: {"featured_image" : "/projects/jarr/full.jpeg"}
---

## about

{{ github() }}[Github⇗](https://github.com/joseph-x-li/jarr)  
{{ youtube() }}[Demo⇗](https://www.youtube.com/watch?v=nfWhVgOaVFY)  
📐 [CAD⇗](https://cad.onshape.com/documents/377210a764448a03d8c2452c/w/4b00f0117df7dc110a1be7fe/e/04cd887d46c7703afd3cc0a6?renderMode=0&uiState=62a69f8136debc5150aff378)  
{{ devpost() }}[Devpost⇗](https://devpost.com/software/jarr)


Many robotics projects have no obvious purpose, so they end up being deemed "search and rescue" robots. This is yet another search and rescue robot to add to this motif.

This was a solo 5d hackathon project. I was able to CAD the robot, 3D print/laser-cut the parts, assemble the robot, and write the software in the timeframe.

## how it works

There is an onboard raspberry pi that has a battery power supply hat. The hat supplies power to the pi and servos.

Communication is done from the controller to the server over ZMQ sockets. The server streams back video over ZMQ as well.

## build pictures

<img src="/projects/jarr/steering.jpeg" height="400"/>  
<img src="/projects/jarr/partial_assembly.jpeg" height="400"/>


## what it does

Searches, then rescues!