---
title: New Features For Mail, A More Personal Lock Screen, And System Settings Improvements
description: Updates for August, 2023
author: danrabbit
image: /images/updates-for-august-2023/.png

tags:
  - horus
  - updates
---

This should be the last monthly update before [OS 7.1](https://github.com/orgs/elementary/projects/122/views/2)!

## Mail

This release of Mail was really a labor of love from [Leonhard](https://github.com/leolost2605) and includes several new features and quality of life improvements. It now also uses the File Chooser Portal when selecting attachments and the Background & Autostart portal—[as previously teased](https://blog.elementary.io/updates-for-june-2023)—so you can control its autostart behavior in System Settings → Applications → Startup. Mail also does a better job handling changes in your internet connection, and can check messages in the background even when not autostarted.

In the sidebar, you'll notice that special folders like "Archive" and "Spam" are better detected and appear at the top level, even for accounts like Gmail that used to hide them as subfolders. You can now also rename folders by secondary-clicking on them and selecting "Rename Folder". An issue was resolved where some accounts with no archive folder displayed their inbox in the Archive for all mailboxes. And you'll notice that Mail's primary menu is now in the bottom right corner of the sidebar. Plus, performance has been improved when switching between folders.

In the conversation list, you can now use a multi-touch swipe or click-and-drag left or right to quickly archive or trash a conversation. In the messages list, there's a new "Move conversation" menu that includes search, and you'll notice that archiving and moving messages can now be undone. Mail now does a better job of calculating message height to avoid extra scroll bars, and a handy infobar is shown when a message includes a calendar invite.

When composing a message, you can now add images inline and you can include attachments in forwarded messages. Plus this release brings support for signatures. You can create as many signatures as you'd like and assign them as the defaults for accounts as needed. The new "Insert signature…" menu makes it easy to swap between any of your saved signatures when composing.

## Calendar & Tasks

Calendar now uses the File Chooser Portal when importing and exporting calendar files, animations when switching months have been updated to match button directions, and it now uses your system accent color instead of its own. An issue in tasks where some tasks could become duplicated was resolved, as well as a small visual issue in dark mode. Both Calendar & Tasks now use the Background & Autostart portal as well, and their autostart behavior can be controlled in System Settings → Applications → Startup. Shoutouts to [Gustavo](https://github.com/marukesu), [Leonhard](https://github.com/leolost2605), and [Claudio](https://github.com/Claudio-code) for their work on office productivity apps this month.

## Login &amp; Lock Screen

Meanwhile, [Leo](https://github.com/lenemter) has recently made it his mission to respect all of your system settings and improve accessibility on the Login &amp; Lock screen. It now does a better job matching your mouse, keyboard, and touchpad settings, including improved keyboard layout handling. Your chosen accent color is now used everywhere—not just on your login card—and it now handles solid color wallpapers. Your text size and font settings, pointer size settings, cursor blink settings, Night Light settings and more are all now respected as well. Plus, the ability to reveal the pointer is now available, the Screen Reader can be enabled with a keyboard shortcut, and it does a better job remembering your Screen Reader settings.

In addition to all of that, an issue that prevented cards from being selected when clicked in certain areas has now been fixed, as well as potential issues with dialogs that use Portals, potential issues with multi-display setups, and an issue where settings would be reset when incorrect credentials were entered. Plus you'll also notice that the Login &amp; Lock Screen now has subtly rounded corners that match the logged in session.

## System Settings

Sound Settings got a bit of a redesign for improved responsiveness on small and large displays and you may notice some improved description labels. Plus, [Leo](https://github.com/lenemter) fixed a reported crash.

The Dock &amp; Panel tab of Desktop settings also received a responsive redesign with added description labels for some settings. Additionally, checkboxes for extra indicators like the Accessibility indicator and the Capslock and Numlock indicators are now centrally located here. Plus [Leo](https://github.com/lenemter) fixed an issue where wallpapers might not get removed when quickly closing System Settings.

The Behavior tab of Keyboard settings got a major update with the additional of several new settings for things like Bounce, Slow, and Sticky keys. Slider values are now shown on drag instead of in a separate widget. Plus, app developers can now link directly to custom shortcuts settings thanks again to [Leo](https://github.com/lenemter).

In Security &amp; Privacy Settings, you now have the option to automatically clean up Screenshot files as part of Housekeeping thanks to [Josip](https://github.com/Antolius). And we now make sure not to show Location settings for apps that have been uninstalled.

Finally, the Settings Daemon will now check for and notify of Firmware updates when they're available thanks to [Marius](https://github.com/meisenzahl) and we support Accent Colors on the Settings Portal thanks to [Alice](https://github.com/alice-mkh)

## Panel

Sound:
PlayerRow: use circle buttons by @danirabbit in #248
PlayerRow: keep label size consistent by @danirabbit in #247
volume-control: don't mute monitor sources by @GranPC in #251
Resource: Update microphone icons by @danirabbit in #255

A11y:
Set correct text size on startup by @lenemter in #53
GreeterWidget: Sync with greeter session by @lenemter in #56

## Code

Ensure active project at startup (include non-git folders) by @jeremypw in #1254
Handle saving to unwritable location better to avoid data loss by @jeremypw in #1262
Make symbol outline aware of follow-system-style setting by @jeremypw in #1265
Show running branch if not master by @jeremypw in #1258
Fix styling when no documents by @jeremypw in #1271
Ensure Replace button (and other search widget) states are mutually consistent by @jeremypw in #1278
Delay asking for save location if cannot determine write access by @jeremypw in #1280
Additional Search options in menu by @jeremypw in #1276
Implement option to show files with unknown characters as new document by @jeremypw in #1283
Do not change document search results unexpectedly on focus in by @jeremypw in #1294
Add ctrl + pageUp and pageDown for switching tabs by @stan-janssen in #1297
Persist search settings by @jeremypw in #1291
Set search entry icon and styleclass according to results by @jeremypw in #1285
Ask save location with dialog by @jeremypw in #1308
Ensure folder items in sidebar always expandable by @jeremypw in #1252
Fix creating duplicates of unwritable files by @jeremypw in #1318
FormatBar: Show column number not buffer offset by @jeremypw in #1342
Handle only relevant settings key changes by @jeremypw in #1345
Use dialog for external changes by @jeremypw in #1309
Sync tab settings by @jeremypw in #1347
Fix searchterm reverts by @jeremypw in #1336
Ensure correct sidebar item is focused, or none, when tab removed by @jeremypw in #1320
Fix logic for clearing search entry by @jeremypw in #1359
Fix spurious external change warnings by @jeremypw in #1354

## Window Manager
PiP: Check workspace before hiding the window by @lenemter in #1708
Keep track of dimmed windows by @lenemter in #1710

## Files
Fix regression adding folder to view (shows children until refreshed) by @jeremypw in #2239

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Early Access Preview

Kernel 6.2

Proprietary drivers

screen reader

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
