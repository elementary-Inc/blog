---
title: elementary OS 6 Odin Available Now
description: It’s finally here, and it’s the biggest update to the platform yet
author: cassidyjames
image: /images/elementary-os-6-odin-released/odin.png
thanks: true
tags:
  - odin
  - release
  - flatpak

hidden: 2021-08-09 15:00:00 UTC # 9 AM MDT
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

<figure class="half" markdown="1">
![Desktop Dock & Panel settings](https://github.com/elementary/switchboard-plug-pantheon-shell/raw/master/data/screenshot-dock-panel.png?raw=true){: width="856" height="659"}
![Desktop Multitasking settings](https://github.com/elementary/switchboard-plug-pantheon-shell/raw/master/data/screenshot-multitasking.png?raw=true){: width="856" height="659"}
<figcaption markdown="1">
Dock & Panel and Multitasking settings
</figcaption>
</figure>

Desktop settings in OS 6 also bring new controls for when to move windows to a new workspace with options for toggling the behavior on fullscreen and maximize.

<aside markdown="1">
>elementary OS 6 is the most customizable version to date, enabling you to completely change the look.
</aside>

These new features are made possible by a complete redesign and rewrite of the elementary OS system stylesheet. We revisited every detail from contextual shading and contrast to shadows, strokes, and border radii. The end result ensures _much_ better contrast throughout the whole OS while enabling unprecedented customization.

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "look-and-feel-changes-elementary-os-6" | first %}
{% include featured.html post=post %}
</div>

### Sandboxing & Portals

elementary OS 6 leverages cutting-edge sandboxing technology to enforce privacy and security protections at a technical level. In OS 6, all AppCenter apps are now packaged and distributed as Flatpaks, a modern container format that keeps apps siloed away from each other—and your sensitive data. Several default elementary OS apps are now being distributed as Flatpaks as well.

In addition, elementary OS 6 utilizes Portals to keep you in control of how apps interact with each other and your data. Apps must explicitly request permission in a well-defined way to get access to files, screenshots, or even launching other apps. A new Permissions view in _System Settings_ → _Applications_ exposes all the permissions apps have requested and gives you control to override or revoke them.

<figure class="constrained" markdown="1">
![Applications Permissions settings](https://github.com/elementary/switchboard-plug-applications/raw/master/data/screenshot-permissions.png?raw=true){: width="892" height="659"}
<figcaption markdown="1">
_System Settings_ → _Applications_ → _Permissions_
</figcaption>
</figure>

These protections are in place for apps installed from AppCenter, but importantly also apply to all apps installed via the built-in Sideload utility—including all third-party Flatpak apps from external sources like Flathub or a developer's own website. With these protections built in and elementary OS 6 being Flatpak-first, it's easier and safer than ever to get and use the apps you need.

## New Features

It wouldn't be a new OS release without exciting new features to improve your experience, and OS 6 delivers on that front.

### Multi-touch

One of the most pervasive new features for touch screen and touchpad users is the new multi-touch support throughout elementary OS 6. A three-finger swipe up smoothly opens the Multitasking View, exposing open apps and workspaces. A three-finger swipe left or right smoothly switches between the dynamic workspaces, making it even faster to jump between tasks.

<figure class="half card" markdown="1">
![Multitasking View](/images/multitouch-gestures-in-elementary-os-6/multitasking.gif)
![Switching workspaces](/images/multitouch-gestures-in-elementary-os-6/workspaces.gif)
<figcaption markdown="1">
1:1 multi-touch gestures used for Multitasking View and switching workspaces
</figcaption>
</figure>

But it's not just the desktop that has multi-touch support; we've worked to bring smooth and intuitive two-finger multi-touch gestures into apps as well. Swipe through paged layouts like screenshots in AppCenter, months in the Date & Time indicator, or steps in the Initial Setup and Welcome screens. Swipe to dismiss notification bubbles on screen or in the Notification Center. Swipe to go back in Web, System Settings, and several other apps. And smoothly swipe between users on the login/lockscreen greeter.

<figure class="third" markdown="1">
![AppCenter Screenshots](/images/multitouch-gestures-in-elementary-os-6/appcenter.gif)
![Notification Center](/images/multitouch-gestures-in-elementary-os-6/notification-center.gif){: width="399" height="672" }
![Keyboard Layouts](/images/multitouch-gestures-in-elementary-os-6/keyboard-layouts.gif)
<figcaption markdown="1">
**Left:** Swipe to switch pages | **Center:** Swipe to dismiss | **Right:** Swipe to go back
</figcaption>
</figure>

These new multi-touch gestures make elementary OS 6 faster and smoother to navigate on a touch screen or touchpad—all while ensuring each interaction is just as easy with a traditional mouse and keyboard as before. Multi-touch gestures can be customized from _System Settings_ → _Mouse & Touchpad_ → _Gestures_.

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

Since notifications are now using native GTK widgets just like native apps, they follow the dark style preference and emoji are displayed in full color. Urgent notifications sport a new look and a distinct sound to make them easier to identify. Lastly, notification bubbles also now support multi-touch swipe-to-dismiss on both touch screens and touchpads.

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

<figure class="constrained" markdown="1">
![Firmware settings](https://github.com/elementary/switchboard-plug-about/raw/master/data/screenshot-firmware.png?raw=true){: width="892" height="659"}
<figcaption markdown="1">
Firmware updates built into System Settings
</figcaption>
</figure>

### App Updates

Several apps in elementary OS 6 sport brand new features, making OS 6 more capable than ever before.

<figure class="half" markdown="1">
![Screenshot of Web in a light style](/images/{{ page.slug }}/web.png)
![Screenshot of Web in a dark style](/images/{{ page.slug }}/web-dark.png)
<figcaption markdown="1">
Web in both light and dark styles
</figcaption>
</figure>

The web browser in elementary OS 6 has been updated and renamed. Formerly known as Epiphany, Web is now distributed as a Flatpak to enable even faster updates to support the latest web technologies. Web also features Intelligent Tracking Protection and ad blocking built-in and enabled by default for even greater privacy protections out of the box. The new reader mode brings a stripped down and easier to read view for content-heavy pages. Web follows the new dark style preference both with its own interface and for websites that support the standardized CSS color scheme preference. And as previously mentioned, Web now supports multi-touch swipes for navigating back and forth between pages for touch and touchpad users.

<figure markdown="1">
![Screenshot of Mail](https://raw.githubusercontent.com/elementary/mail/master/data/screenshot.png){: width="1352" height="777"}
<figcaption>Mail</figcaption>
</figure>

Mail has been completely rewritten in OS 6. With the rewrite comes tighter Online Accounts integration powered by the open source Evolution Data Server. To start, the new system-wide Online Accounts settings supports the IMAP standard for mail accounts, but we now have the foundation to add more types of accounts over time. The rewrite also brings web process sandboxing so each email is displayed in its own sandbox—improving safety and security. The new Mail is using native widgets instead of custom drawing in places like the message list and conversation view, greatly improving support for right-to-left languages and platform-wide accessibility features.

<figure markdown="1">
![Screenshot of Calendar](/images/{{ page.slug }}/calendar.png){: width="1039" height="765"}
<figcaption>Calendar</figcaption>
</figure>

Calendar also supports the Online Accounts integration via the CalDav standard; add any CalDav-compliant account in System Settings, and its events and tasks will show up in the Calendar and Tasks apps. We've also added ICS import, improved offline support, and fixed a number of issues around all-day events and timezones.

<figure markdown="1">
![Screenshot of Camera](/images/{{ page.slug }}/camera.png){: width="704" height="544"}
<figcaption>Camera</figcaption>
</figure>

We've revamped Camera in OS 6 with a fresh UI and several new features. Camera now supports switching between multiple cameras, toggling mirroring of the image, and brightness and contrast adjustment. When a recording is finished, Camera now sends an in-app notification with a button to open the video—perfect for making sure it looks how you want.

<figure markdown="1">
![Screenshot of AppCenter](/images/{{ page.slug }}/appcenter.png){: width="1081" height="669"}
<figcaption>AppCenter</figcaption>
</figure>

With elementary OS 6 being all-in on Flatpaks, AppCenter has been updated to match. While we've always reviewed, approved, and curated third-party AppCenter apps, they're now also distributed as sandboxed Flatpaks for even stronger privacy and security. When an app is installed from a list, AppCenter now shows an in-app notification when it's complete so it's even faster to open. We've improved the design of app headers, including the contrast of buttons. And AppCenter notifications now provide richer context with improved language and contextual badges for installed apps and updates.

<figure markdown="1">
![Screenshot of Files](/images/{{ page.slug }}/files.png){: width="924" height="608"}
<figcaption>Files</figcaption>
</figure>

After a lot of user feedback, testing, and iterating, we're shipping a subtle but important behavioral change to Files in elementary OS 6: as always, a single click navigates between folders, but opening a file in its default app now uses a double click. This change balances the efficiency of single-click navigation (matching the rest of the OS and the web) while addressing the real issue of accidentally opening multiple copies of a file or opening a large file in a slower-loading app. Files also has an all-new sidebar in OS 6 that makes it easier to drag to bookmark folders while sporting slick animations. We've also improved the list view with a smaller minimum size and added file emblems for communicating statuses like permissions or new files in a Git project, added Mint and Bubblegum colors for files tags, improved click targets for files, and improved support for devices using AFP, AFC, and MTP protocols. And Files now provides the File Chooser interface for Flatpak apps for more consistency.

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/code-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Screenshot of Code" src="/images/{{ page.slug }}/code.png" width="1174" height="703" />
  </picture>
<figcaption>Code</figcaption>
</figure>

For developers, we've continued to improve Code in OS 6. You'll notice a new project button in the header bar which shows the active Git project and enables quickly switching between open projects. Closing a project also now closes any of its open files. We've continued to iterate on Git integration by introducing the ability to switch and create branches, and by adding new line-by-line Git status in the gutter. Markdown support has been improved with new WYSIWYG-like editor shortcuts and spell check support. We've implemented an all-new full text search within folders and entire projects with togglable case sensitivity and regular expression support. For Vim-mode users, you'll notice both new and improved Vim commands as well as Code defaulting to command mode when enabled. We've also improved how Code saves and restores its state in OS 6, now including cursor position and the state of the sidebar when closing and re-opening the app.

<figure class="half">
  <picture>
    <source srcset="/images/{{ page.slug }}/terminal.png" media="(prefers-color-scheme: dark)">
    <img alt="Screenshot of Terminal" src="/images/{{ page.slug }}/terminal-light.png" width="788" height="555" />
  </picture>
  <picture>
    <source srcset="/images/{{ page.slug }}/terminal-paste-protection.png" media="(prefers-color-scheme: dark)">
    <img alt="Screenshot of paste protection dialog" src="/images/{{ page.slug }}/terminal-paste-protection-light.png" width="545" height="329" />
  </picture>
<figcaption>Terminal</figcaption>
</figure>

While users of elementary OS never _need_ Terminal to complete basic tasks, it's a fan favorite of developers and seasoned Linux users—and it's better than ever in OS 6. A flagship feature of the elementary Terminal is smart paste protection; in OS 6 this has been expanded to include multi-line pastes in addition to `sudo` pastes. We've also revised the paste protection copy for clarity and added expandable details including the command that would be executed. Zoom levels are now handled and remembered per-tab. You can now reload a tab from its context menu or with <kbd>Shift</kbd><kbd>Ctrl</kbd><kbd>R</kbd>. We've also added keyboard shortcuts for moving tabs (<kbd>Ctrl</kbd><kbd>Alt</kbd><kbd>←</kbd>/<kbd>→</kbd>) and switching between tabs (<kbd>Ctrl</kbd><kbd>Tab</kbd>). And now in OS 6, all Terminal actions that have keyboard shortcuts show their shortcuts right in the context menu so they're easier to learn and remember. Lastly, process completion notifications now include a badge and copy to indicate whether the process exited with errors or not.

We've improved each of these apps and more in OS 6 like Music, Videos, Photos, and Calculator with bug fixes, improved performance, and updated localization.

### Panel

In elementary OS 5.1 we added a tooltip to the Applications Menu to provide more information including keyboard shortcuts—making a core OS feature of launching apps more discoverable. In talking to several users, we learned that many didn't realize most indicators had a middle-click shortcut to quickly toggle its main control. So with OS 6, we've expanded this convention to the majority of indicators on the Panel on hover.

<figure class="card">
  <picture>
    <source srcset="/images/{{ page.slug }}/panel-tooltip-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Tooltip for the Sound indicator" src="/images/{{ page.slug }}/panel-tooltip.png" width="400" height="225" />
  </picture>
<figcaption>Tooltip for the Sound indicator</figcaption>
</figure> 

Now, when hovering: the Night Light indicator shows the status and middle-click to snooze shortcut; the Sound indicator shows the precise volume and middle-click to mute shortcut; the Network indicator shows the current wireless network name; the Bluetooth indicator shows the on/off state and middle-click to toggle shortcut; the Power indicator exposes the precise battery percent and time until charged or empty, plus the middle-click to toggle shortcut; the Notifications indicator shows exactly how many notifications there are as well as the middle-click for Do Not Disturb shortcut; and the Session indicator details the current user's name and the middle-click to prompt to shut down shortcut.

<figure class="card" markdown="1">
![Screenshot of Sound indicator](/images/{{ page.slug }}/sound-indicator.png){: width="750" height="473"}
<figcaption>Sound indicator</figcaption>
</figure>

We've expanded the functionality of the Sound indicator in OS 6, as well: the indicator now shows both input and output devices right in the popover, making changing between headphones and speakers or different mics easier on the go, without having to open the full sound settings.

<figure class="card" markdown="1">
![Screenshot of Power indicator](/images/{{ page.slug }}/power-indicator.png){: width="750" height="300"}
<figcaption>Power indicator</figcaption>
</figure>

We've improved the Power indicator in OS 6 with better support for desktop devices plus a handy new feature: selecting a device in the popover now opens a Power Statistics interface with more information like the design energy and total capacity of the device's battery.

All together, these changes mean the system indicators in elementary OS 6 are more powerful and make handy, time-saving shortcuts far more discoverable than before.

### System Settings

We've improved several areas in System Settings for OS 6 in addition to what has been mentioned elsewhere. We've improved the

## Easier to Get & More Inclusive

We're always expanding the elementary OS platform and ecosystem making it more useful, desirable, get-able, and keep-able—an approach coined by former Canonical designer [Matthew Paul Thomas](https://twitter.com/mpt) all the way [back in 2010](https://www.youtube.com/watch?v=GT5fUcMUfYg) and covered in our [AppCenter & the Future of the Universe](/appcenter-the-future-of-the-universe) post.

elementary OS 6 makes great strides on the "get-able" front; first [teased in 2018](/meet-the-upcoming-installer), the new installer front-end designed and developed by elementary debuts in OS 6. The new installer has been designed to be simpler, more straightforward, and much faster than the previous Ubiquity installer developed by Canonical for Ubuntu.

<figure class="third" markdown="1">
![Screenshot of Initial Setup's Language page](/images/{{ page.slug }}/initial-setup-language.png)
![Screenshot of Initial Setup's Keyboard page](/images/{{ page.slug }}/initial-setup-keyboard.png)
![Screenshot of Installer's Try or Install page](/images/{{ page.slug }}/installer-try-install.png)
![Screenshot of Installer's Drives page](/images/{{ page.slug }}/installer-drives.png)
![Screenshot of Installer's Encryption page](/images/{{ page.slug }}/installer-encrypt.png)
![Screenshot of Installer's Progress page](/images/{{ page.slug }}/installer-progress.png)
![Screenshot of Installer's Success page](/images/{{ page.slug }}/installer-success.png)
<figcaption>Installer</figcaption>
</figure>

A key consideration of the new installer is that "every install is an OEM install." The installer's job is solely to get the OS onto a device and little more; after installing, you're prompted to either shut down (e.g. to hand the device off to another person) or restart into the new OS. Either way, user account creation is handled in the installed OS by our new Initial Setup utility, then you log straight in to start using your account.

<figure markdown="1">
![Screenshot of Initial Setup's User page](/images/{{ page.slug }}/initial-setup-user.png){: width="916" height="666"}
<figcaption>Initial Setup</figcaption>
</figure>

This means we don't handle network connectivity, user accounts, or updates in the installer itself, greatly streamlining and speeding up the process. It also means small OEMs or organizations that hand-install the OS on devices (rather than using an imaging server, for example) can do so quickly and easily, shutting the device down once it's installed and shipping it off straight to a user. It also means OEMs or organizations that _do_ use an image-based approach can configure a custom install of elementary OS (e.g. by installing any additional hardware drivers), delete the OEM account, and make an image of that; once booted on hardware, Initial Setup will run for a new user just like on a standard fresh install.

With elementary OS shipping on [several hardware devices from multiple retailers](https://store.elementary.io), we've also continued investing in [hardware improvements](/hardware-improvements-coming-to-elementary-os). OS 6 features a new streamlined startup prominently displaying the device manufacturer's logo along with minimal elements like a loading spinner or password entry for encrypted drives. Startup is intentionally non-elementary-branded as it feels much more seamless—and we don't need to constantly advertise your operating system to you.

<figure class="half card" markdown="1">
![Boot Screen: loading spinner](/images/hardware-improvements-coming-to-elementary-os/boot-loading.jpg)
![Boot Screen: unlocking an encrypted drive](/images/hardware-improvements-coming-to-elementary-os/boot-password.jpg)
<figcaption markdown="1">
elementary OS 6 startup on a [Star Labs](https://starlabs.systems) device
</figcaption>
</figure>

elementary OS 6 also includes improved performance across the desktop and apps thanks in part to our work on experimental Pinebook Pro and Raspberry Pi builds. With OS 6, we've improved process communication between desktop components and reduced disk reads and writes, which is especially evident on lower-clocked processors and slower storage mediums like spinning hard drives and SD cards. These performance improvements benefit the entire range of devices on which elementary OS runs.

### Accessibility

Another element of our approach to elementary OS is to ensure it's as inclusive as possible—meaning it's able to be used comfortably by anyone, including those with temporary, chronic, or permanent accessibility needs. As such, we've focused in on our _Accessibility Features are Just Features_ efforts in OS 6.

<figure class="card" markdown="1">
![Screenshot of the Universal Access indicator](/images/{{ page.slug }}/a11y-indicator.png){: width="750" height="343"}
<figcaption>Universal Access indicator</figcaption>
</figure>

elementary OS 6 includes a new Universal Access indicator to expose toggles for features like the screen reader, on-screen keyboard, dwell click, etc. so they're easy to turn on or off as needed. We've also improved usability throughout elementary OS with new features and better defaults.

The redesigned and rewritten system stylesheet ensures much higher contrast by default across the desktop and native apps—including those from developers on AppCenter; this can help people with vision needs, those with unconventional hardware setups like projectors or older, low-contrast displays, and even just anyone using their device in a bright environment like direct sunlight. 

Expanded text size scaling and a new dyslexia-friendly text option can help those with specific vision or reading needs. In addition, the new system stylesheet now uses the text size to smartly scale the rest of the UI, making it a real option for handling display resolutions that don't fit nicely into the integer scaling buckets—all while keeping the UI pixel-perfect and crisp.

The new dark style preference is a visual treat for those who prefer it, but it can also help those with light sensitivity and migraines be able to more comfortably use elementary OS. The new Slate accent color can reduce the effect of distracting colors for those with specific learning or attention needs. And by exposing keyboard shortcuts more consistently in context menus and tooltips throughout the entire desktop in OS 6, we're helping newer users, keyboard warriors, and those with limited mobility learn how to accomplish their tasks without reaching for the mouse or touchpad.

Multi-touch gestures are a new slick way you can navigate the OS on a touchpad or touch screen, but also improve accessibility: previously keyboard-only features like desktop zoom are now able to be used solely on a touchpad or touch screen with a three- or four-finger pinch to zoom.

We've also improved our iconography in elementary OS to improve accessibility and inclusivity. Consistently rounded shapes across arrows, media controls, and more are more friendly and inviting. Depictions of people in icons are now more generic and gender-neutral. And several color icons have been improved for contrast and visibility across a variety of backgrounds, especially when used with the new dark style.

## …and tons more

We've kept with the above themes throughout all the updates to elementary OS. Here's just a bit more of what's new in OS 6:

---

## Settings

### switchboard 6.0.0 Released

- Add multi-touch navigation gestures
- Better support smaller displays
- Remove old GNOME Control Center compatibility layer
- Stability and performance improvements

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

### switchboard-plug-a11y 2.3.0 Released

- Add a switch to show the indicator in the Panel
- Point out how to find other accessibility features in System Settings

## Desktop/first-run?

### Gala 6.0.0 Released

Improvements:

- Show window titles in multitasking view
- Close the Alt + Tab switcher by pressing Esc without releasing Alt
- Increase maximum zoom level and provide feedback when unable to zoom
- Show a context menu when secondary clicking the background
- New Dwell Click and Locate Pointer animations
- Add Take Screenshot to window context menu
- Always play shutter sound when taking screenshots
- Minor visual improvements
- HiDPI fixes

### sideload 6.0.0 Released

- Control notifications in System Settings
- Offer to trash Flatpak files after installing
- Support dark style
- Support Flatpak bundle files
- Fix crashes on installation failure
- Link to System Settings → Applications → Permissions

### screenshot 6.0.0 Released

- Support the dark style
- Drag and Drop the preview image from the save dialog
- Drag to move the window from anywhere
- Show details for errors if they occur

## Panel

### applications-menu 2.8.0 Released

Minor updates

- Sort app actions above AppCenter search
- Always hide Terminal-based programs
- Remove document viewer from block list
- Support fractions without leading number in calculator
- Show overlay key in tooltip when set

### wingpanel-indicator-network 2.3.0 Released

- Fix VPN spinning after connecting
- Improve detecting network encryption type
- Ellipsize long network names
- Show tooltip on hover

## Little Stuff

## Look & Feel

### icons 6.0.0 Released

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

## Developers

### granite 6.1.0 Released

Additions:

- `TRANSITION_DURATION_IN_PLACE` for consistent in-place widget transformations

Other Changes:

- `accel_to_string` handles accel markup without modifiers or that are only modifiers

---

## Release Notes

For detailed release notes organized by version number of each individual component, you can always view our [public Releases site](https://releases.elementary.io).

## Thank You

elementary OS is made in large part by volunteer contributors from around the world. For OS 6 specifically, we'd like to thank the following individuals for their substantial contributions.

- [Corentin Noël](https://github.com/tintou) – OS patches, Files, Flatpak, Camera, and more
- [David Hewitt](https://github.com/sponsors/davidmhewitt) – OS build system, Settings Daemon, AppCenter, Installer, and more
- [Igor Montagner](https://github.com/igordsm) – Camera and more
- [Jeremy Wootten](https://github.com/jeremypw) – Files, Code, Calculator, and more
- [José Expósito](https://github.com/sponsors/joseexposito) – Multi-touch, window management, Screenshot, and more
- [Marco Betschart](https://github.com/sponsors/marbetschar) – Online Accounts, Mail, Tasks
- [Marius Meisenzahl](https://github.com/sponsors/meisenzahl) – Flatpak permissions, scheduled dark style, firmware updates, accent color, and more
- [Sean Davis](https://github.com/sponsors/bluesabre) – Notifications, Sound indicator

Many of these contributors are on GitHub Sponsors, meaning you can show your appreciation and fund their ongoing work by sponsoring them directly.

To all of our sponsors and customers: thank you! Your contributions fund our ongoing work and make it all possible. If you’d like to help build and improve elementary OS, don’t hesitate to <a href="https://elementary.io/get-involved" onclick="plausible('Link: Get Involved')">Get Involved</a>.

[elementary.io]: https://elementary.io
