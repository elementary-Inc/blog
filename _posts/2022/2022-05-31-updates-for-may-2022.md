---
title: Updates for May, 2022
description: OS 6 still gets the latest goodies
author: danrabbit
image: /images/updates-for-may-2022/card.jpg

tags:
  - horus
  - jolnir
  - updates
---

We're now in the final stretch with just a handful of issues left to resolve before we can release elementary OS 7. This month there was a large focus on making new stable releases of packages so that we can prepare for building stable images of OS 7. As we've mentioned before, the primary development focus has shifted from OS 6 and some components can no longer be released there. But, for those things which can still be built on both versions, a trickle of updates has landed in OS 6.1 this month.

## Updates for OS 6.1

<figure class="constrained" markdown="1">
![elementary OS 6.1 Jólnir](/images/elementary-os-6-1-available-now/card.png)
</figure>

Thanks to the shift to Flatpak, some apps will be able to receive updates almost indefinitely. This month, folks running OS 6.1 received the latest version of GNOME Web, including all the security, compatibility, and performance improvements in the latest Webkit. Similarly, the Captive Network Assistant also received an update with the latest Webkit. The latest versions of GNOME Archive Manager and GNOME Document Viewer were also made available thanks to Flatpak. It's worth noting that some of the latest open source operating systems released this last month are still shipping older versions of these apps than are available in OS 6.1. We're very proud and excited to ship the latest apps from the GNOME 42 release on a stable, long-term support operating system.

<aside markdown="1">
> OS 6.1 is shipping newer versions of some apps than the latest Open Source operating systems released last month
</aside>

Also of note is the availability of Gtk4 apps. This month's update to Calculator includes a huge code cleanup, but it also includes the jump to Gtk4. If you've already run your updates, you may have been using a Gtk4 app without even knowing it!

Terminal also received a small feature update this month including new keyboard shortcuts for switching tabs (<key>Alt</key> + <key>1</key>—<key>9</key>), and <key>Ctrl</key> + <key>Shift</key> + <key>Q</key> to quit.

In System Settings there's now offline support for newly added CalDAV accounts, and we fixed an issue that prevented the description text in some authentication dialogs from being localized.

Initial Setup now also intelligently offers to switch the primary mouse button for left-handed folks, and suggests connecting to a network.

And lastly, the Settings Daemon has been updated to provide the first day of the week over the Settings Portal and avoids trying to Housekeep the Downloads folder if you've set downloads to go directly to your Home folder.

### Get These Updates

As always, pop open AppCenter on elementary OS 6.1 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

## OS 7 is Nearly Here!

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus]( {{ page.image }})
</figure>




Photos and Calendar icon redesign

### Feedback:
Avoid focus stealing prevention when opening a web browser
Show more entries under Desktop Components

### AppCenter:
Added an option to automatically update apps
Manually check for new updates
Warn when apps are built against older runtimes
Fixes:

Prevent back button from disappearing or requiring multiple clicks
Improvements:

Don't show a warning dialog about apps from alt stores
Show screenshot captions in a tooltip
Show "Try for Free" when setting an app's price to 0
Performance improvements
Updated translations

### Mail
Fixes:

Fixed an error which caused mail accounts to be loaded multiple times
Fixed a bug which caused Mail to crash occasionally
Display recipient in Sent folder instead of sender
Improvements:

Updated app icon
New design
Updated translations

### Onboarding
Add Automatic Updates view
Add Sunset to Sunrise to Style View
Update for OS 7 and Gtk 4
Updated translations

### System Settings
Add power profile management
Forbid new USB devices while locked

### Shortcut Overlay
ported to Gtk4

### Music 7

Complete rewrite. Available for OS 6 users in AppCenter


As always, you can follow along with detailed progress, including an estimated release schedule, [on GitHub](https://github.com/orgs/elementary/projects/94/views/10).

Expect lots more details in the OS 7 release post highlighting everything new. In the meantime, if you'd like to get Early Access to see what's coming and give your feedback before release, [you can do so with a $10/mo sponsorship](https://builds.elementary.io/)!
