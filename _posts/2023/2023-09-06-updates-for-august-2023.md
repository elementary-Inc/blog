---
title: One Last Bug Fix Update Before The Big One
description: Updates for August, 2023
author: danrabbit
image: /images/updates-for-august-2023/videos.png

tags:
  - horus
  - updates
---

It turns out we have one more updates blog before OS 7.1 and it brings a number of fixes and a few small features. We're hard at work resolving your reported issues to make this release as smooth and shiny as it possibly can be! So read ahead and find out what was new last month.

## Feedback

The Feedback app has been ported to GTK 4 and it now features search! This should make it much speedier to send feedback when something unexpected happens.

<figure markdown="1">
![Feedback](/images/{{ page.slug }}/feedback.png){: width="570" height="621"}
<figcaption markdown="1">
The Feedback app now features search
</figcaption>
</figure>

The feedback app is our way to stay connected with you and address any issues you come across, so please make sure to make use of it. The issues that we send fixes for every month come directly from folks who make use of this app.

## Videos

We've been hard at work getting Videos ready for GTK 4 and one of the steps along the way was getting rid of Clutter—big "C"—which has lead to a massive rework of the app's internals. The code base is much cleaner and clearer and should be more reliable and performant. This release still uses GTK 3, but look forward to GTK 4 in the next release.

<figure markdown="1">
![Videos](/images/{{ page.slug }}/videos.png){: width="1069" height="747"}
<figcaption markdown="1">
Videos is a wee bit flatter
</figcaption>
</figure>

For now you can expect improved playback position saving, a flatter app appearance in the welcome screen and library, smoother navigation, and in-app notifications when adding items to the playlist. Major shoutouts to [Leonhard](https://github.com/leolost2605) here.

## Files

This release of Files sports a new Tab Bar powered by LibHandy with improved animations, smoother drag-and-drop, and reorganized tab context menus, bringing it more in line with Web. [Jeremy](https://github.com/jeremypw) has also rewritten the way color tags are stored using extended file attributes instead of a database; This means tags should be better preserved when restoring from the Trash for example and you've no need to fear because Files will automatically update your tags to use the new system in the background. He also solved several issues around refreshing and temporary files as well as making sure that tab history is properly preserved when opening Files from another app.

## System Settings

A couple of keyboard settings moved around, but were not removed! On-screen keyboard settings are now on the Behavior tab and panel indicator settings are now available in Desktop → Dock &amp; Panel. [Ryo](https://github.com/ryonakano) fixed an issue that prevented the progress dialog from being shown when installing input method engines, as well as adding multitouch gesture support for navigating backwards through the installation steps, and made sure the <kbd>PrintScreen</kbd> key can be used for keyboard shortcuts. [Leo](https://github.com/lenemter) added the "Cycle Windows of application" and "Cycle Windows of application backwards" shortcuts, fixed an issue with input method switching, and guarded against a potential crasher.

In applications settings, we fixed an issue that caused no default music player to be set on new accounts, and added search to the Permissions tab, thanks to [Leonhard](https://github.com/leolost2605).

## Panel

After receiving quite a bit of feedback about the panel appearing broken when folks modify the system visual assets, the panel now always uses the elementary stylesheet and icons to prevent style issues. You can also now close panel indicators with <kbd>Esc</kbd> and [Leo](https://github.com/lenemter) fixed an issue that caused indicators to re-animate if an indicator was updated or removed.

The Power indicator now always uses hours as its largest unit, for example it will say "26 hours remaining" instead of "1 day remaining" and we resolved an issue that caused battery level icons to sometimes be inaccurate. Thanks to [Leo](https://github.com/lenemter) and [Vishal](https://github.com/vjr).

## And More

[Leonhard](https://github.com/leolost2605) fixed an issue where apps using the new Background &amp; Autostart portal might repeatedly try to add themselves to autostart even when you'd previously disabled them. Another half dozen bug fixes landed in our Window Manager thanks to [Leo](https://github.com/lenemter), including several related to workspaces. Also [Gustavo](https://github.com/marukesu) and [Leonhard](https://github.com/leolost2605) fixed a couple issues related to Notification close behavior.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Early Access Preview

If you're in Early Access we'd love your help testing the new additional drivers option in the installer! The latest daily builds include an installation step for Broadcom Wifi and Nvidia Graphics, so if you've previously had trouble installing elementary OS on devices with that hardware, please give it another try and report back if you experience any issues! Also be on the look out for stable Release Candidate quality builds very soon. We'll send a message through GitHub Sponsors when they're available and as part of Early Access, you'll get to download the stable release of OS 7.1 before anyone else!

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!

---

## Developer Platform

A new release of elementary Icons is out and features a number of refinements thanks to [newhoa](https://github.com/newhoa). Notably, arrow shapes have been improved for many action icons and several icons now appear sharper in dark mode. Plus, several non-freedesktop-named icons related to indicators have been removed since they are now shipped with those components instead of as part of our platform.

Speaking of which, Platform 7.2.1 has been released. You can find the full release notes on [GitHub](https://github.com/elementary/flatpak-platform/releases/tag/7.2.1) but note that this is a fairly minor release just incorporating some recent bug fixes and you will not need to update your Flatpak manifest file for your app to take advantage of this update.

<figure markdown="1">
![Icon Browser](/images/{{ page.slug }}/iconbrowser.png){: width="962" height="651"}
<figcaption markdown="1">
Icon Browser's code sample now updates based on your selection
</figcaption>
</figure>

Finally, a new version of Icon Browser has been released that updates the displayed code sample based on which version of an icon you've selected in the view, so be sure to check that out if you write apps for elementary OS.
