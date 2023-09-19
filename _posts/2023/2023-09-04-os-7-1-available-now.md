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

- Inclusive Personalization
- Privacy & Consent
- Addressing Your Feedback

To get elementary OS 7.1 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

# Privacy &amp; Consent

Portals provide a safe and consensual way for apps to interact with operating system features and make sure that they only get access to the data you want them to. One of the ways that apps may become intrusive is by automatically starting themselves or running in the background without your permission. In OS 7.1, we now provide the Background &amp; Autostart Portal which alerts you when apps are running in the background and makes sure that apps ask your permission before they can automatically start up when you turn on your device.

Calendar, Mail, and Tasks now all use the Background & Autostart portal, and their autostart behavior can be controlled along with other apps in System Settings → Applications → Startup. Calendar and Mail have also been updated to use the File Chooser Portal for things like selecting attachments or importing and exporting calendar files.

We've now migrated Location Services from the old Agents system to Portals. This is a more secure method for apps to request access to your location, is the latest FreeDesktop.org standard for doing so, and improves our cross-platform app compatibility. You can adjust location settings in System Settings → Security &amp; Privacy → Location Services. If the main switch here is turned off, apps will not be allowed to even ask for permission, so make sure it's turned on if you are using apps or services that make use of location data.

As we work towards our continual goal of better supporting alternative app stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. In elementary OS, the supported app packaging format is Flatpak which gives us several tools to that end, including the ability to report back to you when apps have advanced access that could leave you vulnerable. In OS 7.1, AppCenter will now inform you if an app can can:

- Read your location, send notifications, or automatically start and run in the background without asking first
- Access system folders or your home folder
- Read and write system settings
- Possibly escape the sandbox altogether

For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent.

Just like in AppCenter, our goal with Sideload is to keep you informed and in control when installing apps provided directly by the developer. We also want to make sure to balance that with the existing trust relationship you may have with the apps you love. So we've made some changes to how apps are presented in Sideload and instead of assuming that a sideloaded app is untrusted, we simply ask for you to validate your trust. Additionally, we now show some basic information about the kinds of broad system permissions that a sideloaded app may request. This isn't as fine-grained as what is presented in AppCenter, but it offers quick validation for apps that are more likely to be safe and puts the emphasis on Sideload as a utility to verify your consent, not to gatekeep your choices.

Housekeeping is a feature designed to free up storage and protect your privacy by automatically deleting old files. You can now choose to automatically clean up the Trash, Downloads, Screenshots, and temporary operating system files on a schedule of your choosing.

# Inclusive Personalization

When we think about settings and personalization in elementary OS, we tend to avoid settings that would pass off design or engineering decisions and instead focus on providing settings that make the operating system more accessible and inclusive for a wider range of people. We use this guiding philosophy to decide which new settings to add without creating an overwhelming or confusing number of customization options. This release, like every release, comes with a number of new features and settings that we hope make it possible for more people to enjoy using an Open Source operating system.

We've received feedback from folks with vision-related disabilities that a huge barrier for them when considering an Open Source operating system is that they often need help to get it installed. Now, when you boot into the install media for elementary OS, we automatically play an audio prompt letting you know the keyboard shortcut for turning on the screen reader. And the same audio prompt is available during Initial Setup, so whether you're buying a computer pre-installed with elementary OS or installing it on your existing computer, you can choose an Open Source operating system and remain independent.

1 in 12 men experience color perception deficiency (aka color blindness) from birth and some folks will develop color deficiency as they age—but those we spoke to about accommodations reported that color deficiency assistance tools are often ineffective or unavailable and the lack of awareness and education around color deficiency means that many don't seek assistance at all. This can affect daily tasks when trying to understand parts of their computer's interface, but it also comes up when playing games and can make it difficult to work and play collaboratively. We introduced a set of 5 display filters, designed to assist folks with Protanopia, Deuteranopia, and Tritanopia with some additional high contrast options and plenty of assistive text to help folks without a formal color deficiency diagnosis.

Additionally, we're now shipping a grayscale filter which can help avoid distractions or alleviate screen addiction and you can now make the display much warmer when using Night Light. For folks who suffer from motion sickness or simply prefer fewer animations, the "Reduce Motion" setting in Desktop → Appearance now covers several more window manager and shell animations. And we've added a new option in Desktop → Wallpaper to dim the wallpaper when the Dark Style is selected.

Navigating via keyboard is important for a wide range of folks whether that's due to disability or personal preference and this release comes with a number of improvements in this area. For managing app windows, you can now use the keyboard shortcut <kbd>Alt</kbd> + <kbd>~</kbd> for switching between windows of the same app, and you can now navigate with the arrow keys while holding down <kbd>Alt</kbd> + <kbd>Tab</kbd>. In the Multitasking View, a number of previously unavailable shortcuts are now available including Pointer location, Screenshots, and Zoom, in additional to regular workspace switching shortcuts. When customizing keyboard shortcuts, we now do a better job handling special keys and single-key shortcuts like the <kbd>PrintScreen</kbd> key. And, you can now close panel indicators with <kbd>Esc</kbd>.

We also completely revamped the Behavior page of System Settings → Keyboard. It now includes several new settings for things like Bounce, Slow, and Sticky keys with descriptions of their effects, and slider values are now shown on drag instead of in a separate widget. This work was the final piece of our project to integrate previously tucked-away accessibility settings throughout System Settings, improving their discoverability and normalizing the use of accomodations for everyone.

The Login &amp; Lock Screen now does a better job matching your mouse, keyboard, and touchpad settings, including improved keyboard layout handling. Your chosen accent color is now used everywhere—not just on your login card—and it now handles solid color wallpapers. Your text size and font settings, pointer size settings, cursor blink settings, Night Light settings and more are all now respected as well. Plus, the ability to reveal the pointer is now available, the Screen Reader can be enabled with a keyboard shortcut, and it does a better job remembering your Screen Reader settings.

We know that Multitouch gestures and navigation are really important to folks running elementary OS on devices with touch screens and multitouch trackpads so we've continued to improve support for navigating via gestures in places like the Installer and in multi-step dialogs.

Additionally, checkboxes for extra indicators like the Accessibility indicator and the Capslock and Numlock indicators are now centrally located in Desktop → Dock &amp; Panel.

# Addressing Your Feedback

One of the greatest advantages we have developing elementary OS in the open as compared to proprietary operating systems is the ability to gather your feedback and for developers to directly engage with you to solve issues and create new features. Combined with our monthly release cadence, the Feedback app creates a tight loop where you can start a report, see development happen transparently, and receive updates quickly. With the release of OS 7, we made sure that the Feedback app was accessible directly from the applications menu, launched instantly, and covered more system components. In OS 7.1, we've added search and we've now ported the app to GTK 4—the latest version of our app toolkit—for improved performance and smoothness. This should make it even speedier to send feedback when something unexpected happens.

<figure markdown="1">
![Feedback](/images/{{ page.slug }}/feedback.png){: width="570" height="621"}
<figcaption markdown="1">
The Feedback app now features search
</figcaption>
</figure>

Since the release of OS 7 at the end of January, we've sent out free updates that address over 200 reports—that's one report addressed every day in addition to our regular planned work. Needless to say OS 7.1 is much smoother, faster, and more stable than its predecessor.

## Onboarding

Onboarding is the most personal part of getting started with elementary OS, where you choose how you'll experience your individual account and are introduced to core features of the operating system.

With Flatpak, you have access to an incredibly wide selection of apps and a growing number of alternative app stores. Unlike on mainstream proprietary operating systems, installing apps via Sideload and accessing alternative app stores are important features of elementary OS. So, when we're introducing people to AppCenter—the pay-what-you-can app store with apps made specifically for elementary OS—we also now much more prominently introduce them to Sideload and even feature a prominent link to the most popular Flatpak-powered app store: Flathub.

Onboarding now also handles providing information about the temporary Guest account.

## AppCenter

AppCenter received a new Flatpak Repair feature which fixes an issue where some Flatpak runtimes could not be installed. Plus, we no longer split out apps from alt stores into a separate header in category views. Plus the updates page now shows a small message when everything is up-to-date, including the last time that AppCenter checked for updates.

## Mail

In the sidebar, you'll notice that special folders like "Archive" and "Spam" are better detected and appear at the top level, even for accounts like Gmail that used to hide them as subfolders. You can now also rename folders by secondary-clicking on them and selecting "Rename Folder". And you'll notice that Mail's primary menu is now in the bottom right corner of the sidebar. Plus, performance has been improved when switching between folders.

In the conversation list, you can now use a multi-touch swipe or click-and-drag left or right to quickly archive or trash a conversation. You might also appreciate some subtle design tweaks like placing the conversation list filter next to the search bar or how headers now appear to float over scrolled content.

In the messages list, there's a new "Move conversation" menu that includes search, and you'll notice that archiving and moving messages can now be undone. And a handy infobar is shown when a message includes a calendar invite.

When composing a message, you can now add images inline and you can include attachments in forwarded messages. Plus we've added support for multiple custom signatures. You can create as many signatures as you'd like and assign them as the defaults for accounts as needed. The new "Insert signature…" menu makes it easy to swap between any of your saved signatures when composing. And the composer now always opens in a separate, non-modal window making it much easier to reference a message you're replying to or manage multiple drafts at the same time. It also features quite a few more keyboard shortcuts for text formatting, adding attachments, etc.

Mail also does a better job handling changes in your internet connection, and if you like to start Mail manually, it will wait until the first time you've started it to check for new messages in the background.

## Files

In the Files app, we're always striving to strike a balance between providing advanced file management features and avoiding clutter and confusion. Folder context menus had begun to reach a point where they were being stretched a bit too far, so we introduced a new app menu in the headerbar to provide app-wide controls and settings and improve the discoverability of some features that were previously only accessible by keyboard shortcut like Zoom and Undo/Redo. The new Zoom controls make it easier to set a comfortable icon size and expose keyboard shortcuts in their tooltips. The Undo and Redo buttons include tooltips showing what operation will be performed before you click them as well as their keyboard shortcuts. The description text for the Double-click setting has been made more clear based on your feedback, and we've consolidated settings for which things will be shown in the view such as Hidden Files and Thumbnails.

We've also introduced Bulk Rename. With this feature, you can select multiple files, secondary-click, and select "Rename…" to get an advanced bulk renaming dialog. This is an especially useful feature if you're working with a large collection of photos or spreadsheets or other kinds of files that you may want to rename by creation date or using another sequence or when you have to format a large number of files the same way. You can add automatically generated prefixes or suffixes to file names, as well as keeping, completely replacing, or partially replacing parts of the original file name. You'll see a preview of how files will be renamed as well as an indication of when file names would conflict or not be changed.

Plus, you can now share files with other devices via Bluetooth. A new Bluetooth transfer dialog is available by secondary-clicking a file or selection of files and selecting "Send Files via Bluetooth" from the context menu. You can see ongoing transfers in the Bluetooth indicator.

Lastly, the tab bar features improved animations, smoother drag-and-drop, and reorganized tab context menus, bringing it more in line with Web. The storage level bar in Properties dialogs will now change color depending on how full a drive is. And we've rewritten the way color tags are stored so that they are better preserved when restoring from the Trash.

## Music &amp; Videos

Music can now accept Drag and Drop of whole folders and you can secondary click on a folder in Files and open it with Music.

Videos has undergone a large rewrite of its internals which has made it more reliable and performant. Expect a flatter app appearance in the welcome screen and library, improved playback position saving, smoother navigation, and in-app notifications when adding items to the playlist.

## Web

The latest GNOME Web 44.6 has now been ported to GTK 4 and features much improved performance and web standards compatibility, plus a new saved passwords popover. With Firefox sync, web apps, and performance that matches major mainstream competitors, there's never been a better time to try this community-made web browser.

## Code

Code now does a better job handling file saving and preventing data loss when files can't be written to their original location. Some busy infobars are now dialogs, and we avoid showing too many aggressive warnings about file saving. And you can now optionally try to continue loading files that contain unknown characters or corrupted content.

Search options are now all available from a new menu, there's now a "match whole words" option, and your search settings are now saved between sessions. The search entry also provides visual feedback when no results are found. We do a better job deciding which string to search if you have both a selection and text in the search entry, and make sure that the "Replace" and "Replace All" buttons are enabled and disabled more accurately.

In the sidebar, folders that don't contain text files can now be expanded properly, and Code does a better job making sure sidebar focus updates correctly when tabs are closed.

The tab width menu has been reworked quite a bit to more accurately prioritize between your global defaults, per document settings, and editorconfig file.

Plus, you can now switch tabs with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>PageUp</kbd>/<kbd>PageDown</kbd>.

## Notifications

The Notifications indicator is where you can catch up with missed notifications and it supports all the same ways you're used to interacting with notifications like tapping a notification to launch the app that sent it and multi-touch swipe left or right to dismiss. Now, missed notifications can also have buttons and apps can replace old outdated notifications with newer up-to-date ones instead of add more and more notifications to the stack.

Sometimes we have apps that send a lot of notifications that are important but drown out other apps, so now you can select the spinning triangle icon to collapse all the notifications from a particular app.

Critical notifications—like low battery warnings—will now still be sent even when Do Not Disturb is active and notifications are now shown even when in the Multitasking View. Plus, we've improved support for notifications that include markup—like bold and italics—and we removed the intrusive "Automatic Suspend" notifications that would sometimes prevent your device from sleeping.

## Design Improvements

Onboarding features several redesigned pages with some new icons and bolder typography. Plus we now use the release wallpaper in a dynamically generated icon on the Welcome page and previews in the Style view use the currently set wallpaper.

Plus you'll also notice that the Login &amp; Lock Screen now has subtly rounded corners that match the logged in session.

Several pages in System Settings have been redesigned for improved responsiveness on large and small displays, including Applications → Defaults and Applications → Startup, Desktop → Dock &amp; Panel, Displays → Night Light, Keyboard → Behavior, and Sound. And in several of these views we improved description text for more complicated settings.

Our responsive work also continued in AppCenter, where App Info views were reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops. And the Installed &amp; Updates view now uses a grid layout for installed apps, making better use of space on large displays.

## Panel

The Network indicator received some much-needed design attention and now offers a vastly-improved experience for using VPNs. You'll notice that most options now appear as circular toggle buttons with icons instead of a list of switches. This new design both saves space on devices with complex network configurations and shows the status of your various connections much clearer, including intermediate and error states. In the case of VPNs, you can now also activate multiple connections at once. We've also added quick access to toggling Airplane Mode, including a middle-click action on the indicator icon. Plus, we're now using a feature of Network Manager to automatically get better device names so you'll rarely see long and cryptic device names any longer.

The Sound indicator was updated to use circle buttons and should no longer change size when skipping tracks. Muting should no longer affect monitor sources.

Bluetooth devices in the indicator will now use any custom device names you've set up before falling back to more generic device names.

The Power indicator now always uses hours as its largest unit, for example it will say "26 hours remaining" instead of "1 day remaining" and we improved the accuracy of battery level icons.

Plus, we've updated icons in the Bluetooth, Network, Night Light, Notifications, and Sound indicators to be more consistently sized and with clearer disabled states.

## Hardware Support

OS 7.1 includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.2.

Some computers contain hardware devices that require additional, proprietary drivers to function properly. This previously made installing elementary OS difficult when wireless network drivers or video card drivers were unavailable. We now provide an option during installation to include these proprietary drivers so that your devices function properly.

We also now automatically check for and notify of updates to device Firmware when they're available.

Finally, there should be more accurate display resolution options available in System Settings → Displays.

---

## Get elementary OS 7.1

elementary OS 7.1 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 7.1 FAQ](https://github.com/elementary/os/wiki/elementary-OS-7.1-FAQ){: .button.flat }
[Download elementary OS 7.1][elementary.io]{: .button.suggested }
</div>

If you’re already on elementary OS 7, you’ll get the update to OS 7.1 alongside regular operating system updates. If you haven't already, open AppCenter and select _Update All_ to be upgraded.

[elementary.io]: https://elementary.io
[updates]: {{ site.baseurl }}/tags/#updates














Stuff I don't know where it goes:

Our Portals—things like the app chooser and access dialogs—have now been ported to GTK 4!

accidentally closing windows when using three-finger multi-touch gestures.

fixes that prevent misclicks and accidentally triggering actions in window manager

The latest release of Desktop settings includes some new options for switching workspaces via hotcorners

Plus improved screen reader names for several settings while here.

Added search to the Permissions tab
