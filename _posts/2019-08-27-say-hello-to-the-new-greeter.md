---
title: Say Hello to The New Greeter
description: Our redesigned login and lock screen
author: danrabbit
image: /images/elementary-blog-code-1600.jpg
tags:
  - design
---

After nearly two years of design, development, and testing, I'm very excited to talk to you about a huge change to the user experience in elementary OS: our new Greeter.

Closed 43 issues with this redesign https://github.com/elementary/greeter/milestone/2?closed=1

accounstservice

# Design Process

Motivations:
* Clutter is harder to work with than Gtk. Fix layout bugs and make it easier to add animations and to make changes in general
* Fix focus issues
* Fix multi-dsiplay issues
* Scale better for lots of users
* High contrast
* Address issues with user settings not being applied to the Greeter. Most notably using the correct time format
* Make things like media keys work
* Special case the guest session so that it doesn't look like a normal user
* Handle the case where there are no users on the system yet
* Fix lots of bitesize bugs

GNOME Shell UX hackfest that cassidy attended was in 2017 https://blog.system76.com/post/167747412318/gnome-ux-hackfest-2017

sketches from Cassidy and mockup from Tobias

mockups and exploration from harvey in May 2018

https://blogs.gnome.org/aday/2018/05/09/redesigning-the-lock-screen/

Initial branch created November of 2018 https://github.com/elementary/greeter/pull/181


# What's Next

initial setup

more accountsservice extensions

a11y options
