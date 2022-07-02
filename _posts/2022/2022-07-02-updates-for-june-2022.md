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

## Files

A slew of bug fixes landed in Files this month. Selecting multiple items by holding <kbd>Shift</kbd> and using arrow keys now works more reliably. Pressing <kbd>Ctrl</kbd><kbd>V</kbd> now reliably pastes into the currently viewed folder, while <kbd>Shift</kbd><kbd>Ctrl</kbd><kbd>V</kbd> pasts into the selected folder, if there is one. Pressing <kbd>Ctrl</kbd><kbd>A</kbd> while renaming now properly selects all text in the entry, and canceling without renaming no longer shows an error message. 

<figure markdown="1">
![File Chooser Confirmation Dialog](/images/updates-for-june-2022/files-confirm.png)
<figcaption markdown="1">
The File Chooser now double checks that you really want to overwrite that file
</figcaption>
</figure>

Network sidebar plugins such as NextCloud are now added correctly, the Trash item can no longer be removed from the sidebar, and bookmarks are now highlighted when dragging a file into them. The appearance of the pointer more accurately reflects the action it will take—especially handy in list and column view—and we now show a confirmation dialog in the file chooser before overwriting an existing file. Plus, a couple of intermittent issues were resolved with duplicate subfolders in list view and previous sessions not being restored accurately.

## Camera

The latest release of Camera now supports more types of cameras including MJPEG cameras, and it shows an error message in case no camera is available. It also does a better job of properly saving photos with different types of cameras, and we ensure brightness, contrast, and mirror settings persist after taking a photo. Plus, we improved performance and stability.

## Tasks

Tasks now does a better job keeping your task list in sync by automatically syncing a task list when you select it as well as when your network becomes available after having been disconnected. Plus we now have offline support for newly created task lists when it is configured for the account.

## Printer Settings

<figure class="half" markdown="1">
![Redesigned Printer Settings](/images/updates-for-june-2022/printer-main.png){: width="1039" height="735"}
![Redesigned Add Printer Dialog](/images/updates-for-june-2022/printer-new.png){: width="611" height="427"}
<figcaption markdown="1">
**Left:** A redesigned print queue and add/remove | **Right:** Drivers now show more info including language
</figcaption>
</figure>

Major shoutouts to Jeremy who took ownership on printer settings this month. We landed several design improvements including making it clearer to add and remove printers, improvements to the way ink levels are shown, a redesign print queue, and much more informative descriptions when selecting a print driver. You can now also clear the print queue per printer—a convenient privacy feature for shared computers—and the sidebar and print queue are much more reliable.

## And More

Notifications was updated to fix some cases where notification bubbles weren't showing the correct icon. The network indicator now correctly reports info for WPA3 networks and does a better job handling VPNs.

## Get These Updates

As always, pop open AppCenter on elementary OS 6.1 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

## OS 7 will be a little longer

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

If you've been watching the OS 7 project board, you may have noticed that we've gotten a little stuck. The major release blocking issues right now are the same ones that we had last month and are proving difficult to resolve. We're so close and we want to deliver OS 7 as soon as possible, but these are real show stoppers that we can't release without fixing. Hang tight!

---

Expect lots more details in the OS 7 release post highlighting everything new. In the meantime, if you'd like to get Early Access to see what's coming and give your feedback before release, [you can do so with a $10/mo sponsorship](https://builds.elementary.io/)!
