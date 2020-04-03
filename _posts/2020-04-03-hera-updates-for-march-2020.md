---
title: Hera Updates for March, 2020
description: OS 5.1.3 brings improvements and fixes across the board
author: cassidyjames
image: /images/hera-updates-for-march-2020/wireless@2x.png
tags:
 - hera
 - updates

facebook:
mastodon:
reddit:
twitter:
---

Fresh on the heels of the [AppCenter for Everyone Remote Sprint](/appcenter-for-everyone-remote-sprint), we still managed to push out a good amount of updates over the course of March (and early April), bundled up in an OS 5.1.3 update. Let's dive into what's new.

## Code

We continued our quest to make Code the best editor for elementary OS with a [new 3.4 update](https://github.com/elementary/code/releases/tag/3.4.0) this month. A file's Git status now shows in its tooltip in the project sidebar, making it easier to understand what the status icons mean—especially if you're colorblind or just don't remember. We also added an option for explicit case-sensitive find/replace for those times when you want to find or replace the word `foo` but _not_ `Foo`.

<figure>
  <picture>
    <source srcset="/images/hera-updates-for-march-2020/code-dark@2x.png" media="(prefers-color-scheme: dark)">
    <img alt="Code" src="/images/hera-updates-for-march-2020/code-light@2x.png" width="1102" height="759" />
  </picture>
</figure>

A couple of fixes round out the release, including fixing a switch alignment issue in the Font settings and correctly showing the Toggle Comment context menu item whether or not any text is selected.

## Files

We landed several fixes for Files this month. With the [4.4.1 release](https://github.com/elementary/files/releases/tag/4.4.1) we corrected a "New Folder" shortcut label, fixed navigation with back/forward context menu items, ensured the path bar shows the correct path when closing a tab, ensured keyboard shortcuts work immediately after creating or renaming a file, and omitted `file://` in certain user-facing places.

With the [4.4.2 release](https://github.com/elementary/files/releases/tag/4.4.2) we fixed a crash when a device icon is coming from a file, fixed missing device icons, fixed occasional view freezes after renaming files, improved renaming logic when dealing with leading/trailing whitespaces, fixed breadcrumbs sometimes being incorrect at startup, and hide the `file://`` prefix in navigation button menu items.

## Panel & Indicators

We spent some time this month pushing out updates to [the top panel itself](https://github.com/elementary/wingpanel/releases/tag/2.3.0) along with many of the indicators. Importantly, we fixed the panel interfering with certain display setups, like when a secondary display is above the primary display—multi-display users rejoice!

We also fixed an issue with disappearing notifications in the [Notifications indicator](https://github.com/elementary/wingpanel-indicator-notifications/releases/tag/2.1.4), corrected the display of "Unknown Artist" in the [Sound indicator](https://github.com/elementary/wingpanel-indicator-sound/releases/tag/2.1.5), improved performance in the [Session indicator](https://github.com/elementary/wingpanel-indicator-session/releases/tag/2.2.8), and updated translations for many others.

## System Settings

In [System Settings](), we fixed a translation bug for Portuguese; updated the Universal Access settings to deduplicate some settings found elsewhere (as part of our [Curb Cuts effort](/accessibility-features-are-just-features)); added a new "Workspaces" icon and fixed how the Space key works with shortcuts in Keyboard settings; and fixed an issue with cancelling installing languages in the Language & Region settings.

<figure markdown="1">![Wireless Network settings](/images/hera-updates-for-march-2020/wireless.png){: srcset="/images/hera-updates-for-march-2020/wireless@2x.png 2x" width="989" height="685"}
<figcaption>Refreshed design for the Wireless Network settings</figcaption>
</figure>

We released an improved design for the Wireless page in Network settings, which should make it more reliable and clear to join and manage networks. We also updated translations for most of the other settings pages.

## Calendar

This month we released a [minor update to Calendar](https://github.com/elementary/calendar/releases/tag/5.0.4) to fix a few issues; saving event reminders should be more reliable, participant details will be ellipsized if too long, and events should no longer be accidentally rescheduled when editing their title.

## Music

We released [Music 5.0.5](https://github.com/elementary/music/releases/tag/5.0.5) with a couple of fixes and performance improvements. Namely, we fixed removing items from the queue, and we made the sensitivity of the equalizer sliders more reliable when using certain settings.

## Desktop

We released the [3.3 update for Gala](https://github.com/elementary/gala/releases/tag/3.3.0), the component that displays multitasking and manages windows. The update includes keyboard shortcuts in window menus, fixes media keys not working in certain situations, and fixes the displaying of a "Gala Background Services" item in the dock when logging in.

## …and more!

An under-the-hood change this month was the retiring of an old desktop component called [Cerbere](https://github.com/elementary/cerbere). Without getting too into the weeds, our desktop now works more closely with upstream components to ensure the session is launched and managed properly.

A small [update to Terminal](https://github.com/elementary/terminal/releases/tag/5.5.2) adds a new `-t` command-line option to open a new tab, plus fixes accidental URL clicks. [Sideload 1.1](https://github.com/elementary/sideload/releases/tag/1.1.0) now shows the name of the app once the its data has loaded, making it easier to see and remember what you're about to install. And we added a new distinct app icon for Onboarding in [the 1.2 update](https://github.com/elementary/onboarding/releases/tag/1.2.0).

Finally, we released [an update](https://github.com/elementary/granite/releases/tag/5.3.1) to Granite, our library for developers, that better aligns labels in settings sidebars and makes keyboard shortcut labels settable.

### New Releases Tool

To help us (and downstream projects) better track releases, we built out a little [releases tool](https://releases.elementary.io/) this week using the GitHub API, GitHub Actions to automatically keep up up to date, and GitHub Pages for hosting. It's just a start, but it's already super handy with a clear design, responsive layout, and automatic light/dark styles based on your browser.

Try it out at [releases.elementary.io](https://releases.elementary.io/). Want to see how it works or adapt it to your own uses? Check out the [source code on GitHub](https://github.com/elementary/releases).

## Get It

As always, you can get these updates on elementary OS 5.1 Hera alongside updated translations, bug fixes, and performance improvements by opening AppCenter and hitting **Update All**.

If you're new to elementary OS or would just like a fresh ISO, these updates are included in the new elementary OS 5.1.3 Hera download on [our homepage](https://elementary.io).
