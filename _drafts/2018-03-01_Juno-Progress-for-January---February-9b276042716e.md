---
title: Juno Progress for January & February
description: A sneak peek at changes coming this year
date: '2018-03-01T19:57:41.408Z'
categories: []
keywords: []
slug: /@DanielFore/juno-progress-for-january-february-9b276042716e
---

As you may know, elementary operates on a task-based rather than time-based system for releases. This means before we can release [Juno](https://medium.com/elementaryos/lets-talk-about-elementary-os-5-0-juno-a3a65b97ee7e), there’s a lot of work to do! So far, there are a little over [350 closed issue reports](https://github.com/issues?q=is%3Aissue+user%3Aelementary+milestone%3Ajuno-beta1+is%3Aclosed) associated with the first Juno beta. Here are some highlights of the things you’ll see in the next version of elementary OS:

### Panel, Applications Menu, & Indicators

The panel has received a lot of love for Juno. The most immediately-obvious improvement is the addition of a search icon to the Applications menu. This helps inform users what they can expect behind that item, plus it helps balance the left side of the panel out a bit better with the right. We’ve also added a tooltip of “Open and search apps (⌘ + Space)” to provide even more feedback if the user hovers over it for a moment (signaling they’re unsure). It also gives a bit of progressive disclosure of keyboard shortcuts, helping teach users even faster ways to do things.

![](https://cdn-images-1.medium.com/max/800/1*bQYs-HNXSHejeL95sgRxrQ@2x.png)

Something you’ll notice with certain wallpapers is a new translucent light mode. Previously, the panel had four states: transparent dark, transparent light, translucent, and maximized. In Juno, we’re splitting translucent out into translucent dark and translucent light.

![](https://cdn-images-1.medium.com/max/600/1*LjHMtWfruGVCrZRd2-0w6w@2x.png)
![Transparent Dark (on a dark wallpaper) and Transparent Light (on a light wallpaper)](https://cdn-images-1.medium.com/max/600/1*_MlM4Hh-0pKu-LhB1d0-2Q@2x.png)
Transparent Dark (on a dark wallpaper) and Transparent Light (on a light wallpaper)

If the top of your wallpaper is busy (high variations in contrast), the panel draws a translucent background. Now in Juno, the panel will detect if it’s drawing on a mostly light or mostly dark area, and shades the panel and foreground appropriately. The result is a panel that more closely respects the user’s preference for a light or dark desktop.

![](https://cdn-images-1.medium.com/max/600/1*MCO2lXwO2RTHt6pX39752A@2x.png)
![Translucent Dark (on a busy dark wallpaper) and the new Translucent Light (on a busy light wallpaper)](https://cdn-images-1.medium.com/max/600/1*a-g9Td8nJScQgkz5IKpFVA@2x.png)
Translucent Dark (on a busy dark wallpaper) and the new Translucent Light (on a busy light wallpaper)

When an app is maximized or tiled, we still go into the full-black maximized state to put the focus on the app and let the panel blend into the bezel.

![Maximized](https://cdn-images-1.medium.com/max/800/1*zQE3P0fG1H5vCM9GfFxU0g@2x.png)
Maximized

We’ve also improved the system indicators. Several icons are now animated between states; for example, the bell in the notifications indicator “rings” when you get a new notification, and it animates the slashing-out when put into Do Not Disturb mode.

![Some panel icons now come with animations](https://cdn-images-1.medium.com/max/800/1*UnVjdm6PKwdEuNiKrILRRw.gif)
Some panel icons now come with animations

The Applications menu now only scrolls one page per trackpad swipe, making for a better experience on laptops.

The power indicator — which shows battery level, brightness controls, and apps using lots of power — also got a couple new features. We now display the correct total percentage when your device has multiple internal batteries, and middle-clicking the icon toggles showing the battery percentage.

### System Settings

While working on the new Installer and Initial Setup we spent some time iterating through creating user accounts. This work is also reflected in System Settings where we now do a much better job of providing useful feedback about invalid input and encouragement to create strong passwords.

![](https://cdn-images-1.medium.com/max/600/1*674CXyxAt0cFpy4A7LmIfw.png)
![Left: Invalid inputs; Right: valid inputs](https://cdn-images-1.medium.com/max/600/1*5Ai8bKKEWScyZ1KoqT5-9w.png)
Left: Invalid inputs; Right: valid inputs

Currently in Loki, we rely on an Ubuntu-specific script to guess if the device we’re running on is a laptop, then show Power options based on that guess. In Juno, we now detect individual hardware components in a distro-agnostic way which allows us to show relevant power settings for more form factors.

In Mouse & Touchpad settings there are two new options: the ability to disable middle-click paste, and (if a touchpad is present) the ability to enable the touchpad even while typing, something very useful for gamers.

In Desktop settings, you can now hover over a wallpaper image to see the name of the Artist for each image. We get our wallpapers from [Unsplash](https://unsplash.com/) and now you can easily find more images from artists whose work you enjoy.

Keyboard settings have also received quite a bit of attention for Juno. On the Shortcuts tab, we’ve added shortcut settings for cycling workspaces (⌘ + Tab by default) and Zoom In and Out (⌘ + and ⌘ - by default), we now show “Ctrl”, “Tab”, and “Shift” keys as text instead of using symbols, and each category has a nice icon. On the Layout tab, we’ve backported some of the language selection work we’ve done in [the new Installer](https://medium.com/elementaryos/meet-the-upcoming-installer-a499341218f5) for finding and previewing keyboard layouts.

![](https://cdn-images-1.medium.com/max/600/1*3k8HH23TZPhdQkkXw6VJ0Q.png)
![The new popover for keyboard layout selection](https://cdn-images-1.medium.com/max/600/1*OPGX23pdbWmNyQVKdkTwEg.png)
The new popover for keyboard layout selection

We’ve also added a Rotation Lock setting in Displays and we’re working on a brand new Sound page.

### Music

As one of our longest-developed apps, Music has been the target of insane amounts of code clean up this cycle. We’ve replaced many of its old custom widgets with their Granite counterparts like using the same Granite StorageBar used in Files for devices in Music. We’ve fixed some long-standing issues like loading embedded album cover art, and there are still plenty of large refinements to come.

![New album placeholder art and the new album sidebar](https://cdn-images-1.medium.com/max/1200/1*AtwQqHBvVrhC42wiN8Zw5Q.png)
New album placeholder art and the new album sidebar

You’ll also notice that there’s been some design work happening here: there is no longer a statusbar across the full bottom of the app, albums appear in a new sidebar, and shuffle and repeat options have moved to the headerbar. You may also notice crisp new album placeholder art.

### Photos

We’ve been doing a lot of cleanup and refinement in Photos for Juno. The most immediately obvious update is that Photos now sports a dark style in both the viewer and library modes, putting a stronger focus on your photos.

![New dark style for the library](https://cdn-images-1.medium.com/max/1200/1*5SrfyE5fMqn-dBP8dS0qFg@2x.png)
New dark style for the library

We’ve also added full HiDPI support for both thumbnails and single photo views, meaning your shots will look as crisp as possible, no matter your display density.

In fullscreen mode, we’ve reworked the toolbar and improved its hide behavior: it now hides automatically and unhides on mouse move.

### Terminal

Our Terminal is getting even better in Juno with new options for text scale and three built-in color schemes: High Contrast, Solarized Light, and Solarized Dark.

![](https://cdn-images-1.medium.com/max/400/1*8R4mud5OEOUvsreyMaH4fQ.png)
![](https://cdn-images-1.medium.com/max/400/1*QJrAAkUNUGXlJ7Ot2NAxMg.png)
![New color schemes for Terminal](https://cdn-images-1.medium.com/max/400/1*Ip-UWv6eWh1wZ3ZeGZyxhg.png)
New color schemes for Terminal

You’ll also notice that the tab icon for exited processes now shows a red exclamation when the exit status is `>0`. What we can’t show in these screenshots is that we also correctly restore tab order and the active tab when Terminal is closed.

### Night Light

This frequently asked for feature will make its debut in Juno! There’s a new Night Light tab under the Displays settings to let you turn the feature on, set its schedule, and adjust the color temperature.

![](https://cdn-images-1.medium.com/max/1200/1*wlc7BPNTrTE5vHUuRvO9bA@2x.png)

We’ve also added a handy indicator that shows up during the scheduled time. It lets you temporarily snooze it (until the next scheduled time), adjust the temperature on the fly, and quickly dive into the aforementioned settings.

![](https://cdn-images-1.medium.com/max/1200/1*0lQz38e0MJC5vFPAm04pUA@2x.png)

### And More

CapnetAssist — our helper for captive networks that you find in airports, coffee shops, etc. — now uses portal detection from Network Manager. This means you can now configure your captive portal server if you want to use something other than the default. The captive portal window also now saves its window size between sessions.

Various shell features like notifications and the Alt+Tab window switcher now respect HiDPI, bringing us even closer to true full HiDPI support.

Both the network indicator in the panel and the network pane in System Settings now support mobile broadband devices.

### And There’s Still More!

Juno is still under active development and we’re expecting to land even more features, fixes, optimizations, etc. before its big debut. Stay tuned to this blog for more highlights and announcements as we move toward the next major version of elementary OS. If you missed it, be sure to check out our [previous post about Juno](https://medium.com/elementaryos/lets-talk-about-elementary-os-5-0-juno-a3a65b97ee7e).

_Thank you to everyone who’s bought an app on AppCenter, our supporters on_ [_Bountysource_](https://salt.bountysource.com/teams/elementary) _and_ [_Patreon_](https://www.patreon.com/elementary)_, and those who’ve purchased a copy of_ [_elementary OS_](https://elementary.io/) _or merch from_ [_our store_](https://elementary.io/store/)_. Every contribution helps make all of this possible, and we wouldn’t be here without you! If you’d like to help improve elementary OS, don’t hesitate to_ [_Get Involved_](https://elementary.io/get-involved)_!_

_Portions of this piece authored by_ [_Cassidy James Blaede_](https://medium.com/u/d1d97e2b0d79)_._