---
title: OS 6 Updates for August, 2021
description: Just three weeks since the release, and we already have more goodies
author: danrabbit
image: /images/elementary-os-6-odin-released/odin.png
tags:
  - odin
  - updates
---

Earlier this month we released elementary OS 6 Odin and we've been absolutely overwhelmed with the amount of feedback we've received. So far OS 6 has been downloaded from our website [nearly 75,000 times](https://plausible.io/elementary.io?period=month&goal=Download)! Over the last three weeks we've been gathering up all of your feedback and jumping right into delivering the first batch of free fix and feature updates for OS 6.

# AppCenter & Sideload

If you found AppCenter a little sparse on release day, you might want to take another look! App developers have begun releasing compatible versions of their apps and we're currently up to [51 apps now available](https://appcenter.elementary.io/) in OS 6. We've been in touch with developers and there's quite a few more in the queue, so hang tight if a favorite hasn't made its way in yet.

If you're not running elementary OS but still want to get these AppCenter apps, we've made it much easier with a recent update to our [AppCenter website](https://appcenter.elementary.io/): Free apps now include a "Download as Flatpak" button that will give you a Flatpak reference file which you can sideload on your operating system of choice. Enjoy!

We've also been putting a lot of work into the first run experience, especially with regards to sideloaded apps from third-party stores like Flathub. Apps from freshly sideloaded remotes should now show in AppCenter without needing to restart your computer first. We've added a reminder about Sideload when searching returns no results with the same language that is used in the Welcome app. We now ensure that apps predictably default to installing per-user when selected from the home page. Also, both AppCenter and Sideload can now use system-wide installed app runtimes for per-user app installs, which means the first time you install a new app should be a faster, smaller download.

We've also addressed an issue with apps not opening from in-app notifications, there is a less abrupt transition when choosing which source to download an app from, and AppCenter will now pull in Linux kernel headers when installing device drivers that use DKMS. Plus, we've reworked the way the applications menu watches for changes in installed apps, so it should be more responsive about showing freshly installed apps.

# Online Accounts, Tasks, Mail, and Calendar

Our brand new Online Accounts system has seen a little love around IMAP accounts: we now do a better job of detecting the correct authentication method for accounts and you can edit existing accounts by selecting the pencil icon in its row.

The latest release of Calendar includes a fix for an issue with some all-day events displaying incorrectly, and we do a better job of getting calendar colors from online accounts.

We've heard reports of some folks having issues with online accounts and Tasks and have narrowed it down to restrictions with app sandboxing. For now we've decided to ship Tasks as a traditional deb package by default to work around this issues while we work toward a more long-term solution.


# Files

Fix small context menus on breadcrumbs
Fix bookmarking a single selected item with Ctrl + D
Fix renaming bookmarks in the sidebar
FIx an issue with showing color tags when thumbnails are hidden


# System Settings

Use formatted device name when available
Display more information for certain GPUs, including Intel® Xe Graphics


Ensure the "Use this display" switch works in more circumstances


Add toggle for showing battery percentage in Panel

Fix a potential issue with resuming from sleep


Improve restoring Bluetooth state on restart and resuming from suspend

# Installer & Initial Setup

Fix the Taiwan thing
Fix styles for "Unused" disk partitions
Ensure a usable hostname


Confirm and change device name
Two-finger swipe to navigate back

# Other Fixes

Ensure accel_to_string works with multiple modifiers
Fix locale issues in Flatpaks

Include window decorations in screenshots for server-side decorated windows

Power Indicator
Show brightness level when scrolled
Show battery percentage automatically at 20% or lower
Match scroll direction with Sound indicator
Show "Fully Charged" at 100% when plugged in

- grub is updated correctly when needed
- No more visible grub on regular boot
- Shim/Dell EFI fix
- Latest 20.04.3 repos

If you're experiencing an issue that wasn't fixed in this round of updates or you have an idea for a new feature, we'd love to hear from you! You can send your feedback to the team using the Feedback app by searching for "Feedback" in the applications menu or by navigating to System Settings → System and selecting "Send Feedback" at the bottom of the window. Alternatively, you can file issue reports or start discussions [on GitHub](https://github.com/elementary). The team prioritizes our work based directly off of the feedback we receive through GitHub, so it's the best way to make sure your voice is heard.

Also, mention ARM without being too committal

# Get These Updates

As always, if you're running elementary OS 6 you can get all of these updates directly from AppCenter by opening up the "Installed" tab and selecting "Update All". If you're not yet running OS 6, we've published a shiny new download for a pay-what-you-can price that includes all of these updates [on our homepage](https://elementary.io).

# Special Thanks

Shoutouts to Marco. More info on his blog about fixes and features he's working on: https://www.marco.betschart.name/blog/2021-08-30-elementary-os-6-post-release-bugfixing

Also shoutouts to David for Flatpak and Applications menu fixes
