---
title: elementary OS 7 Available Now
description:
author: danrabbit
image: /images/elementary-os-7-available-now/card.png
tags:
  - horus
  - release
---

12/20/21 was release date of OS 6.1

It's been just over a year since we released elementary OS 6.1 Jólnir which brought new features and fixes based on your feedback, introduced new office productivity features, and expanded compatibility with a wide range of hardware. So far, OS 6.1 has been downloaded from our website [over 390,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-12-20&to=2022-12-05&props=%7B%22Version%22:%226.1%22%7D), over 100,000 times more than 6.0—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page!

<figure class="constrained" markdown="1">
![elementary OS 7 Horus](/images/{{ page.slug }}/hero.png)
</figure>

Today we're proud to announce that OS 7, codenamed Horus, is available to download now and shipping on several high-quality computers. With OS 7, we've focused in on:

- Helping you get the apps you need
- Empowering you with new features and settings
-


To get elementary OS 7 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

## Helping you get the apps you need

As always, AppCenter is the centerpiece of elementary OS. The primary purpose of any operating system is to support the apps that you use to work, play, and express yourself creatively. In the latest version of AppCenter we've worked on making app descriptions more engaging with more information, making it easier to update to the latest versions of apps, and improving support for sideloading and alt stores. We've also worked on improving AppCenter's responsiveness—making sure you can comfortable use it when tiling and on small displays as well as better using space on large displays.

[Screenshots]

We've completely rewritten the way navigation works in AppCenter and now support two-finger swipe gestures to navigate back. The entire app loads much faster and provides more feedback when running background tasks via an overlay bar in the bottom right or left corner.

Recently updated apps are shown at the top of category views

### App Descriptions

The biggest change you'll notice when viewing app info pages is the improved emphasis on screenshots. Screenshot carousels now fill the width of the window, showing more screenshots at once. They can now also be accompanied by their own captions, which can help describe individual features as well as making pages more accessible to folks with vision-related disabilities. And finally each screenshot now sits on a card that uses the app's accent color, showing off more of the developer's personality.

[Screenshot of app info page]

Knowing how actively developed an app is and how engaged the developer is with their community is an important factor in decided which apps to install. We now help you know what to expect by showing an icon when an app uses an older, unsupported platform as well as showing up to 5 recent releases and their release notes instead of just the latest release. We also now show links to resolved tickets in an app's issue tracker per release, so you verify that app developers will take your feedback into consideration.

### Getting Updates

Staying up to date with the latest versions of apps is something we hear often is very important to folks using elementary OS. Flatpak makes it simple for developers to publish updates quickly and now you can get those updates automatically. If you'd still like to check for updates on your own time or want to force a manual refresh, there's now a handy menu option that you can use.

[Screenshot of updates page]

### Sideloading & Alt Stores

Sideloading apps and using Alt Stores like Flathub is a major feature of elementary OS and a competitive edge over closed platforms that only let you install apps from a locked down store. In this release we've made several improvements to smooth out the experience of using Alt Stores based on your feedback and the latest cross-platform standards.

There's no longer a warning dialog every time you install an app that's supplied by an Alt Store, instead we show an unobtrusive icon alongside the app's other content warnings letting you know that elementary hasn't reviewed this particular app.

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

[Screenshot of Automatic Updates view and Style view]

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







## Look & Feel

New default wallpaper
New app icons






## Developer Platform

### Icon Browser
A modern redesign!

Fancy new icon
Drag the window from anywhere
Follow the system dark style preference
Updated for Gtk 4

### Code

The current document filename is now shown as the window title in multitasking view
Hidden folders are now shown in the project sidebar
The currently selected result and the number of results is displayed while searching
The search bar now has a regular expression mode
Fixes:

It is now possible to change Git branch with untracked files present in a project
Crashes are prevented while searching in large projects
The correct document is now focused after opening Code from an external program
Line duplication is now actioned correctly if there is no selection present
Code no longer crashes when asked to open an unknown URI format

### Terminal

Option to follow system dark style preference
Create a custom color palette

Default styles are fully opaque and updated to the latest upstream values from Solarized for improved legibility
New features:

Switch tabs with Alt + 1-9
Quit with Ctrl + Shift + Q


### icons
Additions:

"computer-fail"
"preferences-desktop-theme"
"application-x-sharedlib"
"process-paused"
Removals:

"office-address-book"
Flash file types
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
Other Changes:

Fix broken link for SVG file types
Fix missing links for PGP file types
Scale some icons to more sizes

Additions:

caps-lock-symbolic
eye-not-looking-symbolic
eye-open-negative-filled-symbolic
num-lock-symbolic
Updated families:

Redesign media-playlist-repeat
Update media-playlist-shuffle and media-playlist-consecutive
Rounder square icons
Rounded arrow corners on Downloads folder
Deb and Flatpak Bundle files use a package metaphor
Updates arrow points up
Redesigned package with new colors
Removals:

notification-*
Non-FDO network-*
Non-FDO app icons

### stylesheet
Improvements:

Checkerboard styles are more subtle
Set `large-icons` size on headerbars to 24px
Adjust header layout and typography in Granite.SimpleSettingsPage
Infobars: set correct button margins
Add padding to Gtk.Entry's completion popover
Fix labels for scale marks
Fixes:

Correct .title-4 padding in Lists
Buttons: don't set font weight for children like popovers
New Features:

Support for Gtk4
Fixes:

Fix titlebar in GNOME Web 42
Fix font style for bold labels in some languages
ModelButtons: add margin between checks, radios, and labels

### granite
New Features:

Granite.STYLE_CLASS_RICH_LIST for standard Gtk.ListBox row padding
Granite.STYLE_CLASS_FRAME for adding a border to Gtk.LisBox, Gtk.InfoBar, and others
Granite.STYLE_CLASS_SIDEBAR for styling application sidebars
Granite.STYLE_CLASS_BACKGROUND to use the default background color for a widget
Add optional secondary text to Granite.HeaderLabel
Improvements:

Allow text in Granite.Toast to wrap
SimpleSettingsPage: Wrap titles and allow description text to go under switches
Updated translations
New Features:

Ported to GTK4! tada
Granite.Placeholder: replaces AlertView and Welcome
SimpleSettingsPage: Allow markup in description
Removals:

Application: use Gtk.Application instead
Drawing: Use Gtk.CSS
DynamicNotebook: use Adw.TabBar instead
Logger: use GLib.log instead
ModeButton: Use Gtk.ToggleButton with the "group" property and "linked" style class instead
Paths: use GLib.Environment instead
Seekbar
Services.Settings: use GLib.Settings instead
SimpleCommand: use GLib.AppInfo.create_from_commandline instead
SourceList: use Gtk.ListBox with the "sidebar" style class instead
StorageBar
TextStyle: use style class constants instead
Several functions in System were replaced by GLib.AppInfo

### flatpak-platform
7.1.0

### Gtk 4

Sideload
Shortcuts
Music
Onboarding

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
