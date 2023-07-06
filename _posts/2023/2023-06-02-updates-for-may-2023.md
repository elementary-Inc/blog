---
title: Getting in shape for summer
description: Updates for May, 2023
author: danrabbit
image: /images/updates-for-february-2023/card.png

tags:
  - horus
  - updates
---

This month we have mostly minor maintenance updates as we gear up for a feature-filled future release. Enjoy a mild May because this summer is going to get hot!

# Calculator

Calculator now follows keyboard shortcuts for copy and paste, even when the main text entry isn't focused, thanks to [Leo](https://github.com/lenemter)! It will no longer preserve extra white space on the right side of the window when used with alternative window button layouts. And Calculator will now always use the elementary stylesheet and icons, even when run on a different operating system, to prevent breakage related to missing assets.

# System Settings

A new version of Security &amp; Privacy settings has been released that now supports the Location portal. This is a more secure method for apps to request access to location services and is the latest FreeDesktop.org standard for doing so. If you've had trouble with sideloaded apps accessing location services before, this change will most likely fix that issue. You can adjust location settings in System Settings → Security &amp; Privacy → Location Services. If the main switch here is turned off, apps will not be allowed to even ask for permission, so make sure it's turned on if you are using apps that make use of location data.

# Music

Music can now accept Drag and Drop of whole folders, thanks to [Jeremy](https://github.com/jeremypw), and you can secondary click on a folder in Files and open it with Music thanks to [Aitor](https://github.com/aitor-gomila). Plus it's been updated to the latest Flatpak platform which fixes issues with certain animations.

# Other Updates

The latest version of Web fixes a crash in the bookmarks popover, improves the reliability of creating web apps, and has a fix related to local storage access requests.

Calculator, Camera, Captive Network Assistant, Music, Screenshot, and Videos were all updated to the latest elementary Flatpak platform, saving you a little bit of disk space and providing minor platform bug fixes.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Developer Platform

Hand in hand with our updates for the location portal, we want to ask developers to switch their apps over if they've been using geoclue directly. Future versions of AppCenter will warn about direct location services access, now that the portal is available. So make sure you remove the GeoClue line from your finish arguments if it is present. This is also a good time to re-evaluate other sandbox holes as AppCenter will be providing much more comprehensive sandbox hole warnings very soon.

Thanks go to [Josip](https://github.com/Antolius) for updating our documentation around [writing release notes](https://docs.elementary.io/develop/appcenter/publishing-updates#release-notes), including documenting the issues tag. As a little treat thanks to GitBook, our [docs](https://docs.elementary.io/develop/) now feature a dark mode toggle! Plus, you can now optionally use "Lens" to get LLM-generated answers trained on our docs in addition to regular search.

## Early Access Preview

This month we started putting together the [roadmap for OS 7.1](https://github.com/orgs/elementary/projects/122/views/2). It's been just over 120 days since OS 7 was released, so we're excited for a mid-cycle update with plenty of new features this summer.

Housekeeping is getting the ability to clean up the Screenshots folder thanks to [Josip](https://github.com/Antolius). If you're anything like me, you have a ton of those! So look out for that to appear soon in Security &amp; Privacy settings.

Color blindness correction and monochrome filters are just about ready to merge, so expect options for that soon. 1 in 12 men are color blind and the most common is red/green color sensitivity issues, so we're excited to roll out a new accessibility feature that could have such a wide impact.

Mail recently received the ability to move conversations between folders along with a healthy dose of performance improvements related to moving, archiving, and trashing, along with better undo handling. Expect better network connectivity handling as well. It also does a much better job detecting special folders, for example with GMail. Expect better attachment handling soon and [Leonhard](https://github.com/leolost2605) is currently working on the ability to [create and manage signatures](https://github.com/elementary/mail/pull/900), so hopefully that lands soon!

AppCenter has been getting a lot of work on App Info pages. Expect them to not only be more responsive to small window sizes, with tighter spacing and better grid alignment, but also be on the lookout for more comprehensive permissions warnings. AppCenter now screens apps for holes in their "sandbox" and provides you with warnings when they have access to things like files and folders, system settings, location, or the ability to break out of the sandbox altogether. We're taking [a comprehensive look](https://github.com/elementary/appcenter/discussions/2045) at the kinds of sandbox holes developers have been poking to make sure we're providing useful and accurate warnings when apps are less secure.

Speaking of [sandboxing &amp; portals](https://github.com/orgs/elementary/projects/120), we've also recently merged support for the background portal and are working on making sure default apps are all using it. This means you get more control over which apps are allowed to start up automatically when you turn your device on, as well as which apps are allowed to run in the background without a window.

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
