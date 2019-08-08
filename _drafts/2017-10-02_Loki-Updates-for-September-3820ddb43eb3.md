---
title: Loki Updates for September
description: Celebrating a year of elementary OS 0.4
date: '2017-10-02T18:38:28.053Z'
categories: []
keywords: []
slug: /@DanielFore/loki-updates-for-september-3820ddb43eb3
---

This month marks a full year of elementary OS 0.4 Loki. If you’d like a bit of a throwback, check out [our release blog post on Tumblr](http://blog.elementary.io/post/147637979911/loki-04-stable-release). Loki brought a brand new set of indicators in the panel (including the notifications indicator), many refreshed or redesigned settings panes, parental controls and DLNA sharing, and new features across all of our apps.

![Loki, day 1](https://cdn-images-1.medium.com/max/1200/1*gBHrZtd_uIshaztegrv2pQ.png)
Loki, day 1

8 months later, in May, we released [a major update](https://medium.com/elementaryos/new-release-elementary-os-loki-0-4-1-2a756549ee76) that included new, curated apps powered by AppCenter Dashboard, a new hardware enablement stack, and plenty of other feature updates.

![AppCenter in the 0.4.1 update](https://cdn-images-1.medium.com/max/1200/1*Z2Pv6bIY5-_wFhYLvNp1ug.png)
AppCenter in the 0.4.1 update

We’ve made it a point to regularly push updates to Loki and this month is no exception! Here is the Loki updates roundup for September:

### Networking

You may have noticed a rather big change to the way we display password protected and open networks in the menu. Following up on Cassidy’s “[Secure by Default](https://medium.com/elementaryos/secure-by-default-689abcac6c66)” post, we now show a slashed lock icon next to open access points instead of a lock icon next to password protected access points. You’ll also notice a new tooltip when hovering the name of an access point that will display more information about the security level of the access point.

![New network indicator with a secure-by-default UX](https://cdn-images-1.medium.com/max/800/1*_KCjbWrnSOukTtlogphzIQ.png)
New network indicator with a secure-by-default UX

The icon in the panel should now always prioritize active network connections. Configured VPNs will now show in the menu. An issue was resolved that caused duplicated menu separators at the greeter screen.

The network settings page gets a little smarter this month and now ignores network interfaces from virtual machines and containers like Docker. We also resolved an issue that prevented SOCKS proxies from working properly and added an explantion for the HotSpot feature.

### AppCenter

It wouldn’t be a Loki updates post without new features and fixes for AppCenter! This update brings the much requested feature to show release descriptions (i.e. changelogs) in both the updates view and the app info page. For the time being, release descriptions are optional for developers to provide but you may notice your favorite apps using them already.

![](https://cdn-images-1.medium.com/max/600/1*cmQGtURvk03aGFkkTT-lkA.png)
![Example of release descriptions in AppCenter. They display at the bottom of an app’s info page and in the Updates view in an expander.](https://cdn-images-1.medium.com/max/600/1*gGsXsUB8xiLY51De6E--wA.png)
Example of release descriptions in AppCenter. They display at the bottom of an app’s info page and in the Updates view in an expander.

We also resolved an issue that caused the badge in the dock to get out of sync with the amount of available updates, made some memory usage optimizations in list views, and squashed a couple of other minor bugs.

### And More!

Badges in the applications menu are now drawn with a Gtk widget instead of directly with Cairo Code, fixing their appearance for HiDPI users. We fixed an issue for apps which refer to their icon using absolute path; they now appear correctly. You can now also switch between indicators in the panel using the keyboard shortcut `Ctrl + Tab`

In addition to the updates mentioned above, you can always rely on updated translations, stability and performance fixes, and general code cleaning. Make sure to pop open AppCenter and hit “Update All” to get the latest and greatest. While you’re at it, be sure to check out some of the new apps that were published this month!

_We’d like to say thanks again to everyone who’s bought an app on AppCenter, our supporters on_ [_Bountysource_](https://salt.bountysource.com/teams/elementary) _and_ [_Patreon_](https://www.patreon.com/elementary)_, and those who’ve purchased a copy of_ [_elementary OS_](https://elementary.io/) _or merch from_ [_our store_](https://elementary.io/store/)_. Every contribution helps make all of this possible, and we wouldn’t be here without you! If you’d like to help improve elementary OS, don’t hesitate to_ [_Get Involved_](https://elementary.io/get-involved)_!_