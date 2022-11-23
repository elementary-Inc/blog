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

It's been just under a year since we released elementary OS 6.1 Jólnir which brought new features and fixes based on your feedback, introduced new office productivity features, and expanded compatibility with a wide range of hardware. So far, OS 6.1 has been downloaded from our website [over 360,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-12-20&to=2022-11-02&props=%7B%22Version%22:%226.1%22%7D), over 100,000 times more than 6.0—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page!

<figure class="constrained" markdown="1">
![elementary OS 7 Horus](/images/{{ page.slug }}/hero.png)
</figure>

Today we're proud to announce that OS 7, codenamed Horus, is available to download now and shipping on several high-quality computers. With OS 7, we've focused in on:

-
-
-


To get elementary OS 7 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

## AppCenter

As always, AppCenter is the centerpiece of elementary OS. The primary purpose of any operating system is to support the apps that you use to work, play, and express yourself creatively.
- More engaging app descriptions with more information
- Easier to update to the latest versions
- Better support for sideloading and alt stores

Responsive design work:
- Wrap links at the bottom pages instead of ellipsize

Rewritten navigation with multitouch gestures to go back
Recently updated apps are shown at the top of category views
A status overlay bar is now shown when tasks are in progress
Redesigned "Fun & Games" category card

Performance & Stability improvements

Show "Try for Free" when setting an app's price to 0

### App Descriptions

Screenshot carousels fill the width of the window, showing more screenshots at once
An app's accent color is now shown behind screenshots

Better dark style support
Warn when apps are built against older runtimes
Show screenshot captions in a tooltip
Up to 5 releases shown
Support for Issues tag

### Getting Updates

Added an option to automatically update apps
Manually check for new updates

Release notes are shown in a dialog
Better fallback icons for components
The "Update All" header now sticks to the top of the window when scrolling

### Sideloading & Alt Stores

Don't show a warning dialog about apps from alt stores
Get brand colors from the AppStream standard so more apps are supported

Sideload

Use updated Flatpak branding
Badge notifications with the sideloaded app's icon
Gtk4

## Other Apps

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


### Calculator

Gtk 4

### Music

Complete rewrite
Gtk4

### Photos

New actions to copy image or metadata to clipboard
Photos taken on the same day show under the same event
Replace all instances of "Shotwell" with "Photos"
Avoid a crash when importing videos
Redesigned Icon

### Calendar

Updated app icon

Ask for confirmation before deleting events
Follow email and web links in the event description with Control + Click

Disabled checkbox "Mark as default calendar" in calendar settings, if the calendar is read-only
Removed no longer needed sandbox permission for accounts service
Fixed potential memory leak

### Mail

Fixed an error which caused mail accounts to be loaded multiple times
Fixed a bug which caused Mail to crash occasionally
Display recipient in Sent folder instead of sender

Updated app icon
New design

Use message subject for composer window title
Added support for Unified Inbox for Microsoft 365 accounts


Fixed an error which caused the inbox monitoring in the background to crash
Removed duplicate sender addresses when composing a message
Fix a freeze when archiving the last message in a folder

Renamed Office 365 to Microsoft 365 to follow suite on Microsoft's rebranding


### Feedback

Avoid focus stealing prevention when opening a web browser
Show more entries under Desktop Components

### Videos

Fix a crash with certain video codecs

### Tasks

New app icon
Add offline support for newly created task lists in case its configured for the account
Automatically synchronize a task list whenever it is selected or the network becomes available again
Send a notification when a task is due

### Files

Improvements:

Provide option to select folders with single click and activate with double click
Only show the properties overlay when files are selected, not when hovered
Fixes:

Fix unexpected file activation after navigation with double-click
Fix dimmed window after use of filechooser portal
Fix possible crash when rapidly changing view modes
Fix startup when restored remote location is no longer connected
Ensure infobar shows in connection server dialog when connection attempt fails
Ensure correct icon for bookmark to a file that is not a folder
Fix possible crash when removing a bookmark
Renaming with the same name no longer shows an error dialog
Ctrl + A when renaming now selects all the text in the entry
Selecting multiple items with Shift + Arrow keys now works properly
The appearance of the cursor now matches the action
The Trash sidebar item can no longer be removed
Network sidebar plugins such as NextCloud are now added correctly
Duplication of subfolders in ListView under some circumstances is fixed
Bookmarks are now highlighted when a file they can accept is dragged onto them
Folders not being restored properly under some circumstances is fixed
Show confirmation dialog in file chooser before overwriting an existing file
Ctrl + V now always pastes into background folder
Shift + Ctrl + V now pastes into selected folder if there is one
Show New Tab and New Window shortcuts in context menus

Double click selects instead of exiting while renaming in list view
Show public share icon in breadcrumbs
Prevent a crash when dragging to re-arrange bookmarks

### Camera

Support MJPEG cameras
Fixes:

Show error in case no camera device is available
New features:

Take a photo or video on secondary-click
Fixes:

Ensure brightness, contrast, and mirror continue working after taking a photo
Wider hardware compatibility (e.g. StarBook Mk V)
Ensure photos saved properly

### Terminal

New features:

Option to follow system dark style preference
Create a custom color palette
Fixes:

Default styles are fully opaque and updated to the latest upstream values from Solarized for improved legibility
New features:

Switch tabs with Alt + 1-9
Quit with Ctrl + Shift + Q

## The Desktop

### Gala
Use access portal for force quit
Properly update accent color in the window switcher
Fix selecting windows underneath the window switcher
Prevent potential crashes
Resize workspaces when displays change
Handle windows with no title
Improvements:

Use access portal for display settings confirmation and force quit
Allow closing multitasking view with Super

### settings-daemon
Add left handed setting (#44)
Check downloads folder isn't home folder (#50)


### shortcut-overlay
Show in the applications menu
Replace keyboard settings button with a labeled link button
Show on-screen keyboard shortcut
Close with the shortcut Ctrl + Q
Updated translations
Gtk 4

### notifications
Fix missing icon when set from icon name

### Portals
Add a destructive action option for access portals
Fixes:

Fix a crash when opening apps in the AppChooser portal
Fix window focus and position for Access portals with no parent window
Set AppChooser portal as a modal dialog for proper animations

### Installation & Onboarding

### initial-setup
Offer to switch to left-handed setup if right clicking
Check for network access

### onboarding
Add Automatic Updates view
Add Sunset to Sunrise to Style View
Update for OS 7 and Gtk 4
Updated translations

### System Settings


### switchboard-plug-about
Added support for dark style manufacturer logos
Added support for offline firmware updates

### switchboard-plug-locale

Central Kurdish is now available as an installable language
Support installation and removal of languages with 3-letter codes

### switchboard-plug-power
 Add power profile management
 
### switchboard-plug-pantheon-shell
There is now an undo option after removing a wallpaper
Wallpapers are now sorted with custom wallpapers first
Fixes:

Wallpaper accent color follows system setting
Set-wallpaper contract fails gracefully when run as sudo
Wallpapers with the same name are distinguished
Switching styles with the keyboard cancels dark style scheduling
Style dyslexia-friendly switch properly
Set custom Terminal commands for each hotcorner
Redesigned Appearance and Multitasking views

### switchboard-plug-onlineaccounts
Added offline support for CalDAV accounts
Choose refresh rate for IMAP

### switchboard-plug-printers
Allow clearing the queue for each printer
Improvements:

Improved job row layout
Show the supported language for each driver
Show color names below ink levels
Avoid expanding the window for printers with many ink levels
Use newer add/remove list pattern
Fixes:

Update sidebar after adding or removing printer
Update sidebar after enabling or disabling printer
Update job list after job state change

### switchboard-plug-network
Show correct info for WPA3 networks
Fix an issue with wired connections repeatedly reconnecting

### switchboard-plug-keyboard
Revert shortcuts to default
Easily disable a shortcut
Support Rime input method for Chinese
Minor updates:

Remove custom shortcuts from their menu
Open Multitasking View with Super

### switchboard-plug-security-privacy
Option to forbid new USB devices while locked

### switchboard-plug-sound
Use device form factor when available to assign more accurate icons
Provide a fallback device icon in case none is available
More helpful placeholder text when no input devices are found

### The Panel

### wingpanel-indicator-notifications
Clear All button no longer leaves undeletable notifications
Reduce delay in initially showing wingpanel when there is a large number of notifications
Reduce delay in clearing all notifications when there is a large number of notifications

### wingpanel-indicator-network
Ensure correct tooltip on system start
Prevent connecting to invalid VPNs
Show correct info for WPA3 networks

### wingpanel-indicator-power
Scroll horizontally on the panel icon to change display brightness
Minor updates:

Do a better job hiding the brightness slider on unsupported displays
Updated translations
Clicking the "Apps Using Lots of Power" header label causes a crash Don't show the power eater section if failed to get app info

### wingpanel-indicator-sound
Use device form factor when available to assign more accurate icons
Provide a fallback device icon when none is available
Fix missing switch animations
Use the volume step value from GNOME Settings Daemon
Updated translations

## Developer Platform

### iconbrowser
A modern redesign!

Fancy new icon
Drag the window from anywhere
Follow the system dark style preference
Updated for Gtk 4

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
7.1.0 ?

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
