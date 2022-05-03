---
title: Updates for April, 2022
description: Counting down to OS 7
author: danrabbit
image: /images/updates-for-april-2022/card.jpg

tags:
  - horus
  - updates
---

it's been a little while since an updates post, but we are back and operating as normal. While our primary focus has been getting everything ready to release elementary OS 7, we've also released a handful of fixes and creature comforts for OS 6.

## Updates for OS 6.1

<figure class="constrained" markdown="1">
![elementary OS 6.1 Jólnir](/images/elementary-os-6-1-available-now/card.png)
</figure>

System Settings received quite a bit of attention last month. Thanks to a first-time contributor, you can now choose to use the super key to open Multitasking View in Keyboard settings. You can now also set the refresh rate for IMAP in Online Accounts settings. Offline firmware updates are now supported on the System page. In Sound settings, we now have more helpful placeholder text when no input devices are found. And the Language & Region page now has better support for locales with 3-letter language codes.

Our window manager also saw several fixes including more accurately using your chosen accent color in the window switcher, and better handling window selections beneath the window switcher. We also do a better job of resizing the Multitasking View when display configurations change, and prevent a number of potential crashes.

Other little improvements include new native dialogs when confirming display settings changes and when force quitting apps who have stopped responding, as well as some performance improvements for notifications.

A new version of Code was also released with some handy improvements. You can now use regular expressions when searching, and the number of results are now shown. Hidden folders are now shown in the project sidebar. The name of the current file is now shown as the window title in Multitasking View. It is now possible to change Git branches with untracked files present in a project. The correct document is now focused after opening Code from an external app. And we fixed a couple of potential crashes.

## Getting OS 7 Ready for Launch

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus]( {{ page.image }})
</figure>

Now that Ubuntu 22.04 has been released, we're clear to wrap up development on elementary OS 7 and get it out the door! There's just a handful of things left to wrap up which you can follow along with on our [OS 7 Project board on GitHub](https://github.com/orgs/elementary/projects/94/views/1). At this time **there is no hard release date**; As per usual we'll be able to release when the outstanding tasks on the release board have been completed. In other words, if you'd like the release to come sooner, you can [get involved](https://elementary.io/get-involved) and make that happen!

As a short summary, the primary blockers right now are cleaning up some regressions in our window manager and hunting down and fixing any other regressions we can find. We've also recently released new versions of our platform components including Granite 7, our Stylesheet, Icons, and our Flatpak runtime. We'll soon be releasing new versions of all of our packages built on the latest platform.

### What to Expect

Firstly, I know some folks really care about the release code name, so I'm happy to announce that the code name for elementary OS 7 will be Horus! This cycle we're really prioritizing a swift release over packing in tons of features at the initial launch time, so you should expect that generally the feature set difference between 6.1 and 7 will be modest. However, because we release updates throughout the life cycle of the OS, you can expect that more features will land in OS 7 as the year goes on.

Some things to look forward to at release time are nice creature comforts like automatic app updates and power profiles options. We're also debuting a brand new more minimal Music. Some components have already migrated to Gtk4, so you can expect improved performance and smoother animations. Plus a few redesigned app icons.

We won't be making the jump to Wayland this cycle in the interest of prioritizing a swift and stable release. Many of the gears are turning to make Wayland a priority, but it's not quite ready for showtime yet. However, we do have a working prototype for offline release upgrades! Once OS 7 is released, we'll be able to more thoroughly test this and hopefully release the feature for OS 6 quickly.

Speaking of OS 6, some components may continue to receive a slow trickle of updates, but development focus has completely shifted to OS 7. OS 6 should be considered in maintanence mode, so don't expect major new features or fixes besides the previously mentioned upgrade to OS 7. One small consolation is that Flatpak apps in AppCenter will continue to be updated and available for OS 6 users until you're ready to make the jump.

<aside markdown="1">
>The time to update your apps to version 7 of our Flatpak platform is now
</aside>

Developers, the time to update your apps to version 7 of our Flatpak platform is now! Platform 7 is released and available from the AppCenter Flatpak remote for OS 6 users, so you can publish apps with it starting today. At release time, be aware that AppCenter will call out apps using the outdated 6.x runtimes. Platform 7 also includes Gtk4; You're not required to port to Gtk4 right away, but it's a good time to start thinking about it.

Expect lots more details in the OS 7 release post highlighting everything new. In the meantime, if you'd like to get Early Access to see what's coming and give your feedback before release, [you can do so with a $10/mo sponsorship](https://builds.elementary.io/)!
