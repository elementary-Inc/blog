---
title: elementary OS 7.1 Available Now
description: 
author: danrabbit
image: /images/os-7-1-available-now/card.png

tags:
  - horus
  - updates
---

Today we're proud to announce that OS 7.1 is available to download now and shipping soon on several high-quality computers. This release represents the sum of our work over the last several months as a single major update to the OS 7 series and includes [all of the monthly OS updates][updates] we've detailed since the OS 7 release.

<figure class="card" markdown="1">
![elementary OS 7.1](/images/{{ page.slug }}/hero.png)
</figure>

With OS 7.1, we've focused in on:

- Accessibility
- Office Productivity
- Settings & Personalization
- Privacy & Security
- Consent & Control

To get elementary OS 7.1 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

# Addressing Your Feedback

One of the greatest advantages we have developing elementary OS in the open as compared to proprietary operating systems is the ability to gather your feedback and for developers to directly engage with you to solve issues and create new features. Combined with our monthly release cadence, the Feedback app creates a tight loop where you can start a report, see development happen transparently, and receive updates quickly. With the release of OS 7, we made sure that the Feedback app was accessible directly from the applications menu, launched instantly, and covered more system components. In OS 7.1, we've added search and we've now ported the app to GTK 4—the latest version of our app toolkit—for improved performance and smoothness. This should make it even speedier to send feedback when something unexpected happens.

<figure markdown="1">
![Feedback](/images/{{ page.slug }}/feedback.png){: width="570" height="621"}
<figcaption markdown="1">
The Feedback app now features search
</figcaption>
</figure>

Since the release of OS 7 at the end of January, we've sent out free updates that address over 200 reports—that's one report addressed every day in addition to our regular planned work.


# Portals

Portals provide a safe and consensual way for apps to interact with operating system features and make sure that they only get access to the data you want them to. One of the ways that apps may become intrusive is by automatically starting themselves or running in the background without your permission. In OS 7.1, we now provide the Background &amp; Autostart Portal which alerts you when apps are running in the background and makes sure that apps ask your permission before they can automatically start up when you turn on your device.

Calendar, Mail, and Tasks now all use the Background & Autostart portal, and their autostart behavior can be controlled along with other apps in System Settings → Applications → Startup.





Calendar and Mail have been updated to use the File Chooser Portal for things like selecting attachments or importing and exporting calendar files.

And thanks to the hard work of [Marco](https://github.com/marbetschar) and [Gustavo](https://github.com/Marukesu) our Portals—things like the app chooser and access dialogs—have now been ported to GTK 4!


A new version of Security &amp; Privacy settings has been released that now supports the Location portal. This is a more secure method for apps to request access to location services and is the latest FreeDesktop.org standard for doing so. If you've had trouble with sideloaded apps accessing location services before, this change will most likely fix that issue. You can adjust location settings in System Settings → Security &amp; Privacy → Location Services. If the main switch here is turned off, apps will not be allowed to even ask for permission, so make sure it's turned on if you are using apps that make use of location data.



## Installer & Initial Setup

We've received feedback from folks with vision-related disabilities that a huge barrier for them when considering an Open Source operating system is that they often need help to get it installed. Now, when you boot into the install media for elementary OS, we automatically play an audio prompt letting you know the keyboard shortcut for turning on the screen reader. And the same audio prompt is available during Initial Setup, so whether you're buying a computer pre-installed with elementary OS or installing it on your existing computer, you can choose an Open Source operating system and remain independent.

Some computers contain hardware devices that require additional, proprietary drivers to function properly. This previously made installing elementary OS difficult when wireless network drivers or video card drivers were unavailable. We now provide an option during installation to include these proprietary drivers so that your devices function properly.

Navigation gestures

## Onboarding

Onboarding is the most personal part of getting started with elementary OS, where you choose how you'll experience your individual account and are introduced to core features of the operating system.

With Flatpak, you have access to an incredibly wide selection of apps and a growing number of alternative app stores. Unlike on mainstream proprietary operating systems, installing apps via Sideload and accessing alternative app stores are important features of elementary OS. So, when we're introducing people to AppCenter—the pay-what-you-can app store with apps made specifically for elementary OS—we also now much more prominently introduce them to Sideload and even feature a prominent link to the most popular Flatpak-powered app store: Flathub.

Housekeeping is a feature designed to free up storage and protect your privacy by automatically deleting old files. You can now choose to automatically clean up the Trash, Downloads, Screenshots, and temporary operating system files on a schedule of your choosing.

Onboarding now also handles providing information about the temporary Guest account.






A fresh version of Onboarding has been released with several redesigned pages including a fancy dynamic icon featuring the release wallpaper on the Welcome page, some new icons, and bolder typography.

StyleView: use actual background when available












## AppCenter

As we work towards our continual goal of better supporting alternative app stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. In elementary OS, the supported app packaging format is Flatpak which gives us several tools to that end, including the ability to report back to you when apps have advanced access that could leave you vulnerable. In OS 7.1, AppCenter will now inform you if an app can can read your location without asking first, if it can access system folders or your home folder, if it can read and write system settings, or if it could possibly escape the sandbox altogether. For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent.







AppInfo views have also been reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops. Plus, we no longer split out apps from alt stores into a separate header in category views, and a potential crash when adding alt stores has been fixed thanks to [Marius](https://github.com/meisenzahl)

AppCenter received a new Flatpak Repair feature thanks to [Marius](https://github.com/meisenzahl) which fixes an issue where some Flatpak runtimes could not be installed. Plus the updates page now shows a small message when everything is up-to-date, including the last time that AppCenter checked for updates.




## Sideload

Just like in AppCenter, our goal with Sideload is to keep you informed and in control when installing apps provided directly by the developer. We also want to make sure to balance that with the existing trust relationship you may have with the apps you love. So we've made some changes to how apps are presented in Sideload and instead of assuming that a sideloaded app is untrusted, we simply ask for you to validate your trust. Additionally, we now show some basic information about the kinds of broad system permissions that a sideloaded app may request. This isn't as fine-grained as what is presented in AppCenter, but it offers quick validation for apps that are more likely to be safe.







## Mail

In the sidebar, you'll notice that special folders like "Archive" and "Spam" are better detected and appear at the top level, even for accounts like Gmail that used to hide them as subfolders. You can now also rename folders by secondary-clicking on them and selecting "Rename Folder". And you'll notice that Mail's primary menu is now in the bottom right corner of the sidebar. Plus, performance has been improved when switching between folders.

In the conversation list, you can now use a multi-touch swipe or click-and-drag left or right to quickly archive or trash a conversation. You might also appreciate some subtle design tweaks like placing the conversation list filter next to the search bar or how headers now appear to float over scrolled content.

In the messages list, there's a new "Move conversation" menu that includes search, and you'll notice that archiving and moving messages can now be undone. Mail now does a better job of calculating message height to avoid extra scroll bars, and a handy infobar is shown when a message includes a calendar invite.

When composing a message, you can now add images inline and you can include attachments in forwarded messages. Plus we've added support for multiple custom signatures. You can create as many signatures as you'd like and assign them as the defaults for accounts as needed. The new "Insert signature…" menu makes it easy to swap between any of your saved signatures when composing. And the composer now always opens in a separate, non-modal window making it much easier to reference a message you're replying to or manage multiple drafts at the same time. It also features quite a few more keyboard shortcuts for text formatting, adding attachments, etc.

Mail also does a better job handling changes in your internet connection, and if you like to start Mail manually, it will wait until the first time you've started it to check for new messages in the background.







## Files




The headlining feature of this Files release is the new app menu in the headerbar. [Jeremy](https://github.com/jeremypw) put together this menu to better improve discoverability for features like zoom and undo/redo as well as to clean up folder context menus. The Undo and Redo buttons include tooltips showing what operation will be performed before you click them and we also updated the description for the double-click setting to make it more clear.

A long requested feature, this month Bulk Rename lands in Files thanks to [Jeremy](https://github.com/jeremypw). With this feature, you can select a number of files, secondary-click, and select "Rename…" to get an advanced bulk renaming dialog. This is an especially useful feature if you're working with a large collection of photos or spreadsheets or other kinds of files that you may want to rename by creation date or using another sequence or when you have to format a large number of files the same way. We're looking forward to your feedback on this feature and improving it to fit your advanced file management needs!

Plus, you can now share files via Bluetooth. A new Bluetooth transfer dialog is available by secondary-clicking a file or selection of files and selecting "Send Files via Bluetooth" from the menu.

This release of Files sports a new Tab Bar powered by LibHandy with improved animations, smoother drag-and-drop, and reorganized tab context menus, bringing it more in line with Web.

Also, the storage level bar in Properties dialogs will now change color depending on how full a drive is.

[Jeremy](https://github.com/jeremypw) has also rewritten the way color tags are stored using extended file attributes instead of a database; This means tags should be better preserved when restoring from the Trash for example and you've no need to fear because Files will automatically update your tags to use the new system in the background.


## Music

Music can now accept Drag and Drop of whole folders and you can secondary click on a folder in Files and open it with Music. Plus it's been updated to the latest Flatpak platform which fixes issues with certain animations.

## Videos

https://github.com/elementary/videos/releases/tag/3.0.0

We've been hard at work getting Videos ready for GTK 4 and one of the steps along the way was getting rid of Clutter—big "C"—which has lead to a massive rework of the app's internals. The code base is much cleaner and clearer and should be more reliable and performant. This release still uses GTK 3, but look forward to GTK 4 in the next release.

For now you can expect improved playback position saving, a flatter app appearance in the welcome screen and library, smoother navigation, and in-app notifications when adding items to the playlist. Major shoutouts to [Leonhard](https://github.com/leolost2605) here.










## Web

The latest GNOME Web 44.2 has now been ported to Gtk 4 and features much improved performance and web standards compatibility, plus a new saved passwords popover. With Firefox sync, web apps, and performance that matches major mainstream competitors, there's never been a better time to try this community-made web browser.

The latest version of Web fixes a crash in the bookmarks popover, improves the reliability of creating web apps, and has a fix related to local storage access requests.

## Calculator

Calculator now follows keyboard shortcuts for copy and paste, even when the main text entry isn't focused, thanks to [Leo](https://github.com/lenemter)! It will no longer preserve extra white space on the right side of the window when used with alternative window button layouts. And Calculator will now always use the elementary stylesheet and icons, even when run on a different operating system, to prevent breakage related to missing assets.






## Code

[Jeremy](https://github.com/jeremypw) has been working diligently on this release of Code which closes more than 20 reported issues and brings plenty of improvements to search. Code now does a better job handling file saving and preventing data loss when files can't be written to their original location. Some busy infobars are now dialogs, and we avoid showing too many aggressive warnings about file saving. And you can now optionally try to continue loading files that contain unknown characters or corrupted content.

Search options are now all available from a new menu, there's now a "match whole words" option, and your search settings are now saved between sessions. The search entry also provides visual feedback when no results are found. We do a better job deciding which string to search if you have both a selection and text in the search entry, and make sure that the "Replace" and "Replace All" buttons are enabled and disabled more accurately. And an issue that prevented global search from working on startup was fixed.

In the sidebar, folders that don't contain text files can now be expanded properly, and Code does a better job making sure sidebar focus updates correctly when tabs are closed. The tab width menu has been reworked quite a bit to more accurately prioritize between your global defaults, per document settings, and editorconfig file. An issue that caused an incorrect column number in the line number menu was fixed.

The Vala symbols outline now correctly matches Code when the style changes after startup, and we fixed issues with styling when no documents are open. An issue that caused excessive reads and writes to settings has been fixed. Plus, you can now switch tabs with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>PageUp</kbd>/<kbd>PageDown</kbd> thanks to [Stan](https://github.com/stan-janssen)

## Terminal

This release was extremely collaborative with quite a few commit authors. It contains fixes related to tab switching shortcuts and makes sure that context menus are updated when activated with the menu key thanks to [Lasne](https://github.com/Faelian) and [Ryo](https://github.com/ryonakano), respectively. [Stan](https://github.com/stan-janssen) also resolved an issue where shortcuts conflicted with some command line apps and added a new option to start Terminal hidden. [Jeremy](https://github.com/jeremypw) also fixed an issue with `#` characters in URLs. Finally, thanks to [Gustavo](https://github.com/marukesu) and [Corentin](https://github.com/tintou) for their work on unit testing and code cleanup in this release.









# System Settings



## Desktop

The latest release of Desktop settings includes some new options for switching workspaces via hotcorners as well as a new feature to dim wallpapers in dark mode. You'll also notice that the setting for disabling animations has moved to the "Appearance" tab and has been renamed to "Reduce Motion".

The Dock &amp; Panel tab of Desktop settings also received a responsive redesign with added description labels for some settings. Additionally, checkboxes for extra indicators like the Accessibility indicator and the Capslock and Numlock indicators are now centrally located here.

## Applications

Updated Startup settings to show apps that use the Background &amp; Autostart Portal and we made quite a few changes to this view to bring it in line with modern design patterns and ensure that it was more responsive for large and small displays.

We also updated Default apps settings and did quite a bit of code cleanup here. plus he improved screen reader names for several settings while here.

Added search to the Permissions tab

## Displays

We're also introducing a new set of display filters, designed to assist folks with color deficiency issues. This is a very common disability with 1 in 12 men experiencing color deficiency and some folks developing color deficiency as they age.

Additionally, we're now shipping a grayscale filter which can help avoid distractions or alleviate screen addiction and you can now make the display much warmer when using Night Light. You may also notice a small redesign of Night Light settings for responsiveness. Finally, there should be more accurate display resolution options available.


## Sound

Sound Settings got a bit of a redesign for improved responsiveness on small and large displays and you may notice some improved description labels.

## Keyboard

The Behavior tab of Keyboard settings got a major update with the additional of several new settings for things like Bounce, Slow, and Sticky keys. Slider values are now shown on drag instead of in a separate widget. Plus, app developers can now link directly to custom shortcuts settings.

A couple of keyboard settings moved around, but were not removed! On-screen keyboard settings are now on the Behavior tab and panel indicator settings are now available in Desktop → Dock &amp; Panel.

Progress dialog from being shown when installing input method engines, as well as adding multitouch gesture support for navigating backwards through the installation steps,

and made sure the <kbd>PrintScreen</kbd> key can be used for keyboard shortcuts.

"Cycle Windows of application" and "Cycle Windows of application backwards" shortcuts

## Security &amp; Privacy

In Security &amp; Privacy Settings, you now have the option to automatically clean up Screenshot files as part of Housekeeping.

## Online Accounts

There's also a new version of Online Accounts settings thanks to [Leonhard](https://github.com/leolost2605) which fixes a freeze when the server doesn't respond while adding an IMAP account, and improves support for special folders like Archive and Sent folders. Online Accounts settings was updated with a fix for setting the correct SMTP username when configuring IMAP accounts, thanks to [Stan](https://github.com/stan-janssen). And, [Leo](https://github.com/lenemter) made sure the icons there for Mail and Tasks were updated to their latest versions.

## Settings Daemon

Finally, the Settings Daemon will now check for and notify of Firmware updates when they're available thanks to [Marius](https://github.com/meisenzahl) and we support Accent Colors on the Settings Portal thanks to [Alice](https://github.com/alice-mkh)












## Panel

As part of the aforementioned Bluetooth file transfer feature, you can see ongoing transfers in the Bluetooth indicator. And thanks to [Stan](https://github.com/stan-janssen), Bluetooth devices will now use any custom device names you've set up before falling back to more generic device names.

We now do a better job making sure notification bubbles you've dismissed with a swipe or the close button don't end up in the Notifications indicator, and the number of missed notifications in the tooltip should be more accurate, thanks again to [Jeremy](https://github.com/jeremypw). [Leo](https://github.com/lenemter) improved support for notifications that contain markup and [Leonhard](https://github.com/leolost2605) fixed the change in indicator width when all notifications have been cleared.

Plus, we updated some icons in the Bluetooth, Night Light, and Notifications indicators to be more consistent.

The Sound indicator was updated to use circle buttons and should no longer change size when skipping tracks. Muting should no longer affect monitor sources thanks to [Gran](https://github.com/GranPC), and microphone icons have been subtly updated. Plus, [Leo](https://github.com/lenemter) made sure the Accessibility indicator shows the correct text size on startup.

The network indicator has been getting some major design attention and now offers a much better experience for using VPNs. You'll notice that most options now appear as circular toggle buttons with icons instead of a list of switches. This new design both saves space on devices with complex network configurations and shows the status of your various connections much clearer, including intermediate and error states. In the case of VPNs, you can now also activate multiple connections at once.

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


## Notifications

Leo also removed the intrusive "Automatic Suspend" notifications. Gustavo made sure critical notifications are still sent even when Do Not Disturb is active and contributed quite a bit of code cleanup in the notifications server. And new contributor [Sean](https://github.com/SuperRiderTH) made a fix for the option to disable sounds from notifications sent by apps that don't properly identify themselves.

Also [Gustavo](https://github.com/marukesu) and [Leonhard](https://github.com/leolost2605) fixed a couple issues related to Notification close behavior.













## And More

Linux 6.2, Ubuntu HWE

## Get elementary OS 7.1

elementary OS 7.1 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 7.1 FAQ](https://github.com/elementary/os/wiki/elementary-OS-7.1-FAQ){: .button.flat }
[Download elementary OS 7.1][elementary.io]{: .button.suggested }
</div>

If you’re already on elementary OS 7, you’ll get the update to OS 7.1 alongside regular operating system updates. If you haven't already, open AppCenter and select _Update All_ to be upgraded.

[elementary.io]: https://elementary.io
[updates]: {{ site.baseurl }}/tags/#updates
