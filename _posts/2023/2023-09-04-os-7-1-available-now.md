---
title: elementary OS 7.1 Available Now
description: Made with care, with you in mind
author: danrabbit
image: /images/os-7-1-available-now/card.png

tags:
  - horus
  - updates

hidden: 2023-10-31 17:00:00 UTC # 9 AM PST
---

Today, we're proud to announce that OS 7.1 is available to download now and shipping soon on several high-quality computers. This release represents the sum of our work over the last several months as a single major update to the OS 7 series and includes [all of the monthly OS updates][updates] we've detailed since the OS 7 release.

<figure class="full-bleed" markdown="1">
![elementary OS 7.1](/images/{{ page.slug }}/desktop-onboarding.png)
</figure>

With OS 7.1, we've focused in on:

- Providing **personalization** options and features that make our operating system more **inclusive** and **accessible**
- Protecting your **privacy** and ensuring apps always operate with your explicit **consent**
- Addressing your **feedback** with over 200 bug fixes, design changes, and new features

To get elementary OS 7.1 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

# Privacy &amp; Consent

One of the most prevalent problems we face in our current digital lives is the violation of our privacy and the lack of consent when interacting with our devices each day. Portals seek to provide a safe and consensual way for apps to interact with the operating system and ensure that they only get access to the data and features that you want them to.

One of the ways that apps may become intrusive is by automatically starting themselves or running in the background without your permission. In OS 7.1, we now provide the Background &amp; Autostart Portal which alerts you when apps are running in the background and makes sure that apps ask your permission before they can automatically start up when you turn on your device.

<figure markdown="1">
![System Settings → Applications → Startup](/images/{{ page.slug }}/settings-autostart.png){: width="990" height="686"}
<figcaption markdown="1">
Autostarting apps can now be controlled in System Settings → Applications → Startup
</figcaption>
</figure>

Calendar, Mail, and Tasks now all use the Background & Autostart portal, and their autostart behavior can be controlled along with other apps in System Settings → Applications → Startup. Calendar and Mail have also been updated to use the File Chooser Portal—the Portal responsible for making sure apps can’t access data without your permission—for things like selecting attachments or importing and exporting calendar files.

<figure markdown="1">
![The Location Portal](/images/{{ page.slug }}/portal-location.png){: width="502" height="177"}
<figcaption markdown="1">
The Location Portal ensures apps ask before they can get your location
</figcaption>
</figure>

We've now also migrated Location Services from the old Agents system to Portals. This is a more secure method for apps to request access to your location, is the latest FreeDesktop.org standard for doing so, and improves our cross-platform app compatibility. You can adjust location settings in System Settings → Security &amp; Privacy → Location Services. If the main switch here is turned off, apps and system services will not even be allowed to ask for permission to see your location.

## AppCenter &amp; Sideload

As we work towards our continual goal of better supporting alternative app stores, one of the challenges is ensuring that you remain safe while using apps from stores with differing security and privacy policies. In elementary OS, the supported app packaging format is Flatpak which gives us several tools to that end, including the ability to report back to you when apps have advanced access that could leave you vulnerable.

<figure class="card quarter" markdown="1">
![Autostart warning in AppCenter](/images/{{ page.slug }}/appcenter-autostart.png){: width="974" height="704"}
![File access warning in AppCenter](/images/{{ page.slug }}/appcenter-files.png){: width="974" height="704"}
![Sandbox break warning in AppCenter](/images/{{ page.slug }}/appcenter-sandbox.png){: width="974" height="704"}
![Settings access warning in AppCenter](/images/{{ page.slug }}/appcenter-settings.png){: width="974" height="704"}
<figcaption>AppCenter shows more information about app permissions</figcaption>
</figure>

In OS 7.1, AppCenter will now inform you if an app can can:

- Read your location, send notifications, or automatically start and run in the background without asking first
- Access system folders or your home folder
- Read and write system settings
- Possibly escape the sandbox altogether and gain arbitrary advanced permissions

For certain types of administrative apps, having advanced system permissions makes sense, but our goal is to keep you informed and ensure that apps are always operating with your consent.

<figure markdown="1">
![Sideload](/images/{{ page.slug }}/sideload-firefox.png){: width="502" height="320"}
<figcaption markdown="1">
Sideload now quickly checks if apps request advanced system permissions
</figcaption>
</figure>

Our goal with Sideload is to keep you informed and in control when installing apps provided outside of AppCenter. We also want to make sure to balance that with the existing trust relationship you may have with the apps you love. So we've made some changes to how apps are presented in Sideload and instead of assuming that a sideloaded app is untrusted, we simply ask for you to validate your trust. Additionally, we now show some basic information about the kinds of broad system permissions that a sideloaded app may request. This isn't as fine-grained as what is presented in AppCenter, but it offers quick validation for apps that are more likely to be safe and puts the emphasis on Sideload as a utility to verify your consent, not to gatekeep your choices.

## Housekeeping &amp; Temporary Accounts

Housekeeping is a feature designed to free up storage and protect your privacy by automatically deleting old files. In OS 7, you could choose to automatically clean up the Trash, Downloads, and temporary operating system files on a schedule of your choosing. In OS 7.1, we’ve added Screenshots to that list. You’ll first be introduced to Housekeeping in the Onboarding app, but you can adjust your Housekeeping settings at any time in System Settings → Security &amp; Privacy → Housekeeping.

<figure markdown="1">
![Housekeeping in Onboarding](/images/{{ page.slug }}/onboarding-housekeeping.png){: width="485" height="443"}
<figcaption markdown="1">
Housekeeping can clean up old Downloads, Screenshots, Trash, and other temporary files
</figcaption>
</figure>

The Guest account is a special account that provides a temporary space for folks who don’t normally use your device to access your computer without using your personal account. And, all settings and data in this account are reset as soon as they log out. In OS 7.1, Onboarding now handles providing information about how this account works, making its function and limitations much more clear.

# Inclusivity & Personalization

When we think about settings and personalization in elementary OS, we tend to avoid settings that would pass off design or engineering decisions and instead focus on providing settings that make the operating system more accessible and inclusive for a wider range of people. We use this guiding philosophy to decide which new settings to add without creating an overwhelming or confusing number of customization options. This release, like every release, comes with a number of new features and settings that we hope make it possible for more people to enjoy using an Open Source operating system.

We've received feedback from folks with vision-related disabilities that a huge barrier for them when considering an Open Source operating system is that they often need help to get it installed. Now, when you boot into the install media for elementary OS, we automatically play an audio prompt letting you know the keyboard shortcut for turning on the screen reader. And the same audio prompt is available during Initial Setup, so whether you're buying a computer pre-installed with elementary OS or installing it on your existing computer, you can choose an Open Source operating system and remain independent.

<figure markdown="1">
![System Settings → Displays → Filters](/images/{{ page.slug }}/settings-filters.png){: width="990" height="686"}
<figcaption markdown="1">
We've introduced 5 new display filters to assist folks with color perception deficiency
</figcaption>
</figure>

From birth, 1 in 12 men experience color perception deficiency (aka color blindness) and some folks will develop color deficiency through illness or aging—but those we spoke to about accommodations reported that color deficiency assistance tools are often ineffective or unavailable and the lack of awareness and education around color deficiency means that many don't seek assistance at all. This can affect daily tasks when trying to understand parts of their computer's interface, but it also comes up when playing games and can make it difficult to work and play collaboratively. We introduced a set of 5 display filters, designed to assist folks with Protanopia, Deuteranopia, and Tritanopia with some additional high contrast options and plenty of assistive text to help folks without a formal color deficiency diagnosis. These filters alter the colors of the entire display to assist you in differentiating between colors where you may be experiencing color deficiency. The feedback we’ve received from testers has been very positive, so if you’ve used these kinds of filters in the past on other operating systems with lackluster results we encourage you to give these a try.

Additionally, we're now shipping a grayscale filter which can help avoid distractions or alleviate screen addiction. You can now make the display much warmer when using Night Light and we've added a new option in Desktop → Wallpaper to dim the wallpaper when the Dark Style is selected—a couple things that can help alleviate headache and eye strain. For folks who suffer from motion sickness or simply prefer fewer animations, the "Reduce Motion" setting in Desktop → Appearance now covers several more window manager and shell animations.

Finally, checkboxes for optional indicators like the Accessibility indicator and the Capslock and Numlock indicators are now centrally located in Desktop → Dock &amp; Panel. And we’ve improved screen reader names for several settings.

## Gesture and Keyboard Navigation

We know that Multitouch gestures and navigation are really important to folks running elementary OS on devices with touch screens and multitouch trackpads so we've continued to improve support for navigating via gestures in places like the Installer and in multi-step dialogs. And, there are now more options for switching workspaces using hot corners in System Settings →Desktop → Multitasking.

Navigating via keyboard is important for a wide range of folks whether that's due to disability or personal preference and this release comes with a number of improvements in this area. For managing app windows, you can now use the keyboard shortcut <kbd>Alt</kbd> + <kbd>~</kbd> for switching between windows of the same app, and you can now navigate with the arrow keys while holding down <kbd>Alt</kbd> + <kbd>Tab</kbd>. In the Multitasking View, a number of previously unavailable shortcuts are now available including Pointer location, Screenshots, and Zoom, in addition to regular workspace switching shortcuts. When customizing keyboard shortcuts, we now do a better job handling special keys and single-key shortcuts like the <kbd>PrintScreen</kbd> key. And, you can now close panel indicators with <kbd>Esc</kbd>.

We also completely revamped the Behavior page of System Settings → Keyboard. It now includes several new settings for things like Bounce, Slow, and Sticky keys with descriptions of their effects, and slider values are now shown on drag instead of in a separate widget. This work was the final piece of [our project to integrate previously tucked-away accessibility settings](https://blog.elementary.io/accessibility-features-are-just-features/) throughout System Settings, improving their discoverability and normalizing the use of accommodations for everyone.

## Login &amp; Lock Screen

In OS 7, many of the personalization settings and accommodations you may have set up in your account were inaccessible on the Login &amp; Lock Screen. In OS 7.1, we now match your mouse, keyboard, and touchpad settings—including improved keyboard layout handling—your chosen accent color is now used everywhere—not just on your login card—and it now handles solid color wallpapers. Your text size and font settings, pointer size settings, cursor blink settings, Night Light settings and more are all now respected as well. Plus, the ability to reveal the pointer is now available, the Screen Reader can be enabled with a keyboard shortcut, and it does a better job remembering your Screen Reader settings. As a subtle bonus, you’ll also notice that the Login &amp; Lock Screen now has rounded corners that match the logged in session

# Addressing Your Feedback

One of the greatest advantages we have developing elementary OS in the open as compared to proprietary operating systems is the ability to gather your feedback and for developers to directly engage with you to solve issues and create new features. Combined with our monthly release cadence, the Feedback app creates a tight loop where you can start a report, see development happen transparently, and receive updates quickly. With the release of OS 7, we made sure that the Feedback app was accessible directly from the applications menu, launched instantly, and covered more system components. In OS 7.1, we've added search and we've now ported the app to GTK 4—the latest version of our app toolkit—for improved performance and smoothness. This should make it even speedier to send feedback when something unexpected happens.

<figure markdown="1">
![Feedback](/images/{{ page.slug }}/feedback.png){: width="568" height="620"}
<figcaption markdown="1">
The Feedback app is the fastest way to send your feedback directly to our developers
</figcaption>
</figure>

Since the release of OS 7 at the end of January, we've sent out free updates that address over 200 reports—that's one report addressed every day in addition to our regular planned work. Needless to say OS 7.1 is much smoother, faster, and more stable than its predecessor thanks to your feedback. We’ve also made several design changes and added new features to address concerns that you’ve expressed and to better fit how you’ve told us that you use our operating system.

## AppCenter &amp; Alt Stores

With Flatpak, you have access to an incredibly wide selection of apps and a growing number of alternative app stores. Unlike on mainstream proprietary operating systems, installing apps via Sideload and accessing alternative app stores are important features of elementary OS. We’ve consistently heard from folks that sideloading and alt stores are core parts of their experience when using our operating system. So, in the Onboarding app, when we're introducing people to AppCenter—the pay-what-you-can app store with apps made specifically for elementary OS—we also now much more prominently introduce them to Sideload and even feature a link to the most popular Flatpak-powered app store: Flathub. And in AppCenter, we no longer split out apps from alt stores into a separate header in category views.

<figure markdown="1">
![Apps in Onboarding](/images/{{ page.slug }}/onboarding-apps.png){: width="485" height="443"}
<figcaption markdown="1">
Onboarding introduces people to both AppCenter and Sideload equally
</figcaption>
</figure>

One of the challenges we face is gracefully recovering and providing useful options when things go wrong. In OS 7, a failure when installing certain kinds of Flatpak updates could only be resolved by jumping into a Terminal; In OS 7.1, we have a handy Flatpak Repair feature that can fix most issues with these kinds of failures.

## Hardware Support

Some computers contain hardware devices that require additional, proprietary drivers to function properly. This previously made installing elementary OS difficult when wireless network drivers or video card drivers were unavailable. We now provide an option during installation to include these proprietary drivers so that your devices function properly.

OS 7.1 also includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.2. Notably, this brings improved support for Intel 13th gen processors and Intel Arc graphics, as well as performance enhancements for AMD Zen 4 CPUs.

We also now automatically check for and notify of updates to device Firmware when they're available. Plus, there should be more accurate display resolution options available in System Settings → Displays.

## Web

OS 7 shipped with GNOME Web 43, the latest version available at the time. Thanks to Flatpak, we’ve been able to stay up to date with the latest releases of Web and OS 7.1 is shipping with version 44.6 which brings substantial improvements to performance and web standards compatibility, plus a new saved passwords popover.

<figure markdown="1">
![GNOME Web](/images/{{ page.slug }}/web-welcome.png){: width="1058" height="802"}
<figcaption markdown="1">
Web is faster and more capable with features like Firefox sync and intelligent tracking prevention
</figcaption>
</figure>

With Firefox sync, web apps, intelligent tracking prevention that is actually intended to protect your privacy, built-in popup blocking, and performance that now matches major mainstream competitors, there's never been a better time to use this community-made web browser.

## Mail

In OS 6, we began an ambitious rewrite of Mail on a more stable and battle-tested base and we’re happy to report that with OS 7.1, Mail has gained a number of new features and improvements that you’ve been asking for.

In the sidebar, you'll notice that special folders like "Archive" and "Spam" are better detected and appear at the top level, even for accounts like Gmail that used to hide them as subfolders. You can now also rename folders by secondary-clicking on them and selecting "Rename Folder". Plus, performance has been improved when switching between folders.

In the conversation list, you can now use a multi-touch swipe or click-and-drag left or right to quickly archive or trash a conversation. You might also appreciate some subtle design tweaks like placing the conversation list filter next to the search bar or how headers now appear to float over scrolled content.

<figure markdown="1">
![Mail](/images/{{ page.slug }}/mail-move.png){: width="990" height="716"}
<figcaption markdown="1">
The new "Move Conversation" menu with search
</figcaption>
</figure>

In the messages list, there's a new "Move conversation" menu that includes search, and you'll notice that archiving and moving messages can now be undone. And a handy infobar is shown when a message includes a calendar invite.

<figure markdown="1">
![Mail](/images/{{ page.slug }}/mail-compose.png){: width="744" height="564"}
<figcaption markdown="1">
The composer now supports inline attachments and signatures
</figcaption>
</figure>

When composing a message, you can now add images inline and you can include attachments in forwarded messages. Plus we've added support for multiple custom signatures. You can create as many signatures as you'd like and assign them as the defaults for accounts as needed. The new "Insert signature…" menu makes it easy to swap between any of your saved signatures when composing. And the composer now always opens in a separate, non-modal window making it much easier to reference a message you're replying to or manage multiple drafts at the same time. It also features quite a few more keyboard shortcuts for text formatting, adding attachments, etc.

<figure markdown="1">
![Mail](/images/{{ page.slug }}/mail-signatures.png){: width="564" height="364"}
<figcaption markdown="1">
You can set up as many signatures as you like and set per-account defaults
</figcaption>
</figure>

Mail also does a better job handling changes in your internet connection, and if you like to start Mail manually, it will wait until the first time you've started it to check for new messages in the background.

## Files

In the Files app, we're always striving to strike a balance between providing advanced file management features and avoiding clutter and confusion. Folder context menus had begun to reach a point where they were being stretched a bit too far, so we introduced a new app menu in the headerbar to provide app-wide controls and settings and improve the discoverability of some features that were previously only accessible by keyboard shortcut like Zoom and Undo/Redo. The new Zoom controls make it easier to set a comfortable icon size and expose keyboard shortcuts in their tooltips. The Undo and Redo buttons include tooltips showing what operation will be performed before you click them as well as their keyboard shortcuts. The description text for the Double-click setting has been made more clear based on your feedback, and we've consolidated settings for which things will be shown in the view such as Hidden Files and Thumbnails.

<figure markdown="1">
![Files](/images/{{ page.slug }}/files-menu.png){: width="1064" height="744"}
<figcaption markdown="1">
The new app menu in Files exposes more functionality like zoom and undo/redo
</figcaption>
</figure>

We've also introduced Bulk Rename. With this feature, you can select multiple files, secondary-click, and select "Rename…" to get an advanced bulk renaming dialog. This is an especially useful feature if you're working with a large collection of photos or spreadsheets or other kinds of files that you may want to rename by creation date or using another sequence or when you have to format a large number of files the same way. You can add automatically generated prefixes or suffixes to file names, as well as keeping, completely replacing, or partially replacing parts of the original file name. You'll see a preview of how files will be renamed as well as an indication of when file names would conflict or not be changed.

<figure markdown="1">
![Bulk Rename](/images/{{ page.slug }}/files-rename.png){: width="492" height="448"}
<figcaption markdown="1">
You can now quickly rename multiple files at once
</figcaption>
</figure>

Plus, you can now share files with other devices via Bluetooth. A new Bluetooth transfer dialog is available by secondary-clicking a file or selection of files and selecting "Send Files via Bluetooth" from the context menu. You can see ongoing transfers in the Bluetooth indicator.

<figure markdown="1">
![Bluetooth Sharing](/images/{{ page.slug }}/files-bluetooth.png){: width="408" height="508"}
<figcaption markdown="1">
Share files to other devices over Bluetooth
</figcaption>
</figure>

Lastly, the tab bar features improved animations, smoother drag-and-drop, and reorganized tab context menus, bringing it more in line with Web. The storage level bar in Properties dialogs will now change color depending on how full a drive is. And we've rewritten the way color tags are stored so that they are better preserved when restoring from the Trash.

## Code

Code now does a better job handling file saving and preventing data loss when files can't be written to their original location. Some busy infobars are now dialogs, and we avoid showing too many aggressive warnings about file saving. And you can now optionally try to continue loading files that contain unknown characters or corrupted content.

Search options are now all available from a new menu, there's now a "match whole words" option, and your search settings are now saved between sessions. The search entry also provides visual feedback when no results are found. We do a better job deciding which string to search if you have both a selection and text in the search entry, and make sure that the "Replace" and "Replace All" buttons are enabled and disabled more accurately.

In the sidebar, folders that don't contain text files can now be expanded properly, and Code does a better job making sure sidebar focus updates correctly when tabs are closed.

The tab width menu has been reworked quite a bit to more accurately prioritize between your global defaults, per document settings, and editorconfig file.

Plus, you can now switch tabs with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>PageUp</kbd>/<kbd>PageDown</kbd>.

## Music &amp; Videos

Videos has undergone a large rewrite of its internals which has made it more reliable and performant. Expect a flatter app appearance in the welcome screen and library, improved playback position saving, smoother navigation, and in-app notifications when adding items to the playlist.

<figure markdown="1">
![Videos](/images/{{ page.slug }}/videos.png){: width="1069" height="747"}
<figcaption markdown="1">
Videos is now a bit flatter
</figcaption>
</figure>

Music can now accept Drag and Drop of whole folders—in addition to individual files or selections of files—and you can secondary click on a folder in Files and open it with Music.

## Notifications

The Notifications indicator is where you can catch up with missed notifications and it supports all the same ways you're used to interacting with notifications like tapping a notification to launch the app that sent it and multi-touch swipe left or right to dismiss. Now, missed notifications can also have buttons and apps can replace old outdated notifications with newer up-to-date ones instead of adding more and more notifications to the stack.

<figure class="full-bleed" markdown="1">
![Notifications Indicator](/images/{{ page.slug }}/indicator-notifications.png)
<figcaption markdown="1">
Notifications in the indicator can be replaced with updated ones or have buttons and app sections can be collapsed
</figcaption>
</figure>

Sometimes we have apps that send a lot of notifications that are important but drown out other apps, so now you can select the spinning triangle icon to collapse all the notifications from a particular app.

Critical notifications—like low battery warnings—will now still be sent even when Do Not Disturb is active and notifications are now shown even when in the Multitasking View. Plus, we've improved support for notifications that include markup—like bold and italics—and we removed the intrusive "Automatic Suspend" notifications that would sometimes prevent your device from sleeping.

## Panel

The Network indicator received some much-needed design attention and now offers a vastly-improved experience for using VPNs. You'll notice that most options now appear as circular toggle buttons with icons instead of a list of switches. This new design both saves space on devices with complex network configurations and shows the status of your various connections much clearer, including intermediate and error states. In the case of VPNs, you can now also activate multiple connections at once. We've also added quick access to toggling Airplane Mode, including a middle-click action on the indicator icon. Plus, we're now using a feature of Network Manager to automatically get better device names so you'll rarely see long and cryptic device names any longer.

<figure class="card" markdown="1">
![Network Indicator](/images/{{ page.slug }}/indicator-network.png){: width="580" height="326"}
<figcaption markdown="1">
Complex network configurations are handled more gracefully and VPN support has been entirely reworked
</figcaption>
</figure>

We’ve also improved the way Bluetooth devices are listed in the panel: they will now use any custom device names you've set up before falling back to more generic device names.

The Sound indicator was updated to use circle buttons and should no longer change size when skipping tracks. Muting should no longer affect monitor sources.

<figure class="card" markdown="1">
![Sound Indicator](/images/{{ page.slug }}/indicator-sound.png){: width="440" height="248"}
<figcaption markdown="1">
The Sound indicator now uses circular buttons
</figcaption>
</figure>

The Power indicator now always uses hours as its largest unit, for example it will say "26 hours remaining" instead of "1 day remaining" and we improved the accuracy of battery level icons.

Plus, we've updated icons in the Bluetooth, Network, Night Light, Notifications, and Sound indicators to be more consistently sized and with clearer disabled states.

## Other Design Improvements

In OS 7 we began the process of improving the design of our apps and operating system to be used on a wide range of displays from small laptops and tablets to large desktops, and when tiling apps side by side. We’ve continued that work into OS 7.1 in a couple of notable places. 

Several pages in System Settings have been redesigned for improved responsiveness on large and small displays, including Applications → Defaults and Applications → Startup, Desktop → Dock &amp; Panel, Displays → Night Light, Keyboard → Behavior, and Sound. And in several of these views we improved description text for more complicated settings.

<figure class="card" markdown="1">
![Installed apps in AppCenter](/images/{{ page.slug }}/appcenter-updates.png){: width="974" height="704"}
<figcaption markdown="1">
AppCenter's Installed &amp; Updates view makes better use of space on large displays
</figcaption>
</figure>

Our responsive work also continued in AppCenter, where App Info views were reworked to tighten up spacing and improve alignment. Special attention was put into making sure the most important information appears "above the fold", especially on smaller displays like in some laptops. And the Installed &amp; Updates view now uses a grid layout for installed apps, making better use of space on large displays.

<figure class="card quarter" markdown="1">
![Welcome in Onboarding](/images/{{ page.slug }}/onboarding-welcome.png){: width="485" height="443"}
![Style in Onboarding](/images/{{ page.slug }}/onboarding-style.png){: width="485" height="443"}
![Nightlight in Onboarding](/images/{{ page.slug }}/onboarding-nightlight.png){: width="485" height="443"}
![Automatic Updates in Onboarding](/images/{{ page.slug }}/onboarding-updates.png){: width="485" height="443"}
<figcaption>Onboarding features bolder typography and some new icons</figcaption>
</figure>

Onboarding also features several redesigned pages with some new icons and bolder typography. We now use the release wallpaper in a dynamically generated icon on the Welcome page, and previews in the Style view use the currently set wallpaper.

Plus, arrow shapes have been improved for many action icons across all apps and several icons now appear sharper when the dark style is selected.

---

# Get elementary OS 7.1

elementary OS 7.1 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 7.1 FAQ](https://github.com/elementary/os/wiki/OS-7.1-FAQ){: .button.flat }
[Download elementary OS 7.1][elementary.io]{: .button.suggested }
</div>

If you’re already on elementary OS 7, you’ll get the update to OS 7.1 alongside regular operating system updates. If you haven't already, open AppCenter and select _Update All_ to be upgraded.

[elementary.io]: https://elementary.io
[updates]: {{ site.baseurl }}/tags/#updates

