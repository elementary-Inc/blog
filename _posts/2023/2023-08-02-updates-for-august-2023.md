---
title: 
description: Updates for August, 2023
author: danrabbit
image: /images/updates-for-august-2023/.png

tags:
  - horus
  - updates
---

This should be the last monthly update before [OS 7.1](https://github.com/orgs/elementary/projects/122/views/2)!

## Mail

Sort special folders to top by @leolost2605 in #910
Allow renaming of folders by @leolost2605 in #911
Fix grouped archive folder by @leolost2605 in #929
Move menu to FoldersListView by @danirabbit in #905

Swipe to archive and trash by @leolost2605 in #930

Move capability by @leolost2605 in #895
Improve move menu and make it searchable by @leolost2605 in #916
FolderPopover: increase white space, natural height, search placeholder by @danirabbit in #923
Unify trash/archive by @leolost2605 in #888

Add support for inline images in the composer by @leolost2605 in #907
Update composing by @leolost2605 in #894
Add support for signatures by @leolost2605 in #900
Include attachments when forwarding by @leolost2605 in #891


WebView: Update height after images were loaded by @leolost2605 in #889
Show an InfoBar if attachments include an ICS file by @leolost2605 in #915

Application: force use of Portals by @danirabbit in #902
Use flatpak portal for background and autostart by @leolost2605 in #882

Always start InboxMonitor by @leolost2605 in #890
Handle network availability by @leolost2605 in #871
Fix an issue that causes mail to never connect to the network by @leolost2605 in #899

Improve performance when moving messages by @leolost2605 in #897
Improve performance when switching between folders by @leolost2605 in #928

## Calendar & Tasks
Tasks:
Fix a small color issue by @leolost2605 in #356
Use flatpak portal for autostart and background permission by @leolost2605 in #361
Fixed Duplicated tasks in Scheduled by @Claudio-code in #365

Calendar:
Create Autostart File Via Background Portal by @Marukesu in #681
Application: Force use of portals by @danirabbit in #717
Style updates by @leolost2605 in #780

## Login &amp; Lock Screen

Compositor: Mask corners by @lenemter in #661

Use user's mouse and touchpad settings by @lenemter in #655
Use user's xkb options by @lenemter in #658
Copy KeyboardManager from Gala by @lenemter in #644
KeyboardManager: Set keyboard layout on startup by @lenemter in #645
Improve handling of users' accent color by @lenemter in #667
Use user's interface settings by @lenemter in #670
Use user's night light settings by @lenemter in #662
Use users' fonts by @lenemter in #677

Compositor: Implement PointerLocator by @lenemter in #674

Fix screenreader shortcut by @lenemter in #668
Save screenreader state between sessions by @lenemter in #669

AccessDialog: Copy changes from Gala by @lenemter in #636
WindowManager: confirm_display_change() Fixes by @lenemter in #637

UserCard: Handle click event using Gtk.GestureMultiPress by @lenemter in #680

Don't reset user settings when entering wrong credentials by @lenemter in #681

Respect solid color wallpaper by @lenemter in #672

## System Settings

Daemon:
Portal: Support accent colors by @alice-mkh in #60
Check for firmware updates by @meisenzahl in #45
Screenshots housekeeping by @Antolius in #56
Expose user's mouse settings by @lenemter in #66
Expose xkb options by @lenemter in #67
Load left handed mode from settings-daemon by @lenemter in #69
Expose interface settings by @lenemter in #71
Expose night light settings by @lenemter in #68
InterfaceSettings: Expose fonts by @lenemter in #73
Sync wallpaper to greeter by @lenemter in #72

Sound:
Plug: place contents in a Clamp by @danirabbit in #240
Output: more vertical layout by @danirabbit in #241
InputPanel: better use vertical space by @danirabbit in #242
OutputPanel: Remove extra margin by @danirabbit in #243
Set volume scales sensitive based on device by @danirabbit in #244
OutputPanel: include screen reader shortcut by @danirabbit in #245
Try to fix crash by @lenemter in #248

Desktop:
Wallpaper: Confirm wallpaper removal when hidden by @lenemter in #359
Dock: add checks for panel indicators by @danirabbit in #358
Dock: redesign by @danirabbit in #360
Multitasking: Remove top margin to match other pages by @lenemter in #362
Rely on settings-daemon to copy wallpaper to greeter by @lenemter in #361

Keyboard:
Add link to custom shortcuts by @lenemter in #443
Behavior: Remove spinbuttons by @danirabbit in #447
Behavior: add a11y settings by @danirabbit in #446

Security & Privacy:
Add screenshot files cleanup option to Housekeeping by @Antolius in #141
LocationPanel: Check that apps are installed before listing by @danirabbit in #160

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

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
