---
title: Loki Updates for The New Year
description: >-
  We have another set of updates with fixes and new features headed your way!
  Without further ado, let’s dive in.
date: '2017-01-25T18:44:19.076Z'
categories: []
keywords: []
slug: /@DanielFore/loki-updates-for-the-new-year-ff6b6ba65531
---

### Photos

The biggest change landing in Photos is the redesigned metadata sidebar. It features new iconography and a layout that makes it easier to spot camera settings for a given photo. It also displays the location of the photo in a human-readable format instead of by latitude and longitude and file size information is displayed in the same format as Files for familiarity. Overall, the new layout seeks to provide all the same information as the old design, but in an organized and visually pleasing way.

![](https://cdn-images-1.medium.com/max/800/0*w9EpKnpJk1LhhCkJ.)

Photos also received a few fixes and improvements to keyboard shortcuts and navigation. `Ctrl + S` and `Ctrl + Shift + S` now perform “Save” and “Save As” respectively in the photo viewer mode, the `[` key will now rotate photos counterclockwise, and you can navigate to the previous or next photo with the arrow keys.

Another big upgrade is support for Gifs! Photos will now include them as part of your library and preview them with the photo viewer. And of course this release includes a number of fixes and cleanups under the hood including stability and translation fixes.

### Files

Files has always been able to perform a full search using the shortcut `Ctrl + F`, but in the latest release it will also perform that search any time you begin typing. We hope this makes the search feature more discoverable and easily accessible. This release also contains a number of stability fixes, code cleanups, and small HiDPI fixes.

### Parental Controls

This is a brand new component for us and getting feedback is super valuable to make sure that we’ve covered all of the bases when in use out in the wild. We sorry to say that we found a major issue in Parental Controls that was preventing the service from being properly installed, meaning that in some cases it was not running at all. But our team was able to pinpoint the issue and this is now corrected. Parental Controls should be working as expected. We know that this is a very important feature for the adoption of elementary OS, especially for public computers. So we’re glad to have this fixed.

### Network Indicator

Making sure that we communicate the correct state of the system is very important for our indicators. So now, when Airplane mode is engaged, we show the airplane icon in place of the network status. We’ve also added a small “lock” badge when connected to a VPN. For those of you that use Docker, we now ignore virtual interfaces in the list of networks to connect to.

![](https://cdn-images-1.medium.com/max/800/0*B2V8xMEYiMfiGHP9.)

### Applications Menu

The Applications Menu received long-awaited fixes for CJK input methods and now sports some stylish new pager dots instead of numbered buttons.

![](https://cdn-images-1.medium.com/max/800/0*YCvRQ0D0NGRog_u1.)

### Captive Network Assistant

While the Captive Network Assistant is a super useful utility for those of us that frequent coffee shops and travel by train, for some we’ve received the request to be able to disable it. In the latest release, we’ve included a new gsetting key at `org.pantheon.capnet-assist enabled` to do just that. We’re still figuring out exactly how to integrate this setting into the Network section of System Settings, but in the meantime this key can be set directly with either DConf Editor or Terminal.

But if you make regular use of the Captive Network Assistant you’ll be happy to hear that it now handles new tabs properly as well as forwarding downloads to the browser. This is something we’ve seen from certain school’s wireless networks and we’re happy to say that this case is now supported.

### Calculator

While you were able to previously open multiple calculators, a quirky issue meant operations were copied across all calculator windows. This is now fixed and each calculator will operate independently.

### Terminal

Just a tiny change, password feedback is now enabled by default. So when you type your `sudo` password you’ll see asterisks instead of wondering if you’re typing anything at all ;)

### Look & Feel

Several icons received minor touch ups and new sizes, but the biggest change is related to app title bars. The default decoration style now matches modern Gtk3 apps using `Gtk.HeaderBar` instead of legacy Gtk2 apps. It feels more polished and more clearly delineates the title area from the rest of the window.

![](https://cdn-images-1.medium.com/max/600/1*caGfjgF7ihAx-nWJHwkhKg.png)
![Before and After, respectively](https://cdn-images-1.medium.com/max/600/1*UWjtICLAv7mLkdo7fUs0jQ.png)
Before and After, respectively

Other stylesheet fixes include fixes for borders in `Gtk.Assistant`, and a fix for title button pressed states in non-native and legacy apps.

### Bluetooth Indicator

We fixed an issue with the bluetooth indicator that made it fall out of sync with the state of the adapter. Now, the indicator should report the correct status of bluetooth when it’s changed from outside of the indicator.

### And More!

In addition to the updates mentioned above, several other components have received updated translations, stability fixes, and general code cleaning. Make sure to pop open AppCenter and hit “Update All” to get the latest and greatest.

_We’d like to say thanks again to our supporters on_ [_Bountysource_](https://salt.bountysource.com/teams/elementary) _and_ [_Patreon_](https://www.patreon.com/elementary)_, those who’ve purchased a copy of_ [_elementary OS_](https://elementary.io/) _or merch from_ [_our store_](https://elementary.io/store/)_. Every contribution helps make all of this possible, and we wouldn’t be here without you! If you’d like to help improve elementary OS, don’t hesitate to_ [_Get Involved_](https://elementary.io/get-involved)_!_