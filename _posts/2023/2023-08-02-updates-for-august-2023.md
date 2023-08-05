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

## Code

[Jeremy](https://github.com/jeremypw) has been working diligently on this release of Code which closes more than 20 reported issues and brings plenty of improvements to search.

Code now does a better job handling file saving and preventing data loss when files can't be written to their original location. Some busy infobars are now dialogs, and we avoid showing too many aggressive warnings about file saving. And you can now optionally try to continue loading files that contain unknown characters or corrupted content.

Search options are now all available from a new menu, there's now a "match whole words" option, and your search settings are now saved between sessions. The search entry also provides visual feedback when no results are found. We do a better job deciding which string to search if you have both a selection and text in the search entry, and make sure that the "Replace" and "Replace All" buttons are enabled and disabled more accurately.

The Vala symbols outline now correctly matches Code when the style changes after startup, and we fixed issues with styling when no documents are open.

The tab width menu has been reworked quite a bit to more accurately prioritize between your global defaults, per document settings, and editorconfig file. An issue that caused an incorrect column number in the line number menu was fixed.

And an issue that caused excessive reads and writes to settings has been fixed.


Ensure active project at startup (include non-git folders) by @jeremypw in #1254

Show running branch if not master by @jeremypw in #1258

Add ctrl + pageUp and pageDown for switching tabs by @stan-janssen in #1297

Ensure folder items in sidebar always expandable by @jeremypw in #1252

Ensure correct sidebar item is focused, or none, when tab removed by @jeremypw in #1320

## Other Updates

[Jeremy](https://github.com/jeremypw) fixed an issue in Files where sometimes folder contents were incorrect until the folder was refreshed.

[Leo](https://github.com/lenemter) fixed an issue where Picture-in-Picture windows could become unintentionally hidden and made sure parent windows of dialogs are dimmed and undimmed more accurately.

The Sound indicator was updated to use circle buttons and should no longer change size when skipping tracks. Muting should no longer affect monitor sources thanks to [Gran](https://github.com/GranPC), and microphone icons have been subtly updated. Plus, [Leo](https://github.com/lenemter) made sure the Accessibility indicator shows the correct text size on startup.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Early Access Preview

If you're in Early Access there's some new goodies for you to test! Firstly, the latest daily builds now contain Linux 6.2 thanks to the Ubuntu hardware enablement team. Thanks Ubuntu! Additionally, we're testing an option in the Installer to include proprietary drivers when installing; this specifically affects folks with Nvidia graphics or Broadcom networking as well as in certain virtual machines, so we'd love to get your feedback if you've previously failed to install elementary OS due to missing hardware support.

The Installer and Initial Setup now also come with audio directions for enabling the screen reader after a brief timeout. Our hope is that this makes it much easier to install elementary OS for folks with vision-related disabilities. Additionally the Installer now supports two-finger-swipe to go back. If you've previously been unable to or had a difficult time installing elementary OS due to disability, we'd love to hear how we can make your experience better!

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
