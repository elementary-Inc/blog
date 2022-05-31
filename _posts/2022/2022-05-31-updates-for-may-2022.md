---
title: Updates for May, 2022
description: OS 6 still gets the latest goodies
author: danrabbit
image: /images/elementary-os-6-odin-updates-september-2021/card.jpg

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

Terminal also received a small feature update this month including new keyboard shortcuts for switching tabs (<kbd>Alt</kbd> + <kbd>1</kbd>–<kbd>9</kbd>), and <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Q</kbd> to quit.

In System Settings there's now offline support for newly added CalDAV accounts, and we fixed an issue that prevented the description text in some authentication dialogs from being localized.

Initial Setup now also intelligently offers to switch the primary mouse button for left-handed folks, and suggests connecting to a network.

And lastly, the Settings Daemon has been updated to provide the first day of the week over the Settings Portal and avoids trying to Housekeep the Downloads folder if you've set downloads to go directly to your Home folder.

### Get These Updates

As always, pop open AppCenter on elementary OS 6.1 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

## OS 7 is Nearly Here!

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

In case you missed it, [I streamed a few days ago](https://www.youtube.com/watch?v=UKp4xs1_AuU) walking through the remaining tasks before releasing OS 7 as well as showing off some of the changes that have landed and answering your questions. To briefly recap:

* You can always get the latest information, including an estimated release schedule, by following along with our [OS 7 Project board on GitHub](https://github.com/orgs/elementary/projects/94/views/1)
* The remaining work is largely centered around resolving Mutter-related regressions in Gala. If you're an expert with Mutter or Clutter, [your help](https://github.com/elementary/gala/issues) is always appreciated!
* This month, a lot of focus was on filling out the elementary Stable PPA on Launchpad which is required to build stable OS releases. Some of the more notable releases below:

### AppCenter

The headlining feature for AppCenter in OS 7 is the introduction of automatic app updates. You can now choose to have all installed Flatpak apps receive their updates automatically. There's also now a menu with an option to manually check for new updates. And on app info pages, we'll show a warning when apps are built against outdated or abandoned runtimes so you can be well-informed about whether an app you're interested in is receiving regular updates.

We've also removed the warning dialog for apps coming from alternative stores like Flathub and have reduced or removed other instances where AppCenter apps were being favored without legitimate reason. We're always listening to your feedback and we want to do a better job ensuring that AppCenter helps you make informed choices without being overbearing and while avoiding any feelings of vendor lock-in.

Lastly a lot of work has gone into improving performance and making navigation more reliable. A future update will soon improve this even further, so look forward to a quicker and smoother experience discovering new apps and managing your installed ones.

### Music

The first stable release of the brand new Music was published and is even available for folks running OS 6 in AppCenter. This rewrite is about rethinking the role of the Music app in the current landscape. We're excited for you to try this more minimal take on the Music app and we're looking forward to improving it with your feedback.

### Design Updates

Several apps have received updated or redesigned app icons including Photos, Calendar, Mail, and Multitasking. We're tracking a more complete refresh of app icons [here in GitHub](https://github.com/orgs/elementary/projects/110), most of which will come as updates throughout the OS 7 lifecycle. Mail also received a visual refresh with a flatter, pane-focused design that you can look forward to. Overall, the design changes between OS 6 and the first release of OS 7 will be small and subtle, with larger changes coming later.

---

Expect lots more details in the OS 7 release post highlighting everything new. In the meantime, if you'd like to get Early Access to see what's coming and give your feedback before release, [you can do so with a $10/mo sponsorship](https://builds.elementary.io/)!
