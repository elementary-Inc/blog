---
title:  "A New Notifications System"
subtitle: "Rewritten from the ground up, but you wouldn't know it quite yet"
author: cassidyjames
date: 2019-08-01 09:00 -0600
---

This June, Daniel Foré and Adam Bieńkowski tackled a daunting but important project: rewriting the notifications system for Pantheon and thus elementary OS. What was wrong with the old one? No single thing, but it had a number of issues that made it difficult to work with: it was implemented entirely as a monolithic Gala plugin, it was custom-drawn in Cairo and Clutter, and it had low developer visibility (and knowledge).

With our brand new elementary Notifications codebase, we've addressed each of these pain points and paved the way for future iteration.

## Modularity

We've always striven for Pantheon to be as modular as possible, with the dock, panel, compositor, Applications Menu, indicators, shortcut overlay, etc. implemented as individual components.

### Old: Implemented entirely as a Gala plugin

The notifications were notoriously implemented entirely in Gala. While they were a plugin, it was still a more monolithic design that we try to avoid. It also meant a poor separation of responsibilities by mixing window management code (what Gala is designed for) with notification server and presentation code.

### New: A lightweight binary + window management

The Notifications server is now its own repo on GitHub and built as its own standalone binary. This brings it out of the Gala codebase and gives us a fresh start. It also means the desktop is more resilient overall, as any theoretical crashers in the notifications daemon would not take down Gala itself. 

The new notifications are GTK windows with a notification hint, and Gala simply ensures it positions any notification windows correctly. This also means another notification server or non-native notifications setting the correct window hints will work with Gala, and the new notifications system could theoretically be used with any other DE that correctly positions notification windows.
