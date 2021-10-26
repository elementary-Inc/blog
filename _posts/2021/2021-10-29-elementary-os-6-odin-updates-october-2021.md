---
title: elementary OS 6 Updates for October, 2021
description: 
author: danrabbit
image: /images/elementary-os-6-odin-updates-october-2021/card.png
tags:
  - odin
  - updates
---

It's time for another round of updates to elementary OS 6! This month's updates feature a heavy round of creature comforts, healed papercuts, and paid off technical debt.

## AppCenter

The most noticeable change this month in AppCenter is the new progress indicator when installing, removing, or updating apps. Instead of a separate progress bar, progress is now indicated in a compact way. This greatly improves AppCenter with smaller window sizes and fixes layout issues in views that show a lot of apps like the home page and when showing other apps by an author on the app info page.

[SCREENSHOT]

We also fixed a couple of small regressions introduced recently: apps which contain illicit substances now display the correct icon for this content warning, we no longer show a "Multiplayer" badge for apps with online functionality that aren't games, and we make sure not to show plugins on the home page. We also fixed an issue where $0 app installs were being recorded as paid, ensuring that AppCenter can properly suggest payment the next time you get an update from an app developer you haven't supported yet.

## GNOME Web 40

This month we've made the leap from GNOME Web 3.38 to 40.3 which brings quite a number of improvements including a redesigned tab bar, several performance and stability fixes, and of course rounded window corners! Fans of Firefox sync should note that this feature has moved from the preferences dialog to the "Import and Export" menu.

https://blogs.gnome.org/alexm/2021/03/13/reinventing-tabs/

## Calendar

The seemingly never ending battle against timezones continues this month with fixes for Windows-style timezones in synced events. We also plugged a memory leak when fetching timezone information, and we fixed a regression that prevented Calendar from running in the background and notifying of upcoming events.

## Photos

Now when you open a photo in the previewer, we focus the photo itself right away instead of the save button; This enables navigating with the left and right arrow keys right away.

The actions for "Toggle Sidebar" and "Toggle Photo Info" have been moved from the secondary-click menu of certain views to the main menubutton, hopefully making these customization options more discoverable.

Also, we fixed a potential crash when importing photos with invalid date and time info

## Calculator
Showing advanced controls only affects the focused window
Focus the main text entry on startup
Show the correct window title in Multitasking View
Added 'New Window' Desktop Action

## System Settings

### Locale

Support locales with 3-letter codes
Better support for non-Ubuntu based distributions

### User Accounts

Ensure user information in sidebar updates upon changes
Support locales with 3-letter codes
Performance improvements
Better support for non-Ubuntu based distributions

## Indicators

Applications Menu show secondary click menu for search results
Fix an issue with network indicator where it would try to launch capnet for all connections, not just captive networks
Notifications indicator works on Fedora

## Portals

Settings portal including freedesktop dark style preference
First release of elementary portals which includes the OpenURI/AppChooser portal

## Developer Platform

Granite now uses the settings portal for date and time settings
New stylesheet with support for Hdy.Tabbar and fixes for flat style class titlebars
Flatpak platform bump. Can drop accountsservice from your sandbox holes


## Other Fixes & Updates

And as always, there are translation updates, code cleanups, and other under-the-hood improvements included with these updates across the OS and apps.

<aside markdown="1">
>We prioritize our work based directly off of the feedback we receive
</aside>

If you're experiencing an issue that wasn't fixed in this month's updates—or if you have an idea for a new feature—we'd love to hear from you. You can send your feedback on elementary OS 6 by searching for "Feedback" in the Applications Menu or by navigating to _System Settings_ → _System_ and selecting "Send Feedback". We prioritize our work based directly off of the feedback we receive. Also be sure to check out our [improved issue reporting guide](https://docs.elementary.io/contributor-guide/feedback/reporting-issues) for tips and more info.

If you'd like to follow along with development and see what we're working on and prioritizing for the next monthly updates, check out the [OS 6.1 project board on GitHub](https://github.com/orgs/elementary/projects/90).

## Get These Updates

As always, if you're running elementary OS 6 you can get all of these updates directly from AppCenter by opening up the "Installed" tab and selecting "Update All", and previous OS 6 purchase links from email receipts will be upgraded to the newest version.

If you're not yet running OS 6, we'll be publishing a new 6.0.2 download for a pay-what-you-can price that includes all of these updates [on our homepage](https://elementary.io) soon.

## Special Thanks

Major shoutouts this month to David Hewitt for his work on fixing cross-platform issues. 
