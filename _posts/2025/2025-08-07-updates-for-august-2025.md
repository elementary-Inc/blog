---
title:
description: Updates for OS 8 and Early Access
author: danrabbit
image: /images/updates-for-august-2025/card.png

tags:
  - circe
  - updates
  - earlyaccess
---

# System Settings

The previously mentioned redesign of Bluetooth Settings has arrived! This redesign not only brings a bit more visual separation between paired devices and nearby devices, but also improves the keyboard navigation and screen reader experience. Plus, you can now double click rows to activate them. We resolved an issue where sometimes devices would be duplicated in the list and fixed issues when a pairing request requires entering passcodes—like with some keyboards. You'll now also see fewer unnamed devices when discovering, enabling and disabling bluetooth on devices that have been hardware locked should now work reliably, and to top it all off performance when listing lots of devices has also been improved.

Leo and Ryo fixed a couple of issues with sidebar selections when navigating directly to a setting from search. Ryo fixed an issue where Sharing Settings lost its window controls when a network was not connected. And there's now an action to jump directly to the System Updates page from the context menu in the Dock or Applications Menu or via search.

# Code:

Jeremy added a new feature to clone git repositories directly from inside Code via the projects menu in the sidebar. The item for opening project folders has moved there as well. He also fixed an issue with blank tooltips appearing in empty sidebar folders, a crash when deleting selected text while using the "Highlight Selection" plugin, and a freeze when editing lists with the "Markdown" plugin. Plus, the Symbols sidebar now shows a loading spinner when searching symbols takes longer than usual, and filters have been fixed for C symbols.

# Terminal

Terminal will now warn about pasted commands that include options to skip confirmation like `-y`, `--interactive=never`, and `--force`. Plus we now make sure to show all found warnings about a pasted command, not just the first one found. For example, if a command like `sudo apt update && sudo apt install -y fuse` is pasted, we will warn about use of admin privileges, multiple commands, and that it skips confirmations, not just that it uses admin priveleges.

Corentin fixed an issue where long commands could resize windows. Jeremy fixed an issue where tab labels didn't properly update when using `screen` or `ssh`. And he made sure we properly close tabs when using the `exit` command.

# And More

A few small bug fixes for our Window Manager: Corentin resolved a potential crasher, Leo improved dock hide animations, and Leonhard fixed an issue with revealing the panel over fullscreen apps.

A new Hardware Enablement stack has arrived thanks to Ubuntu! This includes Linux 6.14 and Mesa 25 which brings support for newer hardware as well as some big performance gains and potential battery life improvements. OMG! Ubuntu! breaks down all the nerdy details [here](https://www.omgubuntu.co.uk/2025/03/linux-kernel-6-14-released-delivers-big-boosts-to-linux-gaming)

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

## Maps

Last month, Ryo made the last release of Atlas on AppCenter because we'll soon be shipping it by default in elementary OS as Maps! As part of our work to make elementary OS great on computers you take with you—like notebooks and tablets—we've been working on features that use your location, and shipping a Maps app is part of that work. Our hope with Maps is to improve support for mapping and location features in our platform libraries and to improve experiences in other apps like Tasks and Calendar as well as 3rd party apps in AppCenter. We've also already made a tiny improvement to the wider Freedesktop ecosystem by documenting a standard location icon used across desktops and in Portals. We're really looking forward to getting your feedback and learning how we can improve experiences for apps that use your location in elementary OS.

## Window Manager &amp; Dock

First up is some new eye candy. We've heard requests for transparency and blur over the years and I'm happy to report we're now experimenting with some new effects in shell elements like the `alt` + `tab` Window Switcher. We want to make sure to carefully balance shiny effects with performance and legibility, so be sure to send in your feedback. We're also on track to apply some blur behind the Dock soon, so watch out for that.

Speaking of the Dock, you may have noticed that it's now sticking around when in Multitasking View! We've replaced the old workspace switcher and you can now launch apps from the Dock directly into different workspaces to quickly get things set up exactly how you like. We've also merged in a new feature to monitor background apps that use the cross-platform Background Portal. Here you can not only manage background apps, but also see an explanation of what exactly they're doing while running. With these features, we're seeing years of design and development work come together: an improved way to multitask on elementary OS whether you use a mouse at your desktop, multitouch gestures on your laptop or tablet, or rely on keyboard shortcuts to get the job done. I'm extremely proud of what the team has done here and look forward from hearing more from you about it!

And that's not all. Building on the previously mentioned [Gesture Controller](https://github.com/elementary/gala/pull/2258), the new [Touchpad backend](https://github.com/elementary/gala/pull/2497) for multitouch gestures has also landed. This replaces Touchégg in the Secure Session as the way to track multitouch gestures, fixes bugs, and enables new features like two-dimensional swiping between workspaces and the full Multitasking View. So if you are a fan of gestures on your notebook, we'd love for you to try it out and report back before we ship it for everyone.

## Hardware Support

Last but not least, we're now building Universal EFI install images for ARM64 processors. This means instead of building unique ARM images for every hardware platform, we can build a single universal image for platforms like Pinebook, Raspberry Pi, and M-series Macs. These builds are still experimental and come with a few bugs, but we'd love folks to give them a spin in a virtual machine or on a spare computer and report back. If everything looks good, we may be able to offer stable ARM64 downloads starting with OS 8.1 later this year.

---

## Sponsors

Special shoutout for big sponsorship!





At the moment we're at 23% of our monthly funding goal and 322 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
