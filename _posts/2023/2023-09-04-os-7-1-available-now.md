---
title: 
description: 
author: danrabbit
image: /images/os-7-1-available-now/card.png

tags:
  - horus
  - updates
---

How many bugs squashed since 7.0?

Major themes:
* Accessibility
* Office Productivity
* Settings & Personalization

# Installer & Initial Setup

Navigation gestures
Screen reader

https://github.com/elementary/initial-setup/releases/tag/6.3.0

# Onboarding

A fresh version of Onboarding has been released with several redesigned pages including a fancy dynamic icon featuring the release wallpaper on the Welcome page, a much more prominent explanation of Sideloading, some new icons, and bolder typography.

<figure class="half" markdown="1">
![Welcome view of Onboarding](/images/{{ page.slug }}/onboarding-welcome.png){
![Apps view of Onboarding](/images/{{ page.slug }}/onboarding-apps.png)
![Early Access view of Onboarding](/images/{{ page.slug }}/onboarding-earlyaccess.png)
![Guest Session view of Onboarding](/images/{{ page.slug }}/onboarding-guest.png)
<figcaption markdown="1">
Onboarding features bolder typography, colorful icons, and a more prominent explanation of Sideloading
</figcaption>
</figure>

Plus, it has better handling for Early Access builds, and Onboarding now handles the Guest account warning as well.

https://github.com/elementary/onboarding/releases/tag/7.2.0

## Feedback

The Feedback app has been ported to GTK 4 and it now features search! This should make it much speedier to send feedback when something unexpected happens.

<figure markdown="1">
![Feedback](/images/{{ page.slug }}/feedback.png){: width="570" height="621"}
<figcaption markdown="1">
The Feedback app now features search
</figcaption>
</figure>

The feedback app is our way to stay connected with you and address any issues you come across, so please make sure to make use of it. The issues that we send fixes for every month come directly from folks who make use of this app.

## AppCenter

As we work towards our continual goal of better supporting alternative app stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. This month we've rolled out a new set of app sandbox warnings to help you better assess risk when installing apps. AppCenter will now inform you if an app can can read your location without asking first, if it can access system folders or your home folder, if it can read and write system settings, or if it could possibly escape the sandbox altogether and gain advanced permissions. For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent. Expect more of these types of warnings to roll out in the future!

<figure markdown="1">
![AppCenter](/images/{{ page.slug }}/appcenter-permissions.png){: width="1198" height="901"}
<figcaption markdown="1">
AppCenter now warns about advanced Flatpak sandbox permissions
</figcaption>
</figure>

AppInfo views have also been reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops. Plus, we no longer split out apps from alt stores into a separate header in category views, and a potential crash when adding alt stores has been fixed thanks to [Marius](https://github.com/meisenzahl)

AppCenter received a new Flatpak Repair feature thanks to [Marius](https://github.com/meisenzahl) which fixes an issue where some Flatpak runtimes could not be installed. Plus the updates page now shows a small message when everything is up-to-date, including the last time that AppCenter checked for updates.

## Sideload

Since sideloading is an expected and important part of installing apps on elementary OS, we've made a couple of changes to help you stay informed and be in control. Instead of describing sideloaded apps as "Untrusted", we've updated interface copy to instead ask for your trust. Additionally, we now show some basic feedback about the kinds of broad system permissions that a sideloaded app may request. This will likely get more fine-grained in the future, but for now we can warn about apps that request advanced permissions and let you know when an app is more tightly sandboxed.

<figure markdown="1">
![Files](/images/{{ page.slug }}/sideload.png){: width="502" height="334"}
<figcaption markdown="1">
Sideload now shows recommendations regarding sandbox permissions
</figcaption>
</figure>

[Leo](https://github.com/lenemter) fixed some visual glitches in Sideload and made sure the "Open" button can be activated when pressing <kbd>Enter</kbd> after installing.

# Mail

Mail does a better job handling newly added online accounts and includes fixes for a couple of potential crashes, plus a ton of code cleaning under the hood and even a few performance improvements. The composer now always opens in a separate, non-modal window making it much easier to reference a message you're replying to or manage multiple drafts at the same time.

<figure class="half" markdown="1">
![Mail](/images/{{ page.slug }}/mail.png)
![Composer Window](/images/{{ page.slug }}/mail-compose.png)
<figcaption markdown="1">
Subtle design changes in Mail include floating headers and a flatter compose window
</figcaption>
</figure>

It also features quite a few more keyboard shortcuts for text formatting, adding attachments, etc. You might also appreciate some subtle design tweaks like placing the conversation list filter next to the search bar or how headers now appear to float over scrolled content. Major thanks goes to [Leonhard](https://github.com/leolost2605) for his hard work on this release.

This release of Mail was really a labor of love from [Leonhard](https://github.com/leolost2605) and includes several new features and quality of life improvements. It now also uses the File Chooser Portal when selecting attachments and the Background & Autostart portal—[as previously teased](https://blog.elementary.io/updates-for-june-2023)—so you can control its autostart behavior in System Settings → Applications → Startup. Mail also does a better job handling changes in your internet connection, and can check messages in the background even when not autostarted.

<figure markdown="1">
![Mail](/images/{{ page.slug }}/mail.png){: width="1039" height="765"}
</figure>

In the sidebar, you'll notice that special folders like "Archive" and "Spam" are better detected and appear at the top level, even for accounts like Gmail that used to hide them as subfolders. You can now also rename folders by secondary-clicking on them and selecting "Rename Folder". An issue was resolved where some accounts with no archive folder displayed their inbox in the Archive for all mailboxes. And you'll notice that Mail's primary menu is now in the bottom right corner of the sidebar. Plus, performance has been improved when switching between folders.

In the conversation list, you can now use a multi-touch swipe or click-and-drag left or right to quickly archive or trash a conversation. In the messages list, there's a new "Move conversation" menu that includes search, and you'll notice that archiving and moving messages can now be undone. Mail now does a better job of calculating message height to avoid extra scroll bars, and a handy infobar is shown when a message includes a calendar invite.

<figure class="half" markdown="1">
![Composing a new message in Mail](/images/{{ page.slug }}/mail-compose.png){: width="744" height="564"}
![Creating signatures in Mail](/images/{{ page.slug }}/mail-signatures.png){: width="564" height="364"}
<figcaption markdown="1">
Mail now supports inline images and multiple saved signatures
</figcaption>
</figure>

When composing a message, you can now add images inline and you can include attachments in forwarded messages. Plus this release brings support for signatures. You can create as many signatures as you'd like and assign them as the defaults for accounts as needed. The new "Insert signature…" menu makes it easy to swap between any of your saved signatures when composing.

Early in the month we made a release of Mail that fixed a notorious and pervasive crash thanks to [@leolost2605](https://github.com/leolost2605). This release also contained a fixed for creating links that include a `%` symbol. Look forward to future releases featuring more of their work!

## Calendar & Tasks

Calendar now uses the File Chooser Portal when importing and exporting calendar files, animations when switching months have been updated to match button directions, and it now uses your system accent color instead of its own. An issue in tasks where some tasks could become duplicated was resolved, as well as a small visual issue in dark mode. Both Calendar & Tasks now use the Background & Autostart portal as well, and their autostart behavior can be controlled in System Settings → Applications → Startup. Shoutouts to [Gustavo](https://github.com/marukesu), [Leonhard](https://github.com/leolost2605), and [Claudio](https://github.com/Claudio-code) for their work on office productivity apps this month.

## Files

[Jeremy](https://github.com/jeremypw) made a sizable bug fix release of Files including several fixes related to selections and the overlay bar as well as a couple of reported regressions, fixes related to git emblems, and a crash fix.

The headlining feature of this Files release is the new app menu in the headerbar. [Jeremy](https://github.com/jeremypw) put together this menu to better improve discoverability for features like zoom and undo/redo as well as to clean up folder context menus. The Undo and Redo buttons include tooltips showing what operation will be performed before you click them and we also updated the description for the double-click setting to make it more clear.

<figure markdown="1">
![Files](/images/{{ page.slug }}/files.png){: width="1064" height="744"}
<figcaption markdown="1">
Files now has an app menu with app-wide settings and features
</figcaption>
</figure>

We also fixed a number of reported issues including some off click behavior above and below text in the list view, case sensitivity in file path completion, and issues with MTP and PTP devices that have a colon in their name. Plus we reworked how the File Chooser handles typing focus when saving.

A long requested feature, this month Bulk Rename lands in Files thanks to [Jeremy](https://github.com/jeremypw). With this feature, you can select a number of files, secondary-click, and select "Rename…" to get an advanced bulk renaming dialog. This is an especially useful feature if you're working with a large collection of photos or spreadsheets or other kinds of files that you may want to rename by creation date or using another sequence or when you have to format a large number of files the same way. We're looking forward to your feedback on this feature and improving it to fit your advanced file management needs!

<figure markdown="1">
![Files bulk rename](/images/{{ page.slug }}/files-rename.png){: width="990" height="516"}
<figcaption markdown="1">
You can now rename a large selection of files at once
</figcaption>
</figure>

He also fixed several reported issues in this release related to folder sizes, file creation dates, temporary and duplicate files, and even snuck in some performance improvements. Also, the storage level bar in Properties dialogs will now change color depending on how full a drive is.

<figure markdown="1">
![Bluetooth sharing](/images/{{ page.slug }}/bluetooth-sharing.png){: width="472" height="572"}
<figcaption markdown="1">
You can share files via Bluetooth from the secondary-click menu
</figcaption>
</figure>

Plus, thanks to a joint effort between [Jeremy](https://github.com/jeremypw) and [Torikul](https://github.com/torikulhabib), you can now share files via Bluetooth. A new Bluetooth transfer dialog is available by secondary-clicking a file or selection of files and selecting "Send Files via Bluetooth" from the menu.

[Jeremy](https://github.com/jeremypw) fixed an issue in Files where sometimes folder contents were incorrect until the folder was refreshed.

This release of Files sports a new Tab Bar powered by LibHandy with improved animations, smoother drag-and-drop, and reorganized tab context menus, bringing it more in line with Web. [Jeremy](https://github.com/jeremypw) has also rewritten the way color tags are stored using extended file attributes instead of a database; This means tags should be better preserved when restoring from the Trash for example and you've no need to fear because Files will automatically update your tags to use the new system in the background. He also solved several issues around refreshing and temporary files as well as making sure that tab history is properly preserved when opening Files from another app.

# Music

Music can now accept Drag and Drop of whole folders, thanks to [Jeremy](https://github.com/jeremypw), and you can secondary click on a folder in Files and open it with Music thanks to [Aitor](https://github.com/aitor-gomila). Plus it's been updated to the latest Flatpak platform which fixes issues with certain animations.

## Videos

https://github.com/elementary/videos/releases/tag/3.0.0

We've been hard at work getting Videos ready for GTK 4 and one of the steps along the way was getting rid of Clutter—big "C"—which has lead to a massive rework of the app's internals. The code base is much cleaner and clearer and should be more reliable and performant. This release still uses GTK 3, but look forward to GTK 4 in the next release.

<figure markdown="1">
![Videos](/images/{{ page.slug }}/videos.png){: width="1069" height="747"}
<figcaption markdown="1">
Videos is a wee bit flatter
</figcaption>
</figure>

For now you can expect improved playback position saving, a flatter app appearance in the welcome screen and library, smoother navigation, and in-app notifications when adding items to the playlist. Major shoutouts to [Leonhard](https://github.com/leolost2605) here.

## Web

The latest GNOME Web 44.2 has now been ported to Gtk 4 and features much improved performance and web standards compatibility, plus a new saved passwords popover. With Firefox sync, web apps, and performance that matches major mainstream competitors, there's never been a better time to try this community-made web browser.

The latest version of Web fixes a crash in the bookmarks popover, improves the reliability of creating web apps, and has a fix related to local storage access requests.

# Calculator

Calculator now follows keyboard shortcuts for copy and paste, even when the main text entry isn't focused, thanks to [Leo](https://github.com/lenemter)! It will no longer preserve extra white space on the right side of the window when used with alternative window button layouts. And Calculator will now always use the elementary stylesheet and icons, even when run on a different operating system, to prevent breakage related to missing assets.

## Code

[Jeremy](https://github.com/jeremypw) has been working diligently on this release of Code which closes more than 20 reported issues and brings plenty of improvements to search. Code now does a better job handling file saving and preventing data loss when files can't be written to their original location. Some busy infobars are now dialogs, and we avoid showing too many aggressive warnings about file saving. And you can now optionally try to continue loading files that contain unknown characters or corrupted content.

Search options are now all available from a new menu, there's now a "match whole words" option, and your search settings are now saved between sessions. The search entry also provides visual feedback when no results are found. We do a better job deciding which string to search if you have both a selection and text in the search entry, and make sure that the "Replace" and "Replace All" buttons are enabled and disabled more accurately. And an issue that prevented global search from working on startup was fixed.

<figure markdown="1">
![Code](/images/{{ page.slug }}/code.png)
<figcaption markdown="1">
Code has a new search options menu
</figcaption>
</figure>

In the sidebar, folders that don't contain text files can now be expanded properly, and Code does a better job making sure sidebar focus updates correctly when tabs are closed. The tab width menu has been reworked quite a bit to more accurately prioritize between your global defaults, per document settings, and editorconfig file. An issue that caused an incorrect column number in the line number menu was fixed.

The Vala symbols outline now correctly matches Code when the style changes after startup, and we fixed issues with styling when no documents are open. An issue that caused excessive reads and writes to settings has been fixed. Plus, you can now switch tabs with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>PageUp</kbd>/<kbd>PageDown</kbd> thanks to [Stan](https://github.com/stan-janssen)

## Terminal

This release was extremely collaborative with quite a few commit authors. It contains fixes related to tab switching shortcuts and makes sure that context menus are updated when activated with the menu key thanks to [Lasne](https://github.com/Faelian) and [Ryo](https://github.com/ryonakano), respectively. [Stan](https://github.com/stan-janssen) also resolved an issue where shortcuts conflicted with some command line apps and added a new option to start Terminal hidden. [Jeremy](https://github.com/jeremypw) also fixed an issue with `#` characters in URLs. Finally, thanks to [Gustavo](https://github.com/marukesu) and [Corentin](https://github.com/tintou) for their work on unit testing and code cleanup in this release.

# System Settings

The latest release of Desktop settings includes some new options for switching workspaces via hotcorners as well as a new feature to dim wallpapers in dark mode thanks to [Leo](https://github.com/lenemter)! You'll also notice that the setting for disabling animations has moved to the "Appearance" tab and has been renamed to "Reduce Motion".

<figure class="constrained" markdown="1">
![Appearance Settings](/images/{{ page.slug }}/settings-appearance.png) {: width="1101" height="769"}
<figcaption markdown="1">
The "Reduce Motion" setting has moved to the "Appearance tab"
</figcaption>
</figure>

A new version of Locale settings has also been released that prevents Fcitx 5 from being automatically pulled in with some languages and fixes a potential issue with acquiring permissions to set system-wide locale settings.

As part of their aforementioned work, [Gustavo](https://github.com/marukesu) updated Startup settings to show apps that use the Background &amp; Autostart Portal and we made quite a few changes to this view to bring it in line with modern design patterns and ensure that it was more responsive for large and small displays. We also updated Default apps settings and did quite a bit of code cleanup here. And thanks to [Leo](https://github.com/lenemter) the "Reset to Defaults" button on the Permissions page is now disabled when permissions are already at their defaults, plus he improved screen reader names for several settings while here.

<figure class="half" markdown="1">
![Defaults Settings](/images/{{ page.slug }}/settings-defaults.png){: width="1024" height="720"}
![Startup Settings](/images/{{ page.slug }}/settings-startup.png){: width="1024" height="720"}
<figcaption markdown="1">
Startup and Defaults settings were both redesigned to be more responsive for large and small displays
</figcaption>
</figure>

We're also introducing a new set of display filters, designed to assist folks with color deficiency issues. This is a very common disability with 1 in 12 men experiencing color deficiency and some folks developing color deficiency as they age. Major shoutouts to [Leo](https://github.com/lenemter) for implementing this feature in our window manager and to [@G-dH](https://github.com/G-dH) for developing [the GNOME Shell extension](https://github.com/G-dH/gnome-colorblind-filters) that we modeled our feature off of. If this is a feature that you're looking forward to using, please consider [buying them a coffee](https://buymeacoffee.com/georgdh).

<figure class="card quarter" markdown="1">
![Default colors](/images/{{ page.slug }}/color-default.png){: width="1920" height="1080"}
![Protanopia Filter](/images/{{ page.slug }}/color-protanopia.png){: width="1920" height="1080"}
![Protanopia High Contrast Filter](/images/{{ page.slug }}/color-protanopia-hc.png){: width="1920" height="1080"}
![Deuteranopia Filter](/images/{{ page.slug }}/color-deuteranopia.png){: width="1920" height="1080"}
![Deuteranopia Hight Contrast Filter](/images/{{ page.slug }}/color-deuteranopia-hc.png){: width="1920" height="1080"}
![Tritanopia Filter](/images/{{ page.slug }}/color-tritanopia.png){: width="1920" height="1080"}
![Grayscale Filter](/images/{{ page.slug }}/color-grayscale.png){: width="1920" height="1080"}
<figcaption>A number of new display filters are available to assist with color deficiency</figcaption>
</figure>

Additionally, we're now shipping a grayscale filter which can help avoid distractions or alleviate screen addiction and you can now make the display much warmer when using Night Light. You may also notice a small redesign of Night Light settings for responsiveness. Finally, there should be more accurate display resolution options available thanks to [Vishal](https://github.com/vjr).

<figure class="half" markdown="1">
![Night Light Settings](/images/{{ page.slug }}/settings-nightlight.png){: width="990" height="686"}
![Filters Settings](/images/{{ page.slug }}/settings-filters.png){: width="990" height="686"}
<figcaption markdown="1">
Nightlight settings have been slightly redesigned and Filters are available as a new tab in Display Settings
</figcaption>
</figure>

Sound Settings got a bit of a redesign for improved responsiveness on small and large displays and you may notice some improved description labels. Plus, [Leo](https://github.com/lenemter) fixed a reported crash.

<figure class="half" markdown="1">
![Sound Output Settings](/images/{{ page.slug }}/sound-output.png){: width="1198" height="686"}
![Sound Input Settings](/images/{{ page.slug }}/sound-input.png){: width="1198" height="686"}
<figcaption markdown="1">
Sound settings slightly redesigned for small and large displays
</figcaption>
</figure>

The Dock &amp; Panel tab of Desktop settings also received a responsive redesign with added description labels for some settings. Additionally, checkboxes for extra indicators like the Accessibility indicator and the Capslock and Numlock indicators are now centrally located here. Plus [Leo](https://github.com/lenemter) fixed an issue where wallpapers might not get removed when quickly closing System Settings.

<figure markdown="1">
![System Settings → Desktop → Dock &amp; Panel](/images/{{ page.slug }}/settings-dock-panel.png){: width="1198" height="686"}
<figcaption markdown="1">
Dock &amp; Panel now includes optional panel indicator settings
</figcaption>
</figure>

The Behavior tab of Keyboard settings got a major update with the additional of several new settings for things like Bounce, Slow, and Sticky keys. Slider values are now shown on drag instead of in a separate widget. Plus, app developers can now link directly to custom shortcuts settings thanks again to [Leo](https://github.com/lenemter).

<figure markdown="1">
![System Settings → Keyboard → Behavior](/images/{{ page.slug }}/keyboard-behavior.png){: width="1198" height="686"}
<figcaption markdown="1">
Keyboard Behavior now includes Bounce, Slow, and Sticky keys
</figcaption>
</figure>

In Security &amp; Privacy Settings, you now have the option to automatically clean up Screenshot files as part of Housekeeping thanks to [Josip](https://github.com/Antolius). And we now make sure not to show Location settings for apps that have been uninstalled.

There's also a new version of Online Accounts settings thanks to [Leonhard](https://github.com/leolost2605) which fixes a freeze when the server doesn't respond while adding an IMAP account, and improves support for special folders like Archive and Sent folders. Online Accounts settings was updated with a fix for setting the correct SMTP username when configuring IMAP accounts, thanks to [Stan](https://github.com/stan-janssen). And, [Leo](https://github.com/lenemter) made sure the icons there for Mail and Tasks were updated to their latest versions.

Finally, the Settings Daemon will now check for and notify of Firmware updates when they're available thanks to [Marius](https://github.com/meisenzahl) and we support Accent Colors on the Settings Portal thanks to [Alice](https://github.com/alice-mkh)

A new version of Security &amp; Privacy settings has been released that now supports the Location portal. This is a more secure method for apps to request access to location services and is the latest FreeDesktop.org standard for doing so. If you've had trouble with sideloaded apps accessing location services before, this change will most likely fix that issue. You can adjust location settings in System Settings → Security &amp; Privacy → Location Services. If the main switch here is turned off, apps will not be allowed to even ask for permission, so make sure it's turned on if you are using apps that make use of location data.

A couple of keyboard settings moved around, but were not removed! On-screen keyboard settings are now on the Behavior tab and panel indicator settings are now available in Desktop → Dock &amp; Panel. [Ryo](https://github.com/ryonakano) fixed an issue that prevented the progress dialog from being shown when installing input method engines, as well as adding multitouch gesture support for navigating backwards through the installation steps, and made sure the <kbd>PrintScreen</kbd> key can be used for keyboard shortcuts. [Leo](https://github.com/lenemter) added the "Cycle Windows of application" and "Cycle Windows of application backwards" shortcuts, fixed an issue with input method switching, and guarded against a potential crasher.

In applications settings, we fixed an issue that caused no default music player to be set on new accounts, and added search to the Permissions tab, thanks to [Leonhard](https://github.com/leolost2605).

## Panel

As part of the aforementioned Bluetooth file transfer feature, you can see ongoing transfers in the Bluetooth indicator. And thanks to [Stan](https://github.com/stan-janssen), Bluetooth devices will now use any custom device names you've set up before falling back to more generic device names.

We now do a better job making sure notification bubbles you've dismissed with a swipe or the close button don't end up in the Notifications indicator, and the number of missed notifications in the tooltip should be more accurate, thanks again to [Jeremy](https://github.com/jeremypw). [Leo](https://github.com/lenemter) improved support for notifications that contain markup and [Leonhard](https://github.com/leolost2605) fixed the change in indicator width when all notifications have been cleared.

Plus, we updated some icons in the Bluetooth, Night Light, and Notifications indicators to be more consistent.

The Sound indicator was updated to use circle buttons and should no longer change size when skipping tracks. Muting should no longer affect monitor sources thanks to [Gran](https://github.com/GranPC), and microphone icons have been subtly updated. Plus, [Leo](https://github.com/lenemter) made sure the Accessibility indicator shows the correct text size on startup.

The network indicator has been getting some major design attention and now offers a much better experience for using VPNs. You'll notice that most options now appear as circular toggle buttons with icons instead of a list of switches. This new design both saves space on devices with complex network configurations and shows the status of your various connections much clearer, including intermediate and error states. In the case of VPNs, you can now also activate multiple connections at once.

<figure class="card" markdown="1">
![Network Indicator](/images/{{ page.slug }}/network-indicator.png)
<figcaption markdown="1">
The Network Indicator has been redesigned with better VPN controls and Airplane Mode
</figcaption>
</figure>

We've also added quick access to toggling Airplane Mode, including a middle-click action on the indicator icon. Plus, we're now using a feature of Network Manager to automatically get better device names so you'll rarely see long and cryptic device names any longer. And you may notice some subtly improved icons like a slightly larger Wi-Fi icon with rounded edges.

After receiving quite a bit of feedback about the panel appearing broken when folks modify the system visual assets, the panel now always uses the elementary stylesheet and icons to prevent style issues. You can also now close panel indicators with <kbd>Esc</kbd> and [Leo](https://github.com/lenemter) fixed an issue that caused indicators to re-animate if an indicator was updated or removed.

The Power indicator now always uses hours as its largest unit, for example it will say "26 hours remaining" instead of "1 day remaining" and we resolved an issue that caused battery level icons to sometimes be inaccurate. Thanks to [Leo](https://github.com/lenemter) and [Vishal](https://github.com/vjr).

## Login &amp; Lock Screen

Meanwhile, [Leo](https://github.com/lenemter) has recently made it his mission to respect all of your system settings and improve accessibility on the Login &amp; Lock screen. It now does a better job matching your mouse, keyboard, and touchpad settings, including improved keyboard layout handling. Your chosen accent color is now used everywhere—not just on your login card—and it now handles solid color wallpapers. Your text size and font settings, pointer size settings, cursor blink settings, Night Light settings and more are all now respected as well. Plus, the ability to reveal the pointer is now available, the Screen Reader can be enabled with a keyboard shortcut, and it does a better job remembering your Screen Reader settings.

In addition to all of that, an issue that prevented cards from being selected when clicked in certain areas has now been fixed, as well as potential issues with dialogs that use Portals, potential issues with multi-display setups, and an issue where settings would be reset when incorrect credentials were entered. Plus you'll also notice that the Login &amp; Lock Screen now has subtly rounded corners that match the logged in session.

## Window Management

This release of our window manager contains over a dozen fixes for reported issues thanks to [Leo](https://github.com/lenemter)'s hard work. This includes things like performance improvements and smoother animations, fixes for issues with shadows, improved ability to optionally disable animations, better handling of keyboard shortcuts in Multitasking View, and lots of code cleanup. Plus a fix that avoids accidentally closing windows when using three-finger multi-touch gestures. I recommend reading the [full release notes](https://github.com/elementary/gala/releases/tag/7.0.1) because this is a big one!

This is another great bugfix release for Gala with major thanks to [Leo](https://github.com/lenemter). Some of the highlights include fixes for notification windows—including showing them in Multitasking View, fixes for issues with keyboard shortcuts, fixes that prevent misclicks and accidentally triggering actions, performance improvements, fixes for visual glitches, and more. This is another great release to read the [full release notes](https://github.com/elementary/gala/releases/tag/7.0.2) since it closes another dozen reported issues.

We had yet another great release of our window manager, Gala, this month. This release brings the total number of fixed reported issues since OS 7 in this component alone to nearly 40! Highlights from this release include adding the keyboard shortcut <kbd>Alt</kbd> + <kbd>~</kbd> for switching between windows of the same app, navigating with the arrow keys while holding down <kbd>Alt</kbd> + <kbd>Tab</kbd>, and several more animations now respect your preference to disable them. Plus, the team has been working hard to prepare for Mutter 44 which will bring fractional and per-display scaling support on Wayland, so look forward to seeing that in a future version of elementary OS. Thanks again to [Corentin](https://github.com/tintou), [David](https://github.com/davidmhewitt), and [Leo](https://github.com/lenemter) for all of their work here.

[Leo](https://github.com/lenemter) fixed an issue where Picture-in-Picture windows could become unintentionally hidden and made sure parent windows of dialogs are dimmed and undimmed more accurately.

[Leo] fixed an issue where sometimes parent windows wouldn't un-dim after closing dialogs, and made sure Picture-in-Picture windows update their visibility properly when switching workspaces.

https://github.com/elementary/gala/releases/tag/7.1.2

 Another half dozen bug fixes landed in our Window Manager thanks to [Leo](https://github.com/lenemter), including several related to workspaces. 

## Portals

Another big part of our consent story with apps are Portals. Portals keep apps isolated from your private data and ensure that apps ask before making changes to the system or using features that could become intrusive. This month [Leonhard](https://github.com/leolost2605) and [Gustavo](https://github.com/marukesu) implemented the Background &amp; Autostart Portal which alerts you when apps are running in the background and makes sure that apps ask your permission before they can automatically start up when you turn on your device. There's still a good amount of work to do on our background apps story, but this sets the foundation.

And thanks to the hard work of [Marco](https://github.com/marbetschar) and [Gustavo](https://github.com/Marukesu) our Portals—things like the app chooser and access dialogs—have now been ported to GTK 4!

[Leonhard](https://github.com/leolost2605) fixed an issue where apps using the new Background &amp; Autostart portal might repeatedly try to add themselves to autostart even when you'd previously disabled them.

## Notifications

Leo also removed the intrusive "Automatic Suspend" notifications. Gustavo made sure critical notifications are still sent even when Do Not Disturb is active and contributed quite a bit of code cleanup in the notifications server. And new contributor [Sean](https://github.com/SuperRiderTH) made a fix for the option to disable sounds from notifications sent by apps that don't properly identify themselves.

Also [Gustavo](https://github.com/marukesu) and [Leonhard](https://github.com/leolost2605) fixed a couple issues related to Notification close behavior.

## And More

Linux 6.2, Ubuntu HWE

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.
