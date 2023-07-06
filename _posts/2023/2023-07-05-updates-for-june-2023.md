---
title: 
description: Updates for June, 2023
author: danrabbit
image: /images/updates-for-february-2023/card.png

tags:
  - horus
  - updates
---

As promised, this month brings a bunch of new features including a big new accessibility feature and a major platform improvement. Enjoy this month's contributions to the upcoming [OS 7.1](https://github.com/orgs/elementary/projects/122/views/2)!

## AppCenter

As we work towards out continual goal of better supporting alt stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. This month we've rolled out a new set of app sandbox warnings to help you better assess risk when installing apps. AppCenter will now inform you if an app can can read your location without asking first, if it can access system folders or your home folder, if it can read and write system settings, or if it could possibly escape the sandbox altogether and gain advanced permissions. For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent.

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

As part of their aforementioned work, [Gustavo](https://github.com/marukesu) updated Startup settings to show apps that use the Background &amp; Autostart Portal and we make quite a few design changes to this view to bring it in line with modern design patterns and ensure that it was more responsive for large and small displays. We also updated Default apps settings and did quite a bit of code cleanup here. And thanks to [Leo](https://github.com/lenemter) the "Reset to Defaults" button on the Permissions page is now disabled when permissions are already at their defaults, plus he improved screen reader names for several settings while here.

<figure class="half" markdown="1">
![Defaults Settings](/images/{{ page.slug }}/settings-defaults.png){: width="1024" height="720"}
![Startup Settings](/images/{{ page.slug }}/settings-startup.png){: width="1024" height="720"}
<figcaption markdown="1">
Startup and Defaults settings were both redesigned to be more responsive for large and small displays
</figcaption>
</figure>



Online accounts settings, "ImapDialog: Fix freeze when a server sends no response", "ImapDialog: Store most initial setup keys" thanks to Leonhard



Display:
* Nightlight can now be set warmer
* Slight redesign of nightlight settings
* New filters view with color assistance and monochrome filters
* More accurate display resolution options thanks to vjr 


## Files
* Colorful levelbars in properties dialogs
* Bulk rename thanks to Jeremy
* Performance improvements thanks to Jeremy
* Fix issue with getting correct dates Jeremy
* Fix a regression with duplicate Files, Jeremy
* Fix some issues regarding folder sizes
* Avoid showing temp files when renaming or replacing files

## Panel

Updated icons in indicators: nightlight, bluetooth, notifications

Bluetooth indicator:
* Bluetooth sharing by @torikulhabib and Jeremy
* Use device name alias thanks to @stan-janssen

Notifications:
* Remove notifications if the bubble was dismissed Jeremy
* More accurate notification count in tooltip Jeremy
* Better support for markup lenemter
* Better indicator width when empty thanks to leonhard





## Sideload
 make sure open button grabs focus. Fix some visual glithces thanks to lenemter

## Notifications

Notifications: no more "automatic suspend" notifications. "Turning off sounds for "Other" notifications still plays sounds", "Send Critical Notifications regardless of Do Not Disturb"


## Window Manager

Resolve issue where sometimes parent windows wouldn't undim after closing dialogs
Resolve issue with PiP visiblity when switching workspaces

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---


## Early Access Preview

Wayland

Mail. Better sidebar. Move messages. Inline images. Performance improvements. Better offline support.

Background portal: Mail, Calendar, Tasks

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
