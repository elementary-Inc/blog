---
title: Faster, More Helpful, and More Yours
description: Updates for OS 8
author: danrabbit
image: /images/updates-for-april-2026/onboarding-settings.png

tags:
  - circe
  - updates
  - earlyaccess
---

# AppCenter

The latest version of AppCenter comes with some more improvements to the updates view including now showing all ongoing app installations, upgrades, and removals. Plus the "Last checked" information is now always shown in the "Up to Date" apps header. And we fixed an issue where in-app notifications were sent for every update installed.

<figure markdown="1">
![AppCenter Updates](/images/{{ page.slug }}/appcenter-updates.png)
<figcaption markdown="1">
AppCenter now shows ongoing operations in the updates view
</figcaption>
</figure>

There's also some more performance improvements including much faster startup times, faster info fetching for apps that can be installed from multiple stores, and quite a bit of code simplification and cleanup, thanks to [Leonhard](https://github.com/leolost2605).

# Code

The latest version of Code comes with a number of fixes and a couple new tricks. In the Project's sidebar, sorting project folders is now a toggle-able setting rather than a one-time action, the Terminal pane now follows the currently selected project's path, and [Jeremy](https://github.com/jeremypw) fixed an issue that could cause the number of results for a global search to be incorrect. Plus, [Loric](https://github.com/lobre) fixed an issue that could cause a crash on startup or during certain global searches, and added a new setting to disable syntax highlighting for a more distraction-free editing experience. The High Contrast style has improved contrast for line numbers, thanks to the help of [Micah](https://github.com/micahilbery). And it's no longer possible to open multiple PasteBin dialogs thanks to [Calle](https://github.com/callerun).

# Onboarding &amp; System Settings

We recently removed System Settings as a default dock item—since it's accessible from several other places and dock space is at a premium—but, there were some expressed concerns about discoverability. So we've added some additional information to the final page of Onboarding to close the gap. This page shows even after selecting "Skip All", so folks are always shown how to access additional System Settings and set up their computer how they like it.

<figure markdown="1">
![Onboarding to System Settings](/images/{{ page.slug }}/onboarding-settings.png)
<figcaption markdown="1">
Onboarding now explains ways to access System Settings
</figcaption>
</figure>

We now also support a new accent color option thanks to [Ryo](https://github.com/ryonakano): the smooth and creamy "Latte". This is a great new option for big fans of soft neutrals and can be selected both during Onboarding and from Desktop Settings. And, Desktop settings now supports long-press secondary-click on touch screens for removing wallpapers.

Font settings have also been expanded to allow an open-ended selection. So whether you need a font like OpenDyslexic for accessibility reasons, feel more productive with a coding font like Fira, or just want to have a bit of fun, you now have to option to customize text to your liking.

<figure class="half" markdown="1">
![Text settings](/images/{{ page.slug }}/settings-text.png)
![Font dialog](/images/{{ page.slug }}/settings-font-dialog.png)
<figcaption markdown="1">
Text settings now includes an open ended font selection dialog
</figcaption>
</figure>

In keyboard settings, [Ryo](https://github.com/ryonakano) also addressed an issue that would cause IBus to send a notification in Secure sessions, and [Leo](https://github.com/lenemter) added support for using the "Tools" key present on some keyboards in custom keyboard shortcuts.

# Window Manager

And of course we've got some more window manager improvements including performance improvements while zooming and a fix for an issue that would cause workspaces to change during pinch gestures by [Leo](https://github.com/lenemter). And [Leonhard](https://github.com/leolost2605) fixed issues with fullscreen Firefox videos, flickering when the Reduce Motion setting was enabled, and an issue where the correct window for apps with multiple windows would sometimes not be focused when selected from the Dock.

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

Quite a lot has been happening lately to prepare for OS 9 but I think it deserves its own blog post, so hang tight! For now, I'll say that we're getting close to a place where we might have bootable daily builds and we're making good progress on some big projects like a new design for Portals, improved CJK input support and a new on-screen keyboard, a GTK4 powered panel, our next-generation app framework and visual design and more!

---

## Sponsors

At the moment we're at 20% of our monthly funding goal and 287 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
