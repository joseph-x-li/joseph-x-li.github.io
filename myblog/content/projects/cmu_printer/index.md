---
title: "cmu printer app @ hackcmu"
description: "A simple app for locating CMU printers."
date: 2019-12-30
extra: {"featured_image": "/projects/cmu_printer/cmuprintersplash.png"}
---

## about

{{ github() }}[Github⇗](https://github.com/joseph-x-li/CMUPrinter)  
Teammates: Brian Zhang, Eric Tong, Brian Lee

Several of our team members remember when we needed to print magazine size color memes for a school project when we realized we could not locate the closest printer to satisfy our needs. We tried to use the cryptic CMU Printing Services website but were only confused even further. The map and website are hard to read, and the location descriptions are unclear. This is when we decided to create the CMUPrinter app.

## how it works

<img src="/projects/cmu_printer/printing.png" width="700"/>

Our app uses GPS location services to locate the closest printer that meets the student's specifications (color, print size). It shows the name of the printer, a description of its location, a picture of the printer, and fun facts about the printer's history. It even tells you the approximate distance the student would have to walk to get to the printer. This distance is calculated using an innovative technique known as the Pythagorean Theorem.

Printer statuses are scraped online and automatically updated.

We designed a custom google-maps-like feature to plot printer locations on a map of CMU given GPS coordinates. This was done to avoid paying to use the Google Maps API.

## my contributions

I designed app front-end, app flow (pages, button action), and app infrastructure (Printer class, custom map API to avoid using Google Maps). 