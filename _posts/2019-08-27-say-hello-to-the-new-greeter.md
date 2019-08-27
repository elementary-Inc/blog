---
title: Say Hello to The New Greeter
description: Our redesigned login and lock screen
author: danrabbit
image: /images/say-hello-to-the-new-greeter/screenshot.png
tags:
  - design
---

After nearly two years of design, development, and testing, I'm very excited to talk to you about a huge change to the user experience in elementary OS: our new Greeter.

<figure markdown="1">
![Greeter screenshot](/images/say-hello-to-the-new-greeter/screenshot.png)
<figcaption markdown="1">
A screenshot of the new Greeter
</figcaption>
</figure>

Closed 43 issues with this redesign https://github.com/elementary/greeter/milestone/2?closed=1

## Design & Development Process

There were a laundry list of motivations for rethinking the greeter and we approached the design from a lot of angles. Firstly, we had technical motivations. Gtk has improved greatly over the last few years and Clutter has become abandoned. The old code base was a bit of a mess and made it difficult to fix issues or add new features. Clutter made it difficult to address issues that were trivial to solve in Gtk, like making sure the clock doesn't overlap with the username and password. We also wanted to make sure that the new design ensured high contrast between text on the screen and the background; The old design didn't work well in situations where a user wanted to have a particularly bright wallpaper. Localization was a concern as well: users frequently told us they wanted to be able to select their own indiviual clock format. We also had loads of reported usability issues like the Guest session not being obviously differentiated from normal users, no indication of num or caps lock, cursor focus issues, multi-display issues, HiDPI issues, difficulty with identifying users who didn't set an avatar, and more.

As far back as November of 2017, Cassidy attended the [GNOME Shell UX hackfest](https://blog.system76.com/post/167747412318/gnome-ux-hackfest-2017) in London where it turns out GNOME (and related parties) were struggling with a lot of the same design issues. It was here that Tobias (from Purism) proposed the idea of showing users' wallpapers behind their avatars in a horizontal card layout.

<figure markdown="1">
![GNOME mockups](/images/say-hello-to-the-new-greeter/gnome-mockup.png)
<figcaption markdown="1">
Tobias' concept mocked up
</figcaption>
</figure>

You can see that this design also includes distinguishing the Guest session and manual username entry from regular users by placing separate buttons at the bottom of the display.

These designs and ideas sat until May of 2018 when Harvey Cabaguio revisited a few of these concepts in a new set of mockups and in a more elementary style.

<figure class="half" markdown="1">
![Harvey's mockups](/images/say-hello-to-the-new-greeter/harvey-login-mockup.png)
![Harvey's mockups](/images/say-hello-to-the-new-greeter/harvey-lock-mockup.png)
<figcaption markdown="1">
Harvey's concepts for login and lock
</figcaption>
</figure>

And then again work was pushed to the side until last November when Corentin proposed the [initial branch](https://github.com/elementary/greeter/pull/18) of what would become the new Greeter.

accounstservice extension

## What's Next

initial setup

more accountsservice extensions

a11y options
