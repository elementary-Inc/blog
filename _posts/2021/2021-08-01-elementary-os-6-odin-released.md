---
title: elementary OS 6 Odin
description: It’s finally here, and it’s the biggest update to the platform yet
author: cassidyjames
image: /images/elementary-os-6-odin-released/odin.png
tags:
  - odin
  - release
  - flatpak
---

<figure class="card" markdown="1">
![Screenshot of elementary OS 6 Odin]({{ page.image }})
</figure>

It's been a long road to elementary OS 6—what with a whole global pandemic dropped on us in the middle of development—but it's finally here. elementary OS 6 Odin is available to download now. And it's the biggest update to the platform yet! With OS 6, we've focused in on:

- Empowering you to **be in control** and **express yourself**,
- Continuing to innovate with **new features**, and
- Making elementary OS **easier to get** and **more inclusive**

To get elementary OS 6 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

## Be in Control & Express Yourself

elementary OS is designed to be easy to use, get out of your way, and not leave the hard decisions to you. At the same time, it exists to empower you to take control of your own devices and data. That's why we've always had an unmatched [commitment to privacy](https://elementary.io/privacy):

<aside markdown="1">
>Your data always belongs to you, and only you. We don’t make advertising deals or collect sensitive personal data. We’re funded directly by our users paying what they want for elementary OS and apps on AppCenter. And that’s how it should be.
</aside>

With OS 6, we're empowering you further with new ways to stay in control of your experience—plus new ways to express your own unique style and preferences.

### Dark Style & Accent Color

Get ready to turn down the lights, because Dark Style is here for elementary OS 6. The new visual style is available right from the Welcome screen or at any time from _System Settings_ → _Desktop_ → _Appearance_. Choose the classic Default style or a new Dark style, and the system and default apps will follow suit. Third-party apps are encouraged to follow this new preference, though we avoid breakage by not _forcing_ it; if your favorite app doesn't follow along, be sure to report that to its developer. Dark style can also be scheduled to follow sunset and sunrise for your location, or based on your own schedule.

<figure class="half">
  <picture>
    <source srcset="/images/{{ page.slug }}/onboarding-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Onboarding" src="/images/{{ page.slug }}/onboarding.png" width="532" height="450" />
  </picture>
  <picture>
    <source srcset="/images/{{ page.slug }}/appearance-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Desktop Appearance settings" src="/images/{{ page.slug }}/appearance.png" width="862" height="664" />
  </picture>
<figcaption markdown="1">
**Left:** Dark style and accent colors in the Welcome screen | **Right:** _System Settings_ → _Desktop_ → _Appearance_
</figcaption>
</figure>

We've also added 10 new accent colors to elementary OS, affecting everything from suggested action buttons and switches to text selection focus styles—and the new automatic accent color preference picks an accent color from your current wallpaper. elementary OS 6 is the most customizable version to date, enabling you to completely change the look by playing with different wallpapers, visual styles, and accent colors.

<aside markdown="1">
>elementary OS 6 is the most customizable version to date, enabling you to completely change the look.
</aside>

Both of these new features are made possible by a complete redesign and rewrite of the elementary OS system stylesheet. We revisited every detail from contextual shading and contrast to shadows, strokes, and border radii. The end result ensures _much_ better contrast throughout the whole OS while enabling unprecedented customization.

### Sandboxing & Portals

elementary OS 6 leverages cutting-edge sandboxing technology to enforce privacy and security protections at a technical level. In OS 6, all AppCenter apps are now packaged and distributed as Flatpaks, a modern container format that keeps apps siloed away from each other—and your sensitive data. Several default elementary OS apps are now being distributed as Flatpaks as well.

In addition, elementary OS 6 utilizes Portals to keep you in control of how apps interact with each other and your data. Apps must explicitly request permission in a well-defined way to get access to files, screenshots, or even launching other apps. A new Permissions view in _System Settings_ → _Applications_ exposes all the permissions apps have requested and gives you control to override or revoke them.

<figure markdown="1">
![Applications Permissions settings](https://github.com/elementary/switchboard-plug-applications/raw/master/data/screenshot-permissions.png?raw=true){: width="892" height="659"}
<figcaption markdown="1">
_System Settings_ → _Applications_ → _Permissions_
</figcaption>
</figure>

These protections are in place for apps installed from AppCenter, but importantly also apply to all apps installed via the built-in Sideload utility—including all third-party Flatpak apps from external sources like Flathub or a developer's own website. With these protections built in and elementary OS 6 being Flatpak-first, it's easier and safer than ever to get and use the apps you need.

## New Features

It wouldn't be a new OS release without exciting new features to improve your experience, and OS 6 delivers on that front.

### Multi-touch

One of the most pervasive new features for touchscreen and trackpad users is the new multi-touch support throughout elementary OS 6. A three-finger swipe up smoothly opens the Multitasking View, exposing open apps and workspaces. A three-finger swipe left or right smoothly switches between the dynamic workspaces, making it even faster to jump between tasks.

<figure class="half card" markdown="1">
![Multitasking View](/images/multitouch-gestures-in-elementary-os-6/multitasking.gif)
![Switching workspaces](/images/multitouch-gestures-in-elementary-os-6/workspaces.gif)
<figcaption markdown="1">
1:1 multi-touch gestures used for Multitasking View and switching workspaces
</figcaption>
</figure>

But it's not just the desktop that has multi-touch support; we've worked to bring smooth and intuitive two-finger multi-touch gestures into apps as well. Swipe through paged layouts like screenshots in AppCenter or steps in the Initial Setup and Welcome screens. Swipe to dismiss notification bubbles on screen or in the Notification Center. Swipe to go back in Web, System Settings, and several other apps. And smoothly swipe between users on the login/lockscreen greeter.

<figure class="third" markdown="1">
![AppCenter Screenshots](/images/multitouch-gestures-in-elementary-os-6/appcenter.gif)
![Notification Center](/images/multitouch-gestures-in-elementary-os-6/notification-center.gif){: width="399" height="672" }
![Keyboard Layouts](/images/multitouch-gestures-in-elementary-os-6/keyboard-layouts.gif)
<figcaption markdown="1">
**Left:** Swipe to switch pages | **Center:** Swipe to dismiss | **Right:** Swipe to go back
</figcaption>
</figure>

These new multi-touch gestures make elementary OS 6 faster and smoother to navigate on a touch screen or trackpad—all while ensuring each interaction is just as easy with a traditional mouse and keyboard as before.

### Notifications

elementary OS has always provided desktop notifications, but OS 6 brings a redesign and under-the-hood rewrite with richer, more capable notifications than ever.

<figure class="half" markdown="1">
![Notification with an icon badge](/images/elementary-os-6-odin-beta-2/notification-badge.png){: width="362" height="90"}
![Notification with action buttons](/images/elementary-os-6-odin-beta-2/notification-button.png){: width="362" height="129"}
<figcaption markdown="1">
New notification bubbles
</figcaption>
</figure>

Notification bubbles now feature badge capability, enabling apps to send richer information like a visual status indicator while ensuring you always know which app a notification is coming from. Apps can also now send actions along with notifications, which are displayed as buttons right within the notification bubble—it's easier than ever to not only be informed by apps, but to take quick actions without ever needing to open the app. 

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/notification-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Urgent notification bubble" src="/images/{{ page.slug }}/notification-light.png" width="362" height="90" />
  </picture>
<figcaption>Urgent notification bubble</figcaption>
</figure>

Since notifications are now using native GTK widgets just like native apps, they follow the dark style preference and emoji are displayed in full color. Urgent notifications sport a new look and a distinct sound to make them easier to identify. Lastly, notification bubbles also now support multi-touch swipe-to-dismiss on both touchscreens and trackpads.

<figure class="card" markdown="1">
![Notification Center](https://github.com/elementary/wingpanel-indicator-notifications/raw/master/data/screenshot.png?raw=true){: width="750" height="497"}
<figcaption markdown="1">
Redesigned Notification Center
</figcaption>
</figure>

Notification Center has also been redesigned; notifications here now match the look of notification bubbles including full-color emoji and badges. They're also more clearly grouped by app and support multi-touch swipe-to-dismiss.

### Tasks

The brand new Tasks app debuts in elementary OS 6, helping you tackle your to-do list whether it's stored on your device or synchronized with an online account.

<figure markdown="1">
![Tasks app](https://raw.githubusercontent.com/elementary/tasks/master/data/screenshot.png){: width="1015" height="769"}
</figure>

Tasks is designed around the open CalDav format, ensuring it's compatible with most online account providers. It supports synchronizing with multiple accounts and lists, time-based reminders, location-based reminders, and more.

### Firmware Updates

elementary OS 6 comes with firmware updates built in, powered by the [Linux Vendor Firmware Service](https://fwupd.org). Firmware updates are provided for supported devices by hardware manufacturers like Star Labs, Dell, Lenovo, HP, Intel, Logitech, Wacom, 8bitdo, and many more—now supported devices can get the latest updates for security and stability straight from _System Settings_ → _System_ → _Firmware_ or by searching the Applications Menu for “Firmware.”

<figure markdown="1">
![Firmware settings](https://github.com/elementary/switchboard-plug-about/raw/master/data/screenshot-firmware.png?raw=true){: width="892" height="659"}
<figcaption markdown="1">
Firmware updates built into System Settings
</figcaption>
</figure>

### App Updates

Several apps in elementary OS 6 sport brand new features, making OS 6 more capable than ever before.

<figure class="half" markdown="1">
![Web in a light style](/images/{{ page.slug }}/web.png)
![Web in a dark style](/images/{{ page.slug }}/web-dark.png)
<figcaption markdown="1">
Web in both light and dark styles
</figcaption>
</figure>

The web browser in elementary OS 6 has been updated and renamed. Formerly known as Epiphany, Web is now distributed as a Flatpak to enable even faster updates to support the latest web technologies. Web also features Intelligent Tracking Protection and ad blocking built-in and enabled by default for even greater privacy protections out of the box. The new reader mode brings a stripped down and easier to read view for content-heavy pages. Web follows the new dark style preference both with its own interface and for websites that support the standardized CSS color scheme preference. And as previously mentioned, Web now supports multi-touch swipes for navigating back and forth between pages for touch and trackpad users.

<figure markdown="1">
![Mail](https://raw.githubusercontent.com/elementary/mail/master/data/screenshot.png){: width="1352" height="777"}
<figcaption>Mail</figcaption>
</figure>

Mail has been completely rewritten in OS 6. With the rewrite comes tighter Online Accounts integration powered by the open source Evolution Data Server. To start, the new system-wide Online Accounts settings supports the IMAP standard for mail accounts, but we now have the foundation to add more types of accounts over time. The rewrite also brings web process sandboxing so each email is displayed in its own sandbox—improving safety and security. The new Mail is using native widgets instead of custom drawing in places like the message list and conversation view, greatly improving support for right-to-left languages and platform-wide accessibility features.

### Panel

In elementary OS 5.1 we added a tooltip to the Applications Menu to provide more information including keyboard shortcuts—making a core OS feature of launching apps more discoverable. In talking to several users, we learned that many didn't realize most indicators had a middle-click shortcut to quickly toggle its main control. So with OS 6, we've expanded this convention to the majority of indicators on the Panel on hover.

<figure class="card">
  <picture>
    <source srcset="/images/{{ page.slug }}/panel-tooltip-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Tooltip for the Sound indicator" src="/images/{{ page.slug }}/panel-tooltip.png" width="400" height="225" />
  </picture>
<figcaption>Tooltip for the Sound indicator</figcaption>
</figure>

Now, when hovering: the Sound indicator shows the precise volume and middle-click to mute shortcut; the Network indicator shows the current wireless network name; the Bluetooth indicator shows the on/off state and middle-click to toggle shortcut; the Power indicator exposes the precise battery percent and time until charged or empty, plus the middle-click to toggle shortcut; the Notifications indicator shows exactly how many notifications there are as well as the middle-click for Do Not Disturb shortcut; and the Session indicator details the current user's name and the middle-click to prompt to shut down shortcut.

All together, these changes mean the system indicators in elementary OS provide even more information without clicking and make handy, time-saving shortcuts far more discoverable than before.

## Easier to Get & More Inclusive

- Simpler installer and initial setup
- A11y features by default
- Continued work with hardware OEMs

## …and tons more

We've kept with the above themes throughout all the updates to elementary OS. Here's just a bit more of what's new in OS 6:

### System Settings

We've added even more capabilities to System Settings, enabling you to tune your system just how you want.

#### Desktop

Alongside the new Dark Style preference and accent colors in Desktop settings, we've expanded on the text size options, making it easier to fine-tune how your desktop looks. In addition, the new system stylesheet now uses the text size to smartly scale the rest of the UI, making it a real option for handling display resolutions that don't fit nicely into the integer scaling buckets—all while keeping the UI pixel-perfect and crisp.

<figure class="half" markdown="1">
![Desktop Dock & Panel settings](https://github.com/elementary/switchboard-plug-pantheon-shell/raw/master/data/screenshot-dock-panel.png?raw=true){: width="856" height="659"}
![Desktop Multitasking settings](https://github.com/elementary/switchboard-plug-pantheon-shell/raw/master/data/screenshot-multitasking.png?raw=true){: width="856" height="659"}
<figcaption markdown="1">
Dock & Panel and Multitasking settings
</figcaption>
</figure>

Desktop settings in OS 6 also bring new controls for when to move windows to a new workspace with options for toggling the behavior on fullscreen and maximize.

### Date & Time

We've redesigned the Date & Time settings in OS 6 with a more straightforward layout and new options.

<figure markdown="1">
![Date & Time settings](https://github.com/elementary/switchboard-plug-datetime/raw/master/data/screenshot.png?raw=true){: width="892" height="659"}
<figcaption markdown="1">
New Date & Time settings layout and options
</figcaption>
</figure>

Timezone configuration has been redesigned and moved from being hidden into the popover to being right in the main view. We've also added new options to show or hide the date, weekday, and seconds in the clock on the Panel.

---

## Apps

### mail 6.0.0 Released

Complete rewrite from scratch

### calendar 6.0.0 Released

New Features:

- Import ICS files from the gear menu
- Support the dark style

Fixes:

- Properly show events on the last day of the month
- Fix end times for all-day events
- Notify for all alarms on an event

Minor Updates:

- Improved offline support
- New colorful avatar fallbacks
- Include "film" as an event icon keyword
- Add Mint and Bubblegum to calendar color chooser
- Link to Online Accounts settings in the gear menu

### appcenter 3.6.0 Released

New features:

- Show in-app notification when an app is installed
- Add contextual badges to notifications

Improvements:

- Ensure Home button is usable during search
- Ask the user to manually restart if we can't ask the session to prompt
- Improve styling and contrast of buttons
- More concise and consistent language

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
- Stability improvements

Other updates:

- Rename "Devices" to "Storage"

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

### photos 2.7.1 Released

- Fix keyboard activation in tool windows
- Show saved state correctly in the context-menu

### videos 2.7.3 Released

Other updates:

- Fix an issue with accessing library view
- Fix an issue with returning to the welcome page while playing multiple videos
- Prevent sleep while playing a video

## Settings

### switchboard 6.0.0 Released

- Add multi-touch navigation gestures
- Better support smaller displays
- Remove old GNOME Control Center compatibility layer
- Stability and performance improvements

### switchboard-plug-pantheon-shell 6.0.0 Released

- Dyslexia-friendly text preference to use the OpenDyslexia font system-wide

### switchboard-plug-about 6.0.0 Released

Redesign and new features:

- Rename from About to System
- Split Hardware and Operating System info into their own tabs
- Redesign the Operating System tab with clearer links and buttons
- Add a Firmware view to manage device firmware updates

More information:

- Provide information for ARM CPUs
- Provide information for more types of Graphics

### switchboard-plug-onlineaccounts 6.0.0 Released

Complete redesign based on Evolution Data Server

### switchboard-plug-mouse-touchpad 6.0.0 Released

- Multi-touch gesture options
- Add more snap points to pointer speed sliders
- Redesigned touchpad settings

### switchboard-plug-parental-controls 6.0.0 Released

Fixes:

- Set default Screen Time from midnight to midnight to prevent accidental lockouts
- Improve reliability of app blocking
- Support blocking Flatpak apps

Minor updates:

- Clarify how Screen Time limits work and when they take effect
- New colorful avatar fallback

### switchboard-plug-useraccounts 2.4.0 Released

Minor updates:

- New colorful avatar fallback
- Improved tooltips and labels
- Fix possible crash when deleting an account

### switchboard-plug-notifications 2.2.0 Released

Minor updates:

- New illustrations

### switchboard-plug-keyboard 2.5.0 Released

Minor updates:

- Add Layout popover is now a dialog
- Guarantee we always have at least one layout
- Improvements to ibus and xkb layouts

### switchboard-plug-power 2.5.0 Released

- Change lid settings without restarting
- Show in search results for "sleep" and "timeout"

### switchboard-plug-network 2.4.0 Released

- Show message when Ethernet is unplugged
- Show DNS info

### switchboard-plug-display 2.3.0 Released

- Support 3× scaling
- Reliably detect accelerometers

### switchboard-plug-a11y 2.3.0 Released

- Add a switch to show the indicator in the Panel
- Point out how to find other accessibility features in System Settings

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

### greeter 6.0.0 Released

- Add multi-touch finger tracking
- Add keyboard layout support
- New colorful avatar fallbacks
- Fix clock when resuming from sleep

### initial-setup 6.0.0 Released

Minor updates:

- Set keyboard layout in accountsservice
- Add multi-touch gestures
- Set correct locales
- New colorful avatar fallback

### onboarding 6.0.0 Released

- Add style view
- Add Online Accounts view
- Remove location services view
- Mention Sideload and Flathub

### shortcut-overlay 1.2.0 Released

- Add screenshot shortcuts
- Fix issues with multiple windows

### sideload 6.0.0 Released

- Control notifications in System Settings
- Offer to trash Flatpak files after installing
- Support dark style
- Support Flatpak bundle files
- Fix crashes on installation failure
- Link to System Settings → Applications → Permissions

### feedback 6.0.0 Released

Improvements:

- Show Flatpak Apps
- Support dark style
- Add multi-touch navigation gestures

### screenshot 6.0.0 Released

- Support the dark style
- Drag and Drop the preview image from the save dialog
- Drag to move the window from anywhere
- Show details for errors if they occur

## Panel

### New

- wingpanel-indicator-a11y

### wingpanel 3.0.0 Released

Improvements:

- Fix some issues with indicator sort order
- Adjust special icon colors for dark and light panels to improve contrast
- Fix getting monitor dimensions under Wayland
- Hide tooltips when indicators are open

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

### wingpanel-indicator-notifications 6.0.0 Released

Complete redesign:

- Multi-touch gestures to dismiss notifications
- Close button on each notification
- Show images and badged icons

Minor updates:

- Show tooltip on hover

### wingpanel-indicator-sound 6.0.0 Released

- select specific input and output devices
- Hide temporary audio players when they stop
- Add a tooltip on hover
- Minor visual improvements

### wingpanel-indicator-network 2.3.0 Released

- Fix VPN spinning after connecting
- Improve detecting network encryption type
- Ellipsize long network names
- Show tooltip on hover

### wingpanel-indicator-session 2.3.0 Released

- New colorful avatar fallback
- Tooltip on hover

### wingpanel-indicator-power 6.0.0 Released

New features:

- Show battery statistics when selected
- Launch apps using power when selected
- Control display brightness by scrolling the indicator

Minor updates:

- Improvements for desktops with peripherals
- Filter out internal devices
- Show tooltip on hover

### wingpanel-indicator-datetime 2.3.0 Released

- Add multi-touch gestures
- Improve time zone handling

### wingpanel-indicator-keyboard 2.4.0 Released

Minor updates:

- Show IBus input methods
- Show tooltip on hover

### wingpanel-indicator-bluetooth 2.1.7 Released

- Add tooltip on hover
- Add a fallback device name for headphones

### wingpanel-indicator-nightlight 2.1.0 Released

- Show tooltip on hover

## Little Stuff

### calculator 1.6.1 Released

Minor updates:

- Fixed an issue with multiple windows
- More informative copy in history dialog

### capnet-assist 2.3.0 Released

- Dark style support

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

---

## Release Notes

For detailed release notes organized by version number of each individual component, you can always view our [public Releases site](https://releases.elementary.io).

[elementary.io]: https://elementary.io
