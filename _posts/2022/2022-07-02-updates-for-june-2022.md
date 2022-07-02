---
title: Updates for June, 2022
description: The focus turns back to OS 6 while we're stuck on OS 7
author: danrabbit
image: /images/elementary-os-6-odin-updates-september-2021/card.jpg

tags:
  - horus
  - jolnir
  - updates
---

This month saw quite a number of updates for OS 6.1 including some nice feature updates, bug fixes, performance improvements, and more.

<figure class="constrained" markdown="1">
![elementary OS 6.1 Jólnir](/images/elementary-os-6-1-available-now/card.png)
</figure>

## Network Indicator 
* better support for VPNS, and correctly reports WPA3 networks

## Printer Settings

<figure class="half" markdown="1">
![Redesigned Printer Settings](/images/updates-for-june-2022/printer-main.png){: width="1039" height="735"}
![Redesigned Add Printer Dialog](/images/updates-for-june-2022/printer-new.png){: width="611" height="427"}
<figcaption markdown="1">
**Left:** A redesigned print queue and add/remove | **Right:** Drivers now show more info including language
</figcaption>
</figure>

Major shoutouts to Jeremy who took ownership on printer settings this month. We landed several design improvements including making it clearer to add and remove printers, improvements to the way ink levels are shown, a redesign print queue, and much more information descriptions when selecting a print driver. You can now also clear the print queue per printer, and the sidebar and print queue are much more reliable.

## Files
Fixes:

Renaming with the same name no longer shows an error dialog
Ctrl + A when renaming now selects all the text in the entry
Selecting multiple items with Shift + Arrow keys now works properly
The appearance of the cursor now matches the action
The Trash sidebar item can no longer be removed
Network sidebar plugins such as NextCloud are now added correctly
Duplication of subfolders in ListView under some circumstances is fixed
Bookmarks are now highlighted when a file they can accept is dragged onto them
Folders not being restored properly under some circumstances is fixed
Show confirmation dialog in file chooser before overwriting an existing file
Ctrl + V now always pastes into background folder
Shift + Ctrl + V now pastes into selected folder if there is one

## Tasks
Add offline support for newly created task lists in case its configured for the account
Automatically synchronize a task list whenever it is selected or the network becomes available again

## Notifications
Fix missing icons in some cases

## Camera

Support MJPEG cameras
Take a photo or video on secondary-click

Show error in case no camera device is available
Ensure brightness, contrast, and mirror continue working after taking a photo
Wider hardware compatibility (e.g. StarBook Mk V)
Ensure photos saved properly
Minor updates:

Improved performance and reliability
Updated translations

## Get These Updates

As always, pop open AppCenter on elementary OS 6.1 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

## OS 7 will be a little longer

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

If you've been watching the OS 7 project board, you may have noticed that we've gotten a little stuck. The major release blocking issues right now are the same ones that we had last month and are proving difficult to resolve. We're so close and we want to deliver OS 7 as soon as possible, but these are real show stoppers that we can't release without fixing. Hang tight!

---

Expect lots more details in the OS 7 release post highlighting everything new. In the meantime, if you'd like to get Early Access to see what's coming and give your feedback before release, [you can do so with a $10/mo sponsorship](https://builds.elementary.io/)!
