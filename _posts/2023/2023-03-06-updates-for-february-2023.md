---
title: Updates for February, 2023
description: Big new features and a mountain of bug fixes
author: danrabbit
image: /images/updates-for-february-2023/card.png

tags:
  - horus
  - updates
---

elementary OS 7 has been out for just over a month now and I'm excited to announce the first round of updates to our latest operating system includes both great feature updates and a long list of fixes for reported issues. As you may know, we prioritize our work based on your feedback so a big thanks to everyone sending us reports on GitHub and through the Feedback app.

## Files

The headlining feature of this Files release is the new app menu in the headerbar. [Jeremy](https://github.com/jeremypw) put together this menu to better improve discoverability for features like zoom and undo/redo as well as to clean up folder context menus. The Undo and Redo buttons include tooltips showing what operation will be performed before you click them and we also updated the description for the double-click setting to make it more clear.

<figure markdown="1">
![Files](/images/{{ page.slug }}/files.png){: width="1064" height="744"}
<figcaption markdown="1">
Files now has an app menu with app-wide settings and features
</figcaption>
</figure>

We also fixed a number of reported issues including some off click behavior above and below text in the list view, case sensitivity in file path completion, and issues with MTP and PTP devices that have a colon in their name. Plus we reworked how the File Chooser handles typing focus when saving.

## Network Indicator

The network indicator has been getting some major design attention and now offers a much better experience for using VPNs. You'll notice that most options now appear as circular toggle buttons with icons instead of a list of switches. This new design both saves space on devices with complex network configurations and shows the status of your various connections much clearer, including intermediate and error states. In the case of VPNs, you can now also activate multiple connections at once.

<figure class="card" markdown="1">
![Network Indicator](/images/{{ page.slug }}/network-indicator.png)
<figcaption markdown="1">
The Network Indicator has been redesigned with better VPN controls and Airplane Mode
</figcaption>
</figure>

We've also added quick access to toggling Airplane Mode, including a middle-click action on the indicator icon. Plus, we're now using a feature of Network Manager to automatically get better device names so you'll rarely see long and cryptic device names any longer. And you may notice some subtly improved icons like a slightly larger Wi-Fi icon with rounded edges.

## Window Management

This release of our window manager contains over a dozen fixes for reported issues thanks to [Leo](https://github.com/lenemter)'s hard work. This includes things like performance improvements and smoother animations, fixes for issues with shadows, improved ability to optionally disable animations, better handling of keyboard shortcuts in Multitasking View, and lots of code cleanup. Plus a fix that avoids accidentally closing windows when using three-finger multi-touch gestures. I recommend reading the [full release notes](https://github.com/elementary/gala/releases/tag/7.0.1) because this is a big one!

## And More

AppCenter received a new Flatpak Repair feature thanks to [Marius](https://github.com/meisenzahl) which fixes an issue where some Flatpak runtimes could not be installed. Plus the updates page now shows a small message when everything is up-to-date, including the last time that AppCenter checked for updates.

And thanks to the hard work of [Marco](https://github.com/marbetschar) and [Gustavo](https://github.com/Marukesu) our Portals—things like the app chooser and access dialogs—have now been ported to GTK 4!

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Documentation

Also worthy of mention this month is updates to our [developer documentation](https://docs.elementary.io/develop/). The landing page has been redesigned to better answer common questions and now includes a link to [GitHub Discussions](https://github.com/elementary/docs/discussions). Plus, we rewrote our documentation on the [AppCenter Submission Process](https://docs.elementary.io/develop/appcenter/submission-process) to reflect the current app submission workflow. But the biggest new section describes how to use [DBus Activation](https://docs.elementary.io/develop/apis/launchers#actions) to add your app's actions to your launcher's menu in the Dock and Applications Menu, including a brand new full code sample. Shoutouts to [Josip](https://github.com/Antolius) for the research and patience that went into documenting this API in an accessible way.

## Early Access Preview

Folks in early access should look forward to more big changes coming to Indicators and soon AppCenter will be able to report the specific install-time permissions requested by apps. Now that OS 7 is released, expect a bigger focus on new features and larger design changes. If you've been sending us feedback, Early Access is the best way to see changes as quickly as possible and help us refine new features before they are released to the general public.

If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/).
