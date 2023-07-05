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

AppInfo views have been reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops.

* Show Flatpak permissions for location, settings, system and home folder access, sandbox escape
* Category Views: don't split out apps from alt stores anymore
* Fix a potential crash when adding alt stores thanks to @meisenzahl



## Files
* Colorful levelbars in properties dialogs
* Bulk rename thanks to Jeremy
* Performance improvements thanks to Jeremy
* Fix issue with getting correct dates Jeremy
* Fix a regression with duplicate Files, Jeremy
* Fix some issues regarding folder sizes
* Avoid showing temp files when renaming or replacing files




## System Settings

Online accounts settings, "ImapDialog: Fix freeze when a server sends no response", "ImapDialog: Store most initial setup keys" thanks to Leonhard

Applications:
* Show autostart apps created by background portal thanks to @Marukesu
* Rewrite defaults view and startup view to be more responsive, use modern design patterns, lots of code cleanup
* Better screenreader names thanks to @lenemter
* Permission reset to default button now insensitive when resetting would do nothing thanks to @lenemter

Display:
* Nightlight can now be set warmer
* Slight redesign of nightlight settings
* New filters view with color assistance and monochrome filters
* More accurate display resolution options thanks to vjr 


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



## Portals

Background portal thanks to @leolost and @marukesu

## Sideload
 make sure open button grabs focus. Fix some visual glithces thanks to lenemter

## Notifications

Notifications: no more "automatic suspend" notifications. "Turning off sounds for "Other" notifications still plays sounds", "Send Critical Notifications regardless of Do Not Disturb"


## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---


## Early Access Preview

Wayland

Mail. Better sidebar. Move messages. Inline images. Performance improvements. Better offline support.

Background portal: Mail, Calendar, Tasks

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). As you can see, there's a lot of new stuff to test right now!
