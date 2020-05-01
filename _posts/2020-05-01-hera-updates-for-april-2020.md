---
title: "Hera Updates for April, 2020"
description: Screen Time & Limits, a revamped Applications Menu, deep System Settings search, and more for OS 5.1.4
author: cassidyjames
tags:
 - hera
 - updates
---

## Parental Controls → Screen Time & Limits

Informed by our work last year at the [Metered Data & Parental Controls hackfest](/parental-controls-metered-data-hackfest), we've started overhauling Parental Controls. While we're focusing on the digital wellbeing aspects, we decided to rename it to the more straightforward "Screen Time & Limits." But it's more than just a rename; Screen Time & Limits is now available for your own account in addition to other non-administrator accounts on the device—so you can set your own rules around screen time, Internet access, and app usage.

<figure markdown="1">
![Screenshot of Screen Time & Limits](/images/{{ page.slug }}/screen-time-limits.png){: srcset="/images/{{ page.slug }}/screen-time-limits@2x.png 2x" width="989" height="685"}
<figcaption markdown="1">
New _Screen Time & Limits_ settings
</figcaption>
</figure>

As a result of reworking the feature, Screen Time & Limits is also much more reliable than before. If you previously had issues with Parental Controls, give Screen Time & Limits a try from System Settings and let us know what you think.

## Applications Menu

The Applications Menu handles browsing, searching for, and launching both apps and app actions. This month we released a major update that greatly improves its responsiveness and fluidity on trackpads—and makes it easily usable on touchscreens as well. We've also updatd the category view to show apps in a scrollable list instead of a grid, better supporting a classic menu workflow that some users have been asking for.

<figure markdown="1">
![Screenshot of Applications Menu Category View](/images/{{ page.slug }}/applications-menu.png){: srcset="/images/{{ page.slug }}/applications-menu@2x.png 2x" width="755" height="592"}
<figcaption markdown="1">
Redesigned Applications Menu category view
</figcaption>
</figure>

While we were at it, we improved both keyboard navigation and performance throughout the Applications Menu.

## System Settings

Search inside of System Settings has been completely redesigned and significantly improved! Drawing from the excellent search in the Applications Menu, System Settings now supports deep searching for individual settings, and clearly shows the path to get to each one; this helps find what your looking for, but also helps teach you where settings can be found in the future.

<figure markdown="1">
![Screenshot of System Settings search](/images/{{ page.slug }}/system-settings-search.png){: srcset="/images/{{ page.slug }}/system-settings-search@2x.png 2x" width="916" height="681"}
<figcaption markdown="1">
Redesigned search in System Settings {{page.slug}}
</figcaption>
</figure>

We also pushed out updates to several System Settings panes this month.

For the Desktop Settings, we now illustrate dock icon sizes—making it much easier to visualize. We also fixed system wallpapers being duplicated when applied. And we updated search result terms to include the accessibility feautres like text size, window animations, and Panel translucency—these will make it easier to find what you're looking for from the Applications Menu or System Settings search.

<figure markdown="1">
![Screenshot of Desktop Settings](/images/{{ page.slug }}/dock-settings.png){: srcset="/images/{{ page.slug }}/dock-settings@2x.png 2x" width="916" height="681"}
<figcaption markdown="1">
New illustrated Dock size in _System Settings_ → _Desktop_
</figcaption>
</figure>

In Display Settings, we've fixed one-pixel gaps that could show up between displays, plus we now ensure rotated displays are properly centered. In Mouse & Touchpad Settings we've fixed stretched switches when using large text. For User Accounts Settings, we improved how administrator actions work: we show more accurate reasons for settings being locked, plus only ask for administrator permission on demand when enabling or disabling accounts.

## AppCenter

In April we released a major update to AppCenter with performance improvements, extension improvements, keyboard navigation improvements, and a number of fixes.

Performance-wise, AppCenter will now only check for updates at device startup or log in once daily; this ensures users are still getting updates in a timely manner, but AppCenter will be much lighter on CPU and memory usage when logging in multiple times per day. As always, AppCenter will still fetch the latest updates when opening the app. We also reduced slowdowns when opening apps that require AppCenter to fetch extra data.

We've cleaned up extensions in AppCenter: first, to de-clutter the updates view, extensions are only shown when they require an update. Second, selecting an extension from an app info page will take you to an info page for the extension. Lastly, we've swapped the main and overlay icons for extensions to clearly associate extensions with their app.

<figure markdown="1">
![Screenshot of extensions in AppCenter](/images/{{ page.slug }}/appcenter-extensions.png){: srcset="/images/{{ page.slug }}/appcenter-extensions@2x.png 2x" width="1173" height="847"}
<figcaption markdown="1">
Extensions show up on an app's info page
</figcaption>
</figure>

For keyboard users, you'll be happy to know that you can hit the down arrow from the search bar to select the search results. And now, you can hit <kbd>Ctrl</kbd><kbd>F</kbd> anywhere the search bar is enabled to focus it and start a search.

On the fixes front, AppCenter will now use configured network proxies for apt operations, won't show a non-curated warning when updating non-curated apps, and will show a more informative loading screen when checking for updates. We also fixed a crash when updating Flatpaks and system updates at the same time, and prevent the device from suspending when installing, updating, or removing apps or updates.

## Videos

We released several fixes for Videos in April, including better remembering the last-played video and its playback position, more reliably updating the "replay" button description, and fixing a missing icon in the episode view.

## More

Gala: Fix crash when changing workspaces while certain windows are being opened

Greeter: fix an issue with media keys

WingPanel: Fix an issue with some 3 monitor layouts, Reduce spacing between icons

Photos: Add "Open In" menu to photo viewer

## Get It

As always, you can get these updates on elementary OS 5.1 Hera alongside updated translations, bug fixes, and performance improvements by opening AppCenter and hitting **Update All**.

If you're new to elementary OS or would just like a fresh ISO, these updates will be included in a new elementary OS 5.1.4 Hera download on [our homepage](https://elementary.io) soon.
