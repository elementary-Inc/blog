---
title: Loki Updates for May
description: 'You thought we’d skip this month due to the big Loki release, didn’t you?'
date: '2017-05-30T16:20:23.586Z'
categories: []
keywords: []
slug: /@DanielFore/loki-updates-for-may-1b44b4e942e3
---

If you’ve recently installed [Loki 0.4.1](https://medium.com/elementaryos/new-release-elementary-os-loki-0-4-1-2a756549ee76) you may not have noticed that some of these things are new. But for those upgrading from Loki 0.4.0 here’s a list of updates for the month of May.

### Look & Feel

![](https://cdn-images-1.medium.com/max/800/1*L297dOpf0QWIC7-JWxvClQ.png)

You may have noticed new battery icons in the panel, but you may not have noticed [several other icon changes](https://github.com/elementary/icons/compare/996c760...b952151) like a refined Terminal icon, new USB key icons, non-generic icons for meson build files and CSV files, and more.

### AppCenter

![More specific error messages in the payments dialog](https://cdn-images-1.medium.com/max/800/1*sZ0nHl3iR27B_voyTcNZEw.png)
More specific error messages in the payments dialog

There are now more detailed error messages when payments fail; you’ll be told if the error occurred because of incorrect payment info, processing issues, or if something else went wrong like your bank blocking the payment.

We also received several reports about the “date” field in AppCenter payment dialogs. It now accepts dates formatted as either `MM/YY` or `MMYY`.

### Panel

![](https://cdn-images-1.medium.com/max/800/1*swpZIIhnyuU0fBfwjY9sSQ.png)

A long requested feature fulfilled! The power indicator now includes a brightness slider.

The applications menu received performance improvements along with the ability to start an AppCenter search.

The notifications indicator will no longer save notifications marked by apps as “transient”. Also, when apps request to withdraw a notification they will now be removed from the indicator. Thanks to your reports, we’ve tracked down and fixed several possible crashes when apps send bad info with their notifications.

We’ve also improved stability of the Ayatana Indicator compatibility layer.

### Bits and Bobs

Fixed [an issue](https://github.com/elementary/pantheon-agent-polkit/pull/11) where hitting the `esc` key in authentication dialogs didn’t actually cancel the authentication action. Fixed [an issue](https://github.com/elementary/switchboard-plug-locale/issues/21) where Language & Region settings was empty when first run. User Accounts settings now sends a toast for undo.

Our development library Granite was updated to version 0.4.1 and received [its own blog post](https://medium.com/elementaryos/making-granite-a-better-library-8b925859e9fb), so make sure to check that out.

In addition to the updates mentioned above, you can always rely on updated translations, stability fixes, and general code cleaning. Make sure to pop open AppCenter and hit “Update All” to get the latest and greatest.

_We’d like to say thanks again to our supporters on_ [_Bountysource_](https://salt.bountysource.com/teams/elementary) _and_ [_Patreon_](https://www.patreon.com/elementary)_, those who’ve purchased a copy of_ [_elementary OS_](https://elementary.io/)_, merch from_ [_our store_](https://elementary.io/store/)_, or apps in AppCenter. Every contribution helps make all of this possible, and we wouldn’t be here without you! If you’d like to help improve elementary OS, don’t hesitate to_ [_Get Involved_](https://elementary.io/get-involved)_!_