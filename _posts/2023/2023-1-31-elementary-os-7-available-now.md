---
title: elementary OS 7 Available Now
description:
author: danrabbit
image: /images/elementary-os-7-available-now/card.png
tags:
  - horus
  - release

hidden: 2023-01-31 17:00:00 UTC # 9 AM MST
---

It's been just over a year since we released elementary OS 6.1 Jólnir which brought new features and fixes based on your feedback, introduced new office productivity features, and expanded compatibility with a wide range of hardware. So far, OS 6.1 has been downloaded from our website [over 400,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-12-20&to=2023-01-31&props=%7B%22Version%22:%226.1%22%7D)—150,000 times more than 6.0—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page!

<figure class="constrained" markdown="1">
![elementary OS 7 Horus](/images/{{ page.slug }}/hero.png)
</figure>

Today we're proud to announce that OS 7, codenamed Horus, is available to download now and shipping on several high-quality computers. With OS 7, we've focused in on:

- Helping you get the apps you need
- Empowering you with new features and settings
- Evolving our developer platform and design guidelines

To get elementary OS 7 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

## Helping you get the apps you need

As always, AppCenter is the centerpiece of elementary OS. The primary purpose of any operating system is to support the apps that you use to work, play, and express yourself creatively. In the latest version of AppCenter we've worked on making app descriptions more engaging with more information, making it easier to update to the latest versions of apps, and improving support for sideloading and alt stores. We've also worked on improving AppCenter's responsiveness—making sure you can comfortable use it when tiling and on small displays as well as better using space on large displays.

<figure markdown="1">
![AppCenter at large and small sizes](/images/elementary-os-7-available-now/appcenter-responsive.png)
<figcaption markdown="1">
AppCenter can be used comfortably while tiled or on small displays
</figcaption>
</figure>

We've completely rewritten the way navigation works in AppCenter and now support two-finger swipe gestures to navigate back. The entire app loads much faster and provides more feedback when running background tasks via an overlay bar in the bottom right or left corner.

Recently updated apps are shown at the top of category views

### App Descriptions

The biggest change you'll notice when viewing app info pages is the improved emphasis on screenshots. Screenshot carousels now fill the width of the window, showing more screenshots at once. They can now also be accompanied by their own captions, which can help describe individual features as well as making pages more accessible to folks with vision-related disabilities. And finally each screenshot now sits on a card that uses the app's accent color, showing off more of the developer's personality.

<figure markdown="1">
![AppCenter's app info view](/images/elementary-os-7-available-now/appcenter-appinfo.png)
<figcaption markdown="1">
App Info views show more screenshots with captions and brand colors
</figcaption>
</figure>

Knowing how actively developed an app is and how engaged the developer is with their community is an important factor in decided which apps to install. We now help you know what to expect by showing an icon when an app uses an older, unsupported platform as well as showing up to 5 recent releases and their release notes instead of just the latest release. We also now show links to resolved tickets in an app's issue tracker per release, so you verify that app developers will take your feedback into consideration.

### Getting Updates

Staying up to date with the latest versions of apps is something we hear often is very important to folks using elementary OS. Flatpak makes it simple for developers to publish updates quickly and now you can get those updates automatically. If you'd still like to check for updates on your own time or want to force a manual refresh, there's now a handy menu option that you can use.

<figure markdown="1">
![AppCenter's  updates view](/images/elementary-os-7-available-now/appcenter-updates.png)
<figcaption markdown="1">
App Info views show more screenshots with captions and brand colors
</figcaption>
</figure>

### Sideloading & Alt Stores

Sideloading apps and using Alt Stores like Flathub is a major feature of elementary OS and a competitive edge over closed platforms that only let you install apps from a locked down store. In this release we've made several improvements to smooth out the experience of using Alt Stores based on your feedback and the latest cross-platform standards.

There's no longer a warning dialog every time you install an app that's supplied by an Alt Store, instead we show an unobtrusive icon alongside the app's other content warnings letting you know that elementary hasn't reviewed this particular app.

<figure markdown="1">
![AppCenter's app info view](/images/elementary-os-7-available-now/appcenter-sideload.png)
<figcaption markdown="1">
Even apps sideloaded from alt stores like Flathub can show brand colors
</figcaption>
</figure>

Apps from AppCenter could always use their own brand colors to make their app info pages feel unique and now apps sideloaded from Alt Stores can show brand colors too, thanks to the latest additions in the AppStream standard.

### Web Apps

In the theme of accessing the apps you need, we're shipping the very latest GNOME Web 43 which includes support for creating web apps which show in the applications menu. They can have their own settings including privacy controls and can even run in the background. Installed web apps can be managed from inside GNOME Web.

## Empowering you with new features and settings

### Feedback

[Feedback app screenshot]

The ability to send feedback directly to developers, see development happen transparently, and receive fixes and new features as updates quickly is one of our greatest strengths over both proprietary platforms and traditional Linux distributions. The Feedback app is a critical component in beginning this loop, so this cycle we've brought some major improvements to it including instant launch times, much better coverage of installed apps, settings, and desktop components, and you can now access the Feedback app directly from the applications menu. We've also improved keyboard navigation and responsiveness for small displays, and added the ability to quickly double click a list item to launch.

### Installation, Initial Setup & Onboarding

We've done a decent amount of work this cycle on reducing the number of screens in the Installer and providing more information to help you make informed decisions. For example, we now warn about connecting to power when on battery using an infobar instead of a separate page and we've introduced a combined "Before You Install" page that includes warnings about things like virtual machines, developer builds, and system requirements all in one step. And speaking of virtual machines, we've resolved issues that made the installer window too large to be interacted with on some virtual machines.

[Before You Install screenshot]

During Initial setup, we now detect if you use the right mouse button for clicking and offer to switch to a left-handed mouse button order. There's also a new view that will appear if your device doesn't have network access instructing you how to get connected.

[Screenshot of left-handed mouse dialog and network view]

Onboarding includes a new view for configuring automatic updates, as well as the addition of a "Sunset to Sunrise" option for the dark style.

<figure class="half" markdown="1">
![Choose Your Look view of Onboarding]/images/elementary-os-7-available-now/onboarding-styles.png){: width="497" height="406.5"}
![Night Light view of Onboarding]/images/elementary-os-7-available-now/onboarding-nightlight.png){: width="497" height="406.5"}
![Housekeeping view of Onboarding]/images/elementary-os-7-available-now/onboarding-housekeeping.png){: width="497" height="406.5"}
![Updates view of Onboarding]/images/elementary-os-7-available-now/onboarding-updates.png){: width="497" height="406.5"}
<figcaption markdown="1">
New features and settings are offered during onboarding like scheduled dark mode and automatic updates
</figcaption>
</figure>

### Office Productivity

Mail now sports a more-modern flatter design as a first-step towards work on making it more responsive. The unified inbox now supports Microsoft 365 accounts. And multiple potential crashes and freezes have been resolved.

[Mail Screenshot]

Tasks now has offline support for newly created task lists and it makes sure to synchronize your remote lists when the network becomes available again. Plus it now sends notifications when a task is due.

A long asked-for feature, you can now choose to select folders with a single click instead of activating them in Files, Windows style. Quite a bit of work has gone into making sure multiple click modes are supported and working as expected. We've also spent extra attention dialing in the behavior of keyboard shortcuts, especially regarding copy/paste and selection shortcuts across different view modes and with different types of file selections.

We're also shipping the latest Archive Manager and Document Viewer from GNOME 43. These releases improve support for dark mode, Flatpak portals like the native file chooser, as well as fix bugs and improve reliability.

## Multimedia

As music streaming services have emerged, there's been a shift away from the old paradigm of importing music from CDs, carefully curating playlists, and syncing music from your computer to mobile devices. We've received lots of feedback that Music wasn't meeting folks needs and the old code base was becoming prone to issues.

[Screenshot of Music 7]

This cycle we've completely rewritten Music from scratch with a much more focused design built around quickly queuing up and playing individual audio files or your local music collection. We've heard that the new design is better for folks who just need a fast way to preview audio files that they're using in their other projects, as well as for folks that still carefully curate their own local music collection and don't want to compete with an app for fine grained control of their library's organization scheme.

The new Music 7 already has better support for reading track metadata such as album art, works as you'd expect with system-wide media controls, and can be tiled and resized to fit small and large displays. We're excited to shape future versions of this app with your feedback, so make sure you let us know what kind of features you'd like to see!

Likewise, Videos now appears in the sound indicator alongside other media players.

### System Settings

We've now added support for offline firmware updates.

Central Kurdish is now available as an installable language and we now support installation and removal of languages with 3-letter codes.

Power profile management is now available in System Settings, including Performance mode for hardware that supports it. Expect much improved battery life for mobile devices with Power Saver mode. And you can now scroll both horizontally and vertically on the power indicator to change display brightness.

The redesign Multitasking settings includes the ability to set custom Terminal commands for each hotcorner.

Online accounts includes offline support for CalDAV accounts and the ability to choose a refresh rate for IMAP accounts.

Printer settings received special attention with several redesigns as well as new features like being able to clear the print queue per printer and a much clearer ink levels view.

Keyboard shortcut settings can now be easily disabled or reverted to their defaults and it's much easier to create and manage custom shortcuts. You can now also launch the Shortcuts app from the applications menu.

We've added the option to open and close the Multitasking view using the Super key.

A new security option allows you to forbid new USB devices from connecting while your device is locked.

We now show the correct information for WPA3 networks.

Support Rime input method for Chinese

In both System Settings and the Panel, we now use more information to assign accurate icons to audio devices.

### Performance

I want to make a special note here about performance. In just about every section I could have individually written about performance over and over again. The team has spent quite a bit of time tracking down slowdowns, reworking old code, and optimizing to make everything happen as quickly and responsively as possible and in the most extreme scenarios. I can't emphasize enough how big a part reducing latency plays in our vision for empowering you to do your best.

## Evolving our developer platform and design guidelines


### Iconography

New app icons

Additions:

"computer-fail"
"preferences-desktop-theme"
"application-x-sharedlib"
"process-paused"
caps-lock-symbolic
eye-not-looking-symbolic
eye-open-negative-filled-symbolic
num-lock-symbolic

Removals:

"office-address-book"
Flash file types
notification-*
Non-FDO network-*
Non-FDO app icons

Updated families:

Clean up "preferences-desktop-workspaces"
Update "preferences-desktop" to new tile shape
Update "image-missing" to new tile shape
Update "preferences-desktop-keyboard" to new tile shape
Update "document-import" and "document-export" to new tile shape
Update many file types with new arrow shape
"application-default-icon" is now brightly colored
"media-stop" is now a square
Round symbolic location status icons
Use an outlined shape for symbolic tag icons
Use a rounded star for symbolic bookmark icons
Redesign Night Light
Use latest Flatpak branding
Symbolic volume icons use a rounded shape and a slash when muted
Redesign media-playlist-repeat
Update media-playlist-shuffle and media-playlist-consecutive
Rounder square icons
Rounded arrow corners on Downloads folder
Deb and Flatpak Bundle files use a package metaphor
Updates arrow points up
Redesigned package with new colors

There's now also an Icon Browser app available in AppCenter where you can see all of the icons shipped with the elementary platform. You can search or view icons by category as well as see what sizes and styles an icon comes in and even get a quick code snippet to use in your app.

[Icon Browser screenshot]

### Gtk 4

Sideload
Shortcuts
Music
Onboarding

### Granite

The latest version of our app framework Granite as well as our system stylesheet have been updated to support Gtk 4 and come with a host of new features and API changes to make building apps quick and straightforward.

In Gtk 4, style class constants have moved from Gtk itself into the platform frameworks. This means that all of the supported style class constants in the elementary stylesheet are now provided by Granite. This includes classes you're familiar with like the ones for setting text colors as well as the ones for setting background colors on sidebars or in views, plus some new ones like `RICH_LIST` for setting up padding and margins on listboxes.

A new Granite.Placeholder widget was introduced to replace AlertView and Welcome with a single more flexible widget. It supports all the usual cases like welcome screens with buttons, embedded alerts, and placeholders for lists. It supports markup in descriptions and you can even uses style classes like `ACCENT`, `WARNING`, or `ERROR` to automatically color title text.

Plus, widgets have been reworked to set all of their margins and padding from Gtk.CSS—meaning they scale appropriately with the system text size—and several widgets have been made more responsive for large and small displays.

Every release comes with removals and this migration to Gtk 4 comes with quite a few of them. We're excited to remove several utilities that are better supported in Gtk and GLib upstream, including the Settings class, Logging, Command Launching, several drawing functions now covered by Gtk.CSS, DynamicNotebook since you can now get a great tab bar widget from Adwaita, and others. In each case we looked at existing apps and made sure they could migrate to Gtk 4 without losing functionality and in many cases their code was made more robust and more simple by using functions provided by upstream libraries.

As always, the full API reference for Granite is available [on Valadoc.org](https://valadoc.org/granite-7/Granite.html).

### Flatpak Platform
7.1.0

### Tools

Code

Hidden folders are now shown in the project sidebar
The currently selected result and the number of results is displayed while searching
The search bar now has a regular expression mode

It is now possible to change Git branch with untracked files present in a project
Line duplication is now actioned correctly if there is no selection present


Terminal gains the ability to both follow the system dark style preference as well as create custom color palettes. The new default light and dark styles are now fully opaque and have been updated to match the latest upstream values from the Solarized themes for improved legibility. We've also added the keyboard shortcut <kbd>Alt</kbd> + <kbd>1—9</kbd> for switching tabs and you can quit Terminal with <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Q</kbd>

## Special Thanks

There are tons of other small improvements, bug fixes, and more that didn't make it into this release blog post. I'd like to give a special thanks to our volunteer community for their continual commitment to making a great open source operating system. I'd also like to particularly call out our localization team that works hard to make every release available in dozens of languages, including right-to-left languages, Asian character languages, and more. This release also wouldn't have been possible without the work of developers running Pantheon on other distros like Fedora and NixOS and their participation upstream. And speaking of upstreams, I'm always grateful for the work that goes into the Ubuntu releases that we build upon. I'm very proud of what a diverse community can build together and this release is definitely something to be proud of. Thank you all so much for being a part of it!

---

## Get elementary OS 7

elementary OS 7 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 7 FAQ](https://github.com/elementary/os/wiki/elementary-OS-7-FAQ){: .button.flat }
[Download elementary OS 7][elementary.io]{: .button.suggested }
</div>

### Devices

Our hardware retailers [Laptop with Linux], [Slimbook], and [Star Labs] are all offering elementary OS 7 out of the box starting today. Visit retailers' individual sites for more information.

<div style="text-align: center" markdown="1">
[Shop Devices][store]{: .button }
</div>

[elementary.io]: https://elementary.io
[Laptop with Linux]: https://laptopwithlinux.com/?ref=36&utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Slimbook]: https://slimbook.es/?utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Star Labs]: https://starlabs.systems/?rfsn=4227837.e8f025
[store]: https://store.elementary.io/
