---
title: The First Pride Was a Riot, and So Are These Updates
description: New bug fixes and features for OS 8
author: danrabbit
image: /images/updates-for-june-2025/card.png

tags:
  - circe
  - updates
---

Questionable puns aside, it's Pride Month and we're excited to celebrate by bringing you these updates hand-made by real LGBTQIA+ community members from around the world!—and possibly some straight cis folks too. This rainbow of releases includes some important accessibility updates, tons of bug fixes, and of course a few new features.

## Window Manager &amp; Dock

Another absolutely massive release of our window manager is out that fixes about 20 reported issues and a brand new [Gesture Controller](https://github.com/elementary/gala/pull/2258) thanks to [Leonhard](https://github.com/leolost2605) and [Leo](https://github.com/lenemter). You can now Swipe up in Multitasking View to close windows, app titles in Multitasking View are now always shown—making them accessible for touch screen setups—and screenshots taken with a keyboard shortcut will send a notification that you can use to view it in Files, just to name a few headlining features. If you want to read the [full release notes](https://github.com/elementary/gala/releases/tag/8.2.0), Good Luck Babe they're quite long.

A new release of our Dock is also out which brings back a couple of old Plank features: showing multiple dots for apps with multiple running windows and cycling through app windows when you hold a drag-n-drop over its icon. Plus you can now open context menus with a long-press. And there's a number of bug fixes including things related to hide modes and memory usage. Thanks again to [Leo](https://github.com/lenemter) and [Leonhard](https://github.com/leolost2605) for their hard work here.

## System Settings

[Leonhard](https://github.com/leolost2605) fixed a crash when setting custom hotcorner commands and we now only show the Applications Menu hotcorner action in its corresponding panel corner—that's top-left for folks reading left-to-right and top-right for folks reading right-to-left. Plus there's a new option to enable hotcorners even while an app is fullscreened.

As a follow up to last month's fixes, choosing light or dark mode in System Settings will now properly snooze your schedule instead of disabling it all together—a great convenience for those of us who suffer from eye strain or headaches and need to occasionally reach for that dark mode during the day. Plus, the Reduce Motion setting now covers a whole new range of animations—perfect for folks who get motion sick or find animations distracting.

[Leonardo](https://github.com/leonardo-lemos) tackled a couple of crashes in Display settings including one when mirroring, and another when new displays are attached while System Settings is open. We fixed an issue that prevented CalDAV accounts from connecting in Online Accounts settings. And [Alain](https://github.com/alainm23) snuck in a few design tweaks, fixing button alignments etc.

## And More

Thanks to feedback from [Aaron](https://github.com/aaron-gh), Notifications and the Shortcut Overlay both got releases that add screen reader support. [Corentin](https://github.com/tintou) addressed some Flatpak sandbox issues with an updated Apparmor Profile—especially notable if you'd had trouble with Steam. We now use [BeaconDB](https://beacondb.net/) as our location services provider. And thanks to [Ryo](https://github.com/ryonakano) we're now shipping the latest version of GNOME Web which brings improved performance and web compatibility as well as a redesigned bookmarks sidebar.

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Community Pride

I want to take a little space to say that our community is for everyone regardless of gender or sexual identity. We've long been made up of lots of different kinds of folks and I'm really proud of that. Open Source software should never be a space that is restricted to a narrow set of identities. In a time where many companies are withdrawing their support for the LGBTQIA+ community, I think it's incredibly important that we make a strong statement against hate and don't give in to the pressure to erase queer people in some sad attempt to be "apolitical". Free Software has always been political, and its politics are freedom and inclusivity and so are ours.

---

## Sponsors

At the moment we're at 23% of our monthly funding goal and 336 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
