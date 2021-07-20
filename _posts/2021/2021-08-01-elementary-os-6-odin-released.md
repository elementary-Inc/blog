---
title: elementary OS 6 Odin
description:
author: cassidyjames
tags:
  - odin
---

## Apps

### mail 6.0.0 Released

Complete rewrite from scratch

### appcenter 3.6.0 Released

New features:

- Show in-app notification when an app is installed
- Add contextual badges to notifications

Improvements:

- Ensure Home button is usable during search
- Ask the user to manually restart if we can't ask the session to prompt
- Improve styling and contrast of buttons
- More concise and consistent language
- Updated translations

Fixes:

- Fully uninstall Flatpaks, including locales
- Still fetch screenshots from remotes that don't include proper headers
- Fix truncated footer buttons
- Only show Mail button when a usable mail app is installed
- Fix some apps incorrectly showing as not installed during search
- Show an error dialog when opening an app fails

### files 6.0.0 Released

Fixes:

- Fix connecting to AFP servers so that passwords are remembered
- Fix MTP mounts

Improvements:

- Launch files with double click instead of single click
- Provide a File Chooser portal for Flatpak apps
- Brand new animated Sidebar
- Dark style support
- Mint and Bubblegum color tags
- Do not restore locations that have become inaccessible
- Clicking between thumbnail and text now activates/selects in Icon view
- AFC protocol support
- Add a smaller minimum icon size in list view
- Show emblems inline in list views
- Performance improvements
- Stability improvements

Other updates:

- Rename "Devices" to "Storage"
- Updated translations

### music 5.1.0 Released

- Fix an issue with saving smart playlists
- Drop support for CD-ROM and Last.fm
- Dark style support
- Minor visual improvements

### code 6.0.0 Released

New features:

- New Markdown plugin for WYSIWYG-like editing.
- Switch Git branches or create new ones in project folder context menus
- Show Git diff status in source view gutters
- Full text search within project folder.
- Save and restore cursor position between sessions
- Close files from a project when that project is closed
- Show full file path in tab tooltips
- Clear lines with Ctrl + K

Minor updates:

- Allow Spell Checker extension in Markdown files
- Improve multi-line duplication
- Remember whether the sidebar is open
- Set window title to the focused file
- Add keyboard shortcuts for next and previous documents
- Show full document path in tab tooltip
- Update Pastebin plugin
- Correctly indent last line when using the preserve whitespace plugin
- Keep syntax highlighting when duplicating a file
- Expand a collapsed folder if you attempt to open it twice
- Fix an issue where searches are lost when Code loses focus
- Start Vim plugin in command mode
- Fix and add new Vim commands
- Show project folders with a hidden root folder
- Allow launching with pkexec and disallow launching with sudo
- Remove split view
- Remove browser preview
- Updated translations

### terminal 6.0.0 Released

New features:

- Move tabs with the shortcut Ctrl + Alt + ←/→
- Switch tabs with the shortcuts Ctrl + Tab and Ctrl + Shift + Tab
- Zoom levels are now remembered per-tab
- Also warn about multi-line pastes
- Show text details in unsafe paste dialogs
- Open Link option when secondary clicking
- Reload tabs in the context menu or with the shortcut Ctrl + Shift + R
- Notifications indicate if a process exited with errors or not
- Show keyboard shortcuts in tab context menus

Other updates:

- Fix an issue with keyboard shortcuts not activating the first time they're pressed
- Avoid losing focus when closing background tabs
- Validate custom palette
- Translation updates

### photos 2.7.1 Released

- Fix keyboard activation in tool windows
- Show saved state correctly in the context-menu
- Translation updates

### videos 2.7.3 Released

Other updates:

- Fix an issue with accessing library view
- Fix an issue with returning to the welcome page while playing multiple videos
- Prevent sleep while playing a video
- Translation updates

## Settings

### switchboard-plug-pantheon-shell 6.0.0 Released

New features:

- Accent color and dark style options
- Dyslexia-friendly text preference to use the OpenDyslexia font system-wide
- Maximize and fullscreen workspace management options

Other updates:

- Fix a freeze after opening Power settings
- Improved filter for image file types when importing
- Visual updates
- Some options now appear in different tabs
- Updated translations

### switchboard-plug-about 6.0.0 Released

Redesign and new features:

- Rename from About to System
- Split Hardware and Operating System info into their own tabs
- Redesign the Operating System tab with clearer links and buttons
- Add a Firmware view to manage device firmware updates

More information:

- Provide information for ARM CPUs
- Provide information for more types of Graphics

Fixes:

- Fix an issue where the view was destroyed early when navigating away
- Fix system memory calculation

Minor updates:

- Ellipsize long hardware names
- Performance improvements
- Updated translations

### switchboard-plug-datetime 2.2.0 Released

Minor updates

- Move timezone popover contents to the main view
- Add options to show or hide the date, weekday, and seconds in the clock
- Updated translations

### switchboard-plug-onlineaccounts 6.0.0 Released

Complete redesign based on Evolution Data Server

### switchboard-plug-applications 6.0.0 Released

New features:

- Manage permissions for Flatpak apps

Minor updates:

- Show custom launcher files
- Updated translations

### switchboard-plug-mouse-touchpad 6.0.0 Released

New features:

- Multitouch gesture options

Minor updates:

- Add more snap points to pointer speed sliders
- Multitouch gesture options
- Redesigned touchpad settings
- Updated translations

### switchboard-plug-parental-controls 6.0.0 Released

Fixes:

- Set default Screen Time from midnight to midnight to prevent accidental lockouts
- Improve reliability of app blocking
- Support blocking Flatpak apps

Minor updates:

- Clarify how Screen Time limits work and when they take effect
- New colorful avatar fallback
- Updated translations

### switchboard-plug-useraccounts 2.4.0 Released

Minor updates:

- New colorful avatar fallback
- Performance improvements
- Improved tooltips and labels
- Fix possible crash when deleting an account
- Updated translations

### switchboard-plug-notifications 2.2.0 Released

Minor updates:

- New illustrations
- Updated translations

### switchboard-plug-keyboard 2.5.0 Released

Minor updates:

- Add Layout popover is now a dialog
- Guarantee we always have at least one layout
- Improvements to ibus and xkb layouts
- Updated translations

### switchboard 6.0.0 Released

- Add multi-touch navigation gestures
- Better support smaller displays
- Remove old GNOME Control Center compatibility layer
- Stability and performance improvements
- Updated translations

### switchboard-plug-power 2.5.0 Released

Minor updates:

- Change lid settings without restarting
- Show in search results for "sleep" and "timeout"
- Updated translations

### switchboard-plug-network 2.4.0 Released

Minor updates

- Show message when Ethernet is unplugged
- Show DNS info
- Updated translations

### switchboard-plug-display 2.3.0 Released

New features:

- Support 3× scaling

Fixes:

- Reliably detect accelerometers

Minor updates:

- Updated translations

### switchboard-plug-a11y 2.3.0 Released

Fixes:

- Ensure screen reader shortcut keys are shown

Minor updates:

- Add a switch to show the indicator in the Panel
- Point out how to find other accessibility features in System Settings
- Updated translations

## Desktop/first-run?

### New:

- Settings Daemon
- Installer

### Gala 6.0.0 Released

Improvements:

- Add multi-touch gestures
- Show window titles in multitasking view
- Close the Alt + Tab switcher by pressing Esc without releasing Alt
- Increase maximum zoom level and provide feedback when unable to zoom
- Show a context menu when secondary clicking the background
- New Dwell Click and Locate Pointer animations
- Add Take Screenshot to window context menu
- Always play shutter sound when taking screenshots
- Minor visual improvements
- HiDPI fixes
- Performance improvements
- Updated translations

### notifications 6.0.0 Released

Complete rewrite:

- Support the dark style
- Action buttons
- Optional badge icons
- Automatically badge images with app icons
- Swipe away to dismiss

### greeter 6.0.0 Released

- Add multi-touch finger tracking
- Add keyboard layout support
- New colorful avatar fallbacks
- Fix clock when resuming from sleep
- Updated translations

### initial-setup 6.0.0 Released

Minor updates:

- Set keyboard layout in accountsservice
- Add multi-touch gestures
- Set correct locales
- New colorful avatar fallback
- Translation updates

### onboarding 6.0.0 Released

- Add style view
- Add Online Accounts view
- Remove location services view
- Mention Sideload and Flathub
- Updated translations

### shortcut-overlay 1.2.0 Released

- Add screenshot shortcuts
- Fix issues with multiple windows
- Updated translations

### sideload 6.0.0 Released

- Control notifications in System Settings
- Offer to trash Flatpak files after installing
- Support dark style
- Support Flatpak bundle files
- Fix crashes on installation failure
- Updated translations
- Link to System Settings → Applications → Permissions

### feedback 6.0.0 Released

Improvements:

- Show Flatpak Apps
- Support dark style
- Add multi-touch navigation gestures

Minor updates:

- Ensure links are up-to-date
- Updated translations

## Panel

### New

- wingpanel-indicator-a11y

### wingpanel 3.0.0 Released

Improvements:

- Fix some issues with indicator sort order
- Adjust special icon colors for dark and light panels to improve contrast
- Fix getting monitor dimensions under Wayland
- Hide tooltips when indicators are open
- Updated translations

Deprecations:

- Wingpanel.Widgets.Container: Use Gtk.ModelButton instead
- Wingpanel.Widgets.Separator: Use Gtk.Separator instead
- Wingpanel.Widgets.Switch: Use Granite.SwitchModelButton instead

Removals:

- Wingpanel.Widgets.AutomaticScrollBox: use Gtk.ScrolledWindow.max_content_height instead
- Wingpanel.Widgets.Button: Use Gtk.ModelButton instead

### applications-menu 2.8.0 Released

Minor updates

- Sort app actions above AppCenter search
- Always hide Terminal-based programs
- Remove document viewer from block list
- Support fractions without leading number in calculator
- Show overlay key in tooltip when set
- Performance improvements
- Updated translations

### wingpanel-indicator-notifications 6.0.0 Released

Complete redesign:

- Multi-touch gestures to dismiss notifications
- Close button on each notification
- Show images and badged icons

Minor updates:

- Show tooltip on hover
- Performance improvements
- Updated translations

### wingpanel-indicator-sound 6.0.0 Released

New features

- select specific input and output devices

Minor updates

- Hide temporary audio players when they stop
- Add a tooltip on hover
- Minor visual improvements
- Updated translations

### wingpanel-indicator-network 2.3.0 Released

Fixes:

- Fix VPN spinning after connecting
- Improve detecting network encryption type

Minor updates:

- Ellipsize long network names
- Show tooltip on hover
- Updated translations

### wingpanel-indicator-session 2.3.0 Released

Minor updates:

- New colorful avatar fallback
- Tooltip on hover
- Performance improvements
- Updated translations

### wingpanel-indicator-power 6.0.0 Released

New features:

- Show battery statistics when selected
- Launch apps using power when selected
- Control display brightness by scrolling the indicator

Minor updates:

- Improvements for desktops with peripherals
- Filter out internal devices
- Show tooltip on hover
- Performance improvements
- Updated translations

### wingpanel-indicator-datetime 2.3.0 Released

- Add multi-touch gestures
- Improve time zone handling
- Updated translations

### wingpanel-indicator-keyboard 2.4.0 Released

Minor updates:

- Show IBus input methods
- Show tooltip on hover
- Updated translations

### wingpanel-indicator-bluetooth 2.1.7 Released

- Add tooltip on hover
- Add a fallback device name for headphones
- Updated translations

### wingpanel-indicator-nightlight 2.1.0 Released

- Show tooltip on hover
- Performance improvements
- Updated translations

## Little Stuff

### calculator 1.6.1 Released

Minor updates:

- Fixed an issue with multiple windows
- More informative copy in history dialog
- Updated translations

### capnet-assist 2.3.0 Released

- Dark style support
- Updated translations


## Look & Feel

### icons 6.0.0 Released

Updated families:

- Improved consistency between arrow shapes
- Improved appearance of color icons against dark backgrounds
- More gender-neutral people icons
- Rounded media controls
- Rounded lightening bolt shape
- More colorful battery icons

Additions:

- align-*
- color-picker
- distribute-*
- draw-calligraphic
- office-database-new
- tools-spray
- application-content-*
- thunderbolt devices
- video-display-tv
- symbolic headphones
- application-certificate
- application-json
- office-task-symbolic
- status emblems
- emblem-git-*

Removals:

- accessories-camera
- accessories-screenshot
- audio-speaker-testing
- edit-undo-archive
- internet-mail
- internet-news-reader
- multimedia-audio-player
- notification bell animations
- nm-*
- ubiquity

### wallpapers 6.0.0 Released

- Add day and night custom Odin wallpapers by Freehive
- Add Snow-capped Mountain, Martin Adams, Tj Holowaychuk, and Vikor Forgacs
- Remove Carmine de Fazio, Luca Bravo, Pablo Garcia Saldana, Rob Bye, and Ryan Schroeder

### sound-theme 1.1.0 Released

- Add dialog-warning


## Developers

### granite 6.1.0 Released

Additions:

- `TRANSITION_DURATION_IN_PLACE` for consistent in-place widget transformations

Other Changes:

- `accel_to_string` handles accel markup without modifiers or that are only modifiers
- Updated translations

---

For more detailed release notes (nerds): https://releases.elementary.io/
