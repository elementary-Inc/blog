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

We've been working hard to bring you a new Greeter that's made with your concerns in mind. With the new design, we've closed 43 [reported issues](https://github.com/elementary/greeter/milestone/2?closed=1) in GitHub. This means fixes to things like keyboard focus issues, brightness keys now work as expected, and the clock will show 24 hour or AM/PM formats on a per-user basis. The new design should work better on multi-display setups as well, including docked laptop setups.

You can update and start using the new Greeter today! Just pop open AppCenter and hit that "Update All" button. Enjoy!

---

_That’s it for user-facing information! If you’d like to hear more about the design and development process of the Greeter, read on._

---

## Design & Development Process

There were a laundry list of motivations for rethinking the greeter and we approached the design from a lot of angles. Firstly, we had technical motivations. Gtk has improved greatly over the last few years and Clutter has become abandoned. The old code base was a bit of a mess and made it difficult to fix issues or add new features. Clutter made it difficult to address issues that were trivial to solve in Gtk, like making sure the clock doesn't overlap with the username and password. We also wanted to make sure that the new design ensured high contrast between text on the screen and the background; The old design didn't work well in situations where a user wanted to have a particularly bright wallpaper. Localization was a concern as well: users frequently told us they wanted to be able to select their own indiviual clock format. We also had loads of reported usability issues like the Guest session not being obviously differentiated from normal users, no indication of num or caps lock, cursor focus issues, multi-display issues, HiDPI issues, difficulty with identifying users who didn't set an avatar, and more.

As far back as November of 2017, Cassidy attended the [GNOME Shell UX hackfest](https://blog.system76.com/post/167747412318/gnome-ux-hackfest-2017) in London where it turns out GNOME (and related parties) were struggling with a lot of the same design issues. It was here that Tobias (from Purism) proposed the idea of showing users' wallpapers behind their avatars in a horizontal card layout.

<figure markdown="1">
![GNOME mockups](/images/say-hello-to-the-new-greeter/gnome-mockup.png)
<figcaption markdown="1">
Tobias' concept mocked up
</figcaption>
</figure>

You can see that this design also includes distinguishing the Guest session and manual username entry from regular users by placing separate buttons at the bottom of the display. These designs and ideas took a bit of a backburner until May of 2018 when Harvey Cabaguio revisited a few of these concepts in a new set of mockups and in a more elementary style.

<figure class="half" markdown="1">
![Harvey's mockups](/images/say-hello-to-the-new-greeter/harvey-login-mockup.png)
![Harvey's mockups](/images/say-hello-to-the-new-greeter/harvey-lock-mockup.png)
<figcaption markdown="1">
Harvey's concepts for login and lock
</figcaption>
</figure>

And then again work was deprioritized until last November when Corentin proposed the [initial branch](https://github.com/elementary/greeter/pull/181) of what would become the new Greeter. Since that time, we've been making steady progress. The primary goal was reaching feature parity with the old design. That means making sure we indicate which users are logged in, showing a menu with session options, providing feedback when an incorrect password is entered, detecting HiDPI displays, manual and guest logins, and more. At the time of merging, this branch already closed 13 issues with the old design, but it would be another 48 pull requests over the next 9 months before release.

We're really proud of the work done on making the new Greeter experience smooth, but this is just a first step! Now that we have a clean foundation, the team is ready to more actively discuss changes and iterate based on your feedback.

## What's Next

One of the big tangential changes that came out of this was an AccountsService extension for Pantheon. If you're not familiar, AccountsService makes a limited set of user data available to the system: things like the user's full name, avatar, and wallpaper. In order to solve the issue of showing the correct time format on the Greeter, we needed to create a new extension to AccountsService to save time format data in—previously we'd been using a GSettings key in the Date & Time indicator (which caused a few issues of its own). Having an established AccountsService extension paves the way for exposing other user settings to the Greeter as well. In fact, we have a [GitHub Project](https://github.com/elementary/greeter/projects/2) for tracking requested user settings and we'll be exploring the best way to make sure that the Greeter remains consistent with what users expect from their session settings.

We're also looking at adding an [Accessibility Indicator](https://github.com/elementary/wingpanel-indicator-a11y) to the Greeter to make some previously-inaccessible tools (like the screen reader, on screen keyboard, etc) available. We've also discussed a way to more easily and automatically launch pairing for bluetooth input devices when no inputs are detected. This is pretty essential stuff for new installations for example.

And of course, as part of our work on the new [Installer](https://blog.elementary.io/meet-the-upcoming-installer/), the Greeter now handles the case of having no users on the system and will launch an Initial Setup window to help you create a new user. More on that later, but for now I'll just tell you that the experience is very slick!
