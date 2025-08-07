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

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

Maps

Window Manager:
* Window switcher blur
* Dock workspace switcher in Multitasking View
* New Touchpad backend for Gestures: https://github.com/elementary/gala/pull/2497

Dock:
* backgrounds apps

EUFI ARM64 builds

---

## Sponsors

At the moment we're at 23% of our monthly funding goal and 322 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
