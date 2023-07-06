---
title: Big Feature Updates for Accessibility, Privacy, Security, and More
description: Updates for June, 2023
author: danrabbit
image: /images/updates-for-june-2023/color-protanopia-hc.png

tags:
  - horus
  - updates
---

As promised, this month brings a bunch of new features including a big new accessibility feature and a major platform improvement. Enjoy this month's contributions to the upcoming [OS 7.1](https://github.com/orgs/elementary/projects/122/views/2)!

## AppCenter

As we work towards our continual goal of better supporting alternative app stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. This month we've rolled out a new set of app sandbox warnings to help you better assess risk when installing apps. AppCenter will now inform you if an app can can read your location without asking first, if it can access system folders or your home folder, if it can read and write system settings, or if it could possibly escape the sandbox altogether and gain advanced permissions. For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent. Expect more of these types of warnings to roll out in the future!

<figure markdown="1">
![AppCenter](/images/{{ page.slug }}/appcenter-permissions.png){: width="1198" height="901"}
<figcaption markdown="1">
AppCenter now warns about advanced Flatpak sandbox permissions
</figcaption>
</figure>

AppInfo views have also been reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops. Plus, we no longer split out apps from alt stores into a separate header in category views, and a potential crash when adding alt stores has been fixed thanks to [Marius](https://github.com/meisenzahl)

## Portals

Another big part of our consent story with apps are Portals. Portals keep apps isolated from your private data and ensure that apps ask before making changes to the system or using features that could become intrusive. This month [Leonhard](https://github.com/leolost2605) and [Gustavo](https://github.com/marukesu) implemented the Background &amp; Autostart Portal which alerts you when apps are running in the background and makes sure that apps ask your permission before they can automatically start up when you turn on your device. There's still a good amount of work to do on our background apps story, but this sets the foundation.

## System Settings

As part of their aforementioned work, [Gustavo](https://github.com/marukesu) updated Startup settings to show apps that use the Background &amp; Autostart Portal and we made quite a few changes to this view to bring it in line with modern design patterns and ensure that it was more responsive for large and small displays. We also updated Default apps settings and did quite a bit of code cleanup here. And thanks to [Leo](https://github.com/lenemter) the "Reset to Defaults" button on the Permissions page is now disabled when permissions are already at their defaults, plus he improved screen reader names for several settings while here.

<figure class="half" markdown="1">
![Defaults Settings](/images/{{ page.slug }}/settings-defaults.png){: width="1024" height="720"}
![Startup Settings](/images/{{ page.slug }}/settings-startup.png){: width="1024" height="720"}
<figcaption markdown="1">
Startup and Defaults settings were both redesigned to be more responsive for large and small displays
</figcaption>
</figure>

We're also introducing a new set of display filters, designed to assist folks with color deficiency issues. This is a very common disability with 1 in 12 men experiencing color deficiency and some folks developing color deficiency as they age. Major shoutouts to [Leo](https://github.com/lenemter) for implementing this feature in our window manager and to [@G-dH](https://github.com/G-dH) for developing [the GNOME Shell extension](https://github.com/G-dH/gnome-colorblind-filters) that we modeled our feature off of. If this is a feature that you're looking forward to using, please consider [buying them a coffee](https://buymeacoffee.com/georgdh).

<figure class="card quarter" markdown="1">
![Default colors](/images/{{ page.slug }}/color-default.png){: width="1920" height="1080"}
![Protanopia Filter](/images/{{ page.slug }}/color-protanopia.png){: width="1920" height="1080"}
![Protanopia High Contrast Filter](/images/{{ page.slug }}/color-protanopia-hc.png){: width="1920" height="1080"}
![Deuteranopia Filter](/images/{{ page.slug }}/color-deuteranopia.png){: width="1920" height="1080"}
![Deuteranopia Hight Contrast Filter](/images/{{ page.slug }}/color-deuteranopia-hc.png){: width="1920" height="1080"}
![Tritanopia Filter](/images/{{ page.slug }}/color-tritanopia.png){: width="1920" height="1080"}
![Grayscale Filter](/images/{{ page.slug }}/color-grayscale.png){: width="1920" height="1080"}
<figcaption>A number of new display filters are available to assist with color deficiency</figcaption>
</figure>

Additionally, we're now shipping a grayscale filter which can help avoid distractions or alleviate screen addiction and you can now make the display much warmer when using Night Light. You may also notice a small redesign of Night Light settings for responsiveness. Finally, there should be more accurate display resolution options available thanks to [Vishal](https://github.com/vjr).

<figure class="half" markdown="1">
![Night Light Settings](/images/{{ page.slug }}/settings-nightlight.png){: width="990" height="686"}
![Filters Settings](/images/{{ page.slug }}/settings-filters.png){: width="990" height="686"}
<figcaption markdown="1">
Nightlight settings have been slightly redesigned and Filters are available as a new tab in Display Settings
</figcaption>
</figure>

There's also a new version of Online Accounts settings thanks to [Leonhard](https://github.com/leolost2605) which fixes a freeze when the server doesn't respond while adding an IMAP account, and improves support for special folders like Archive and Sent folders.

## Files

A long requested feature, this month Bulk Rename lands in Files thanks to [Jeremy](https://github.com/jeremypw). With this feature, you can select a number of files, secondary-click, and select "Rename…" to get an advanced bulk renaming dialog. This is an especially useful feature if you're working with a large collection of photos or spreadsheets or other kinds of files that you may want to rename by creation date or using another sequence or when you have to format a large number of files the same way. We're looking forward to your feedback on this feature and improving it to fit your advanced file management needs!

<figure markdown="1">
![Files bulk rename](/images/{{ page.slug }}/files-rename.png){: width="990" height="516"}
<figcaption markdown="1">
You can now rename a large selection of files at once
</figcaption>
</figure>

He also fixed several reported issues in this release related to folder sizes, file creation dates, temporary and duplicate files, and even snuck in some performance improvements. Also, the storage level bar in Properties dialogs will now change color depending on how full a drive is.

<figure markdown="1">
![Bluetooth sharing](/images/{{ page.slug }}/bluetooth-sharing.png){: width="472" height="572"}
<figcaption markdown="1">
You can share files via Bluetooth from the secondary-click menu
</figcaption>
</figure>

Plus, thanks to a joint effort between [Jeremy](https://github.com/jeremypw) and [Torikul](https://github.com/torikulhabib), you can now share files via Bluetooth. A new Bluetooth transfer dialog is available by secondary-clicking a file or selection of files and selecting "Send Files via Bluetooth" from the menu.

## Panel

As part of the aforementioned Bluetooth file transfer feature, you can see ongoing transfers in the Bluetooth indicator. And thanks to [Stan](https://github.com/stan-janssen), Bluetooth devices will now use any custom device names you've set up before falling back to more generic device names.

We now do a better job making sure notification bubbles you've dismissed with a swipe or the close button don't end up in the Notifications indicator, and the number of missed notifications in the tooltip should be more accurate, thanks again to [Jeremy](https://github.com/jeremypw). [Leo](https://github.com/lenemter) improved support for notifications that contain markup and [Leonhard](https://github.com/leolost2605) fixed the change in indicator width when all notifications have been cleared.

Plus, we updated some icons in the Bluetooth, Night Light, and Notifications indicators to be more consistent.

## Other Updates

[Leo](https://github.com/lenemter) fixed some visual glitches in Sideload and made sure the "Open" button can be activated when pressing <kbd>Enter</kbd> after installing. He also removed the intrusive "Automatic Suspend" notifications, fixed an issue where sometimes parent windows wouldn't un-dim after closing dialogs, and made sure Picture-in-Picture windows update their visibility properly when switching workspaces.

Gustavo made sure critical notifications are still sent even when Do Not Disturb is active and contributed quite a bit of code cleanup in the notifications server. And new contributor [Sean](https://github.com/SuperRiderTH) made a fix for the option to disable sounds from notifications sent by apps that don't properly identify themselves.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Early Access Preview

Building off our work on the Background &amp; Autostart Portal, you'll notice in Early Access that Calendar, Mail, and Tasks can now be managed from System Settings → Applications → Startup. Plus Mail is gearing up for a big feature release with an improved sidebar, the ability to move messages, the ability to add images inline, performance improvements and better offline support. Plus, be on the lookout for signatures and improved calendar invite handling soon. We'd appreciate your help testing all of these features before releasing them to the general public.

But the big new Early Access feature is Wayland! That's right, a usable Wayland session is finally available. You can choose to test Wayland from the login and lock screen by selecting the gear menu on your login card and choosing "Pantheon (Wayland)". Keep in mind that the Wayland session is highly experimental and you'll certainly run into issues immediately, the most noticeable of which are the lack of a Dock, broken panel positioning, and other issues with positioning certain windows. There is a whole lot of work to do until it's ready for primetime, but we would love your help testing and reporting issues to make sure there's a smooth transition. With your help, I'd love to see Wayland as a viable option for elementary OS 8. Special thanks here go to [Corentin](https://github.com/tintou), [David](https://github.com/davidmhewitt), and [Leo](https://github.com/lenemter) for all of their hard work on preparing our window manager for Wayland.

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
