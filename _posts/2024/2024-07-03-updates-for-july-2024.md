---
title: 
description: OS 7 Updates and OS 8 progress during June
author: danrabbit
image: /images/updates-for-july-2024/.png

tags:
  - earlyaccess
  - horus
  - updates
---

This month we have several community updates, a couple of Flatpak releases available on OS 7, and plenty of OS 8 news.



## Disability Pride Month

It's disability pride month, which means making space to talk about how we can build communities and systems that better accommodate people with disabilities. Last year for disability pride month we announced [color deficiency assistance filters](https://blog.elementary.io/updates-for-june-2023/) and a new feature that reads out the keyboard shortcut for the screen reader during Installation &amp; Initial Setup. You might also be familiar with our [Curb Cuts](https://blog.elementary.io/accessibility-features-are-just-features/) initiative that was started a few years ago and how we [completed it in OS 7.1](https://blog.elementary.io/os-7-1-available-now/). We also expanded the number of places affected by the Reduce Motion setting, increased the upper intensity limit for Night Light, and made sure accommodations were present on the Lock Screen.

This year we had the pleasure of being introduced to [Florian Biejers](https://www.twitch.tv/ic_null) who describes himself as a fully blind cybersecurity enthusiast. You may have heard him recently on [Linux After Dark](https://latenightlinux.com/linux-after-dark-episode-72/) talking about accessibility on Linux desktops generally. [A couple weeks ago](https://www.youtube.com/watch?v=7jOB4lZH3AE), he took some time to take a look at the state of OS 8 with regards to accessibility for someone who has no vision at all, and I'll be honest we were definitely humbled by his experience. We took notes, filed issue reports, and I'm proud to say we've already taken meaningful steps towards addressing his feedback with fixes across the desktop and in our platform libraries, but there's clearly a long way for us to go! If you want to follow along or help us address accessibility issues in elementary OS, we'd love your help! We're tracking issues in [this GitHub project](https://github.com/orgs/elementary/projects/111). If you discover a new issue—accessibility related or otherwise—we'd love to get your feedback and we have a handy contributor guide to help you [file a report here](https://docs.elementary.io/contributor-guide/feedback/reporting-issues).

## Community Chat

Tracking issues for StarLite Mk V

Discord server

Fedora call for contributors for Pantheon SIG discord.gg/fedora

---

Photos 8 released as Flatpak

Capnet Assist 8

---

## AppCenter

Redesigned links in AppCenter. More links shown including Sponsors that aren't monetized through AppCenter

Much faster AppCenter startup, thanks to Leonhard

Cleanups, bug fixes, performance improvements for updates

AppCenter pages now draw their own headerbars. Already started making design changes like keeping action buttons in the headerbar, showing a smaller window title when scrolled

## System Settings

Locale Settings has temperature unit from locale. Fixed freezes while getting permission. Don't prompt admins for password to change system language

Network Settings shows SSID of connected wireless network in the sidebar

Revamped how links are shown in System Settings → System

Bluetooth settings fix icon with some headphones

## And More

Screencast portal, Inhibit shortcut dialog; thanks to Leonhard

Code now uses Hdy.TabBar, important step in Gtk 4 porting. Also made a lot of progress toward using GLib.Action and GLib.Menu thanks to Colin


## Release Planning

Wayland bug fixes. Almost parity with X11 session

Working on releasing all components. Some of these releases may show up in OS 7, many can't. 

https://github.com/orgs/elementary/projects/128/views/1

---

## Sponsors

At the moment we're just above 20% of our monthly funding goal and we're almost at 350 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

If you're not already in Early Access, you can be among the first to try the next release of elementary OS and give us your feedback by sponsoring elementary [for as little as $1/mo](https://builds.elementary.io/). Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
