---
title: OS 7 Updates and More OS 8 News
description: Updates from the end of the year and the holidays
author: danrabbit
image: /images/updates-for-january-2024/web.png

tags:
  - horus
  - updates
---

It's a new year and that means we're back from the holidays with new updates!

We're now shipping the latest GNOME Web which includes a new Tab Overview mode. Plus we're shipping some updated icons for things like the animated downloads icon in the Headerbar and hardware access icons. And we fixed an issue that would cause the bookmarks popover to be very narrow.

<figure markdown="1">
![GNOME Web](/images/{{ page.slug }}/web.png)
<figcaption markdown="1">
GNOME Web now has a Tab Overview mode
</figcaption>
</figure>

A new version of our Window Manager is out which fixes 10 reported issues including several related to multi-monitor and workspaces. This will be the last release of our Window Manager for OS 7 as we've started introducing large breaking changes for OS 8.

New versions of Network Settings and the Network indicator have been released that bring support for Wireguard VPNs and Opportunistic Wireless Encryption. This is likely the last update that we will see for Settings in OS 7 as well.

In case you missed [our OS 8 post](https://blog.elementary.io/lets-talk-os-8/) in November, I want to repeat that at this point our development focus has shifted to this new version of elementary OS, so the number of updates for OS 7 will continue to slow down as we get nearer to the release. Where possible, we'll continue to release fixes and small feature updates to OS 7 but there are quite a number of larger breaks that prevent backporting.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## OS 8 Early Access

As previously mentioned, our development focus is on the next major version of elementary OS and several of our major projects are coming along nicely.

### GTK 4

The Authentication dialog—also known as the Polkit Agent—has now been ported to GTK 4. System Settings now has complete GTK 4 ports for 12 of its 20 panes. 2 of the remaining panes are awaiting final review and 5 have at least made some progress on porting. Which means there is only 1 pane which doesn't have at least a work in progress branch. As part of the porting process, we've been taking the time to really clean up much of this Settings code which has existed for a decade or more and modernizing the design while improving support for screen readers.

### Dock

We recently merged a branch in the new Dock to vastly improve Drag and Drop support both for reordering apps inside the dock and when dragging apps from the Applications Menu. We also merged in support for badges and progressbars and quick actions in context menus. Plus the ability to add and remove apps to the dock from the Applications Menu's context menu. These are all features you already expect from the current dock in OS 7, but we're excited that the new Dock is quickly reaching feature parity and in a way that works with Wayland and is built completely using GTK 4 instead of custom Cairo drawing.

### And More

While we're taking on some large projects to adopt the latest technology we also aren't neglecting bug fixes and feature requests. Notifications now appear on the left for RTL languages, and sound change confirmations will no longer appear over the sound indicator if it's open. We've also added support for horizontal swipe gestures for switching windows and an option to disable hotcorners for workspaces with fullscreen apps. Several larger pieces of work are still drafting such as support for the Screenshot Portal and some design changes for the Multitasking View that bring in more color. Plus, opaque panel styles received some attention and now have a soft shadow 

<figure class="card half" markdown="1">
![Panel in light style](/images/{{ page.slug }}/panel-light.png)
![Panel in dark style](/images/{{ page.slug }}/panel-dark.png)
<figcaption>The Panel's opaque styles now have a soft shadow</figcaption>
</figure>

The current status of OS 8 builds in Early Access is that they are not installable, but you can run a Demo Mode session! Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/).
