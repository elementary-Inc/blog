---
title: elementary OS 7 Available Now
description:
author: danrabbit
image: /images/{{ page.slug }}/card.png
tags:
  - horus
  - release

hidden: 2023-01-31 17:00:00 UTC # 9 AM PST
---

It's been just over a year since we released elementary OS 6.1 Jólnir which brought new features and fixes based on your feedback, introduced new office productivity features, and expanded compatibility with a wide range of hardware. So far, OS 6.1 has been downloaded from our website [over 400,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-12-20&to=2023-01-31&props=%7B%22Version%22:%226.1%22%7D)—150,000 times more than 6.0—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page!

<figure class="card" markdown="1">
![elementary OS 7 Horus](/images/{{ page.slug }}/hero.png)
</figure>

Today we're proud to announce that OS 7, codenamed Horus, is available to download now and shipping soon on several high-quality computers. With OS 7, we've focused in on:

- Helping you get the apps you need
- Empowering you with new features and settings
- Evolving our developer platform

To get elementary OS 7 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

## Helping you get the apps you need

As always, AppCenter is the centerpiece of elementary OS. The primary purpose of any operating system is to support the apps that you use to work, play, and express yourself creatively. In the latest version of AppCenter we've worked on making app descriptions more engaging with more information, making it easier to update to the latest versions of apps, and improving support for sideloading and alt stores. We've also worked on improving AppCenter's responsiveness—making sure you can comfortably use it when tiling and on small displays as well as better using space on large displays.

<figure markdown="1">
![AppCenter at large and small sizes](/images/{{ page.slug }}/appcenter-responsive.png){: width="1628" height="913"}
<figcaption markdown="1">
AppCenter can be used comfortably while tiled or on small displays
</figcaption>
</figure>

We've completely rewritten the way navigation works in AppCenter and now support two-finger swipe gestures to navigate back. The entire app loads much faster and provides more feedback when running background tasks via an overlay bar in the bottom right or left corner.

### App Descriptions

The biggest change you'll notice when viewing app info pages is the improved emphasis on screenshots. Screenshot carousels now fill the width of the window, showing more screenshots at once. They can now also be accompanied by their own captions, which can help describe individual features as well as making pages more accessible to folks with vision-related disabilities. And finally each screenshot now sits on a card that uses the app's accent color, showing off more of the developer's personality.

<figure markdown="1">
![AppCenter's app info view](/images/{{ page.slug }}/appcenter-appinfo.png){: width="1708" height="1086"}
<figcaption markdown="1">
App Info views show more screenshots with captions and brand colors
</figcaption>
</figure>

Knowing how actively developed an app is and how engaged the developer is with their community is an important factor in deciding which apps to install. We now help you know what to expect by showing an icon when an app uses an older, unsupported platform as well as showing up to 5 recent releases and their release notes instead of just the latest release. We also now show links to resolved tickets in an app's issue tracker per release, so you verify that app developers will take your feedback into consideration.

### Getting Updates

Staying up to date with the latest versions of apps is something we hear often is very important to folks using elementary OS. Flatpak makes it simple for developers to publish app updates quickly and now you can get those updates automatically. If you'd still like to check for updates on your own time or want to force a manual refresh, there's now a handy menu option that you can use.

<figure class="constrained" markdown="1">
![AppCenter's  updates view](/images/{{ page.slug }}/appcenter-updates.png)
<figcaption markdown="1">
Operating system updates are now installed offline and app updates can happen automatically
</figcaption>
</figure>

AppCenter now also installs operating system updates offline, ensuring that important services are restarted correctly and avoiding odd crashes or version mismatches when updating. Packages are downloaded and prepared during your session and then quickly installed whenever you decide to restart, without forced or automatic shutdowns.

### Sideloading & Alt Stores

Sideloading apps and using alt stores like Flathub is a major feature of elementary OS and a competitive edge over closed platforms that only let you install apps from a locked down store. In this release we've made several improvements to smooth out the experience of using alt stores based on your feedback and the latest cross-platform standards.

<figure markdown="1">
![Sideload](/images/{{ page.slug }}/sideload.png){: width="562" height="350"}
<figcaption markdown="1">
The Sideload app makes installing Flatpak apps and configuring alt stores simple
</figcaption>
</figure>

There's no longer a warning dialog every time you install an app that's supplied by an alt store, instead we show an unobtrusive icon alongside the app's other content warnings letting you know that elementary hasn't reviewed this particular app.

<figure class="constrained" markdown="1">
![AppCenter's app info view](/images/{{ page.slug }}/appcenter-sideload.png){: width="1164" height="912"}
<figcaption markdown="1">
Even apps sideloaded from alt stores like Flathub can show brand colors
</figcaption>
</figure>

Apps from AppCenter could always use their own brand colors to make their app info pages feel unique and now apps sideloaded from alt stores can show brand colors too, thanks to the latest additions in the AppStream standard.

### Web Apps

<figure class="constrained" markdown="1">
![Sideload](/images/{{ page.slug }}/web-apps.png){: width="1122" height="866"}
<figcaption markdown="1">
iCloud Numbers running as a saved web app
</figcaption>
</figure>

In the theme of accessing the apps you need, we're shipping the very latest GNOME Web 43 which includes support for creating web apps which show in the applications menu. They can have their own settings including privacy controls and can even run in the background. Installed web apps can be managed from inside GNOME Web.

## Empowering you with new features and settings

<figure class="half" markdown="1">
![Categories view in Feedback](/images/{{ page.slug }}/feedback-categories.png){: width="640" height="500"}
![Apps view in Feedback](/images/{{ page.slug }}/feedback-apps.png){: width="640" height="500"}
<figcaption markdown="1">
Feedback helps you report issues and request new features directly to the developers
</figcaption>
</figure>

The ability to send feedback directly to developers, see development happen transparently, and receive fixes and new features as updates quickly is one of our greatest strengths over both proprietary platforms and traditional Linux distributions. The Feedback app is a critical component in beginning this loop, so this cycle we've brought some major improvements to it including instant launch times, much better coverage of installed apps, settings, and desktop components, and you can now access the Feedback app directly from the applications menu. We've also improved keyboard navigation and responsiveness for small displays, and added the ability to quickly double click a list item to launch.

### Installation, Initial Setup & Onboarding

We've done a decent amount of work this cycle on reducing the number of screens in the Installer and providing more information to help you make informed decisions. For example, we now warn about connecting to power when on battery using an infobar instead of a separate page and we've introduced a combined "Before You Install" page that includes warnings about things like virtual machines, developer builds, and system requirements all in one step. And speaking of virtual machines, we've resolved issues that made the installer window too large to be interacted with on some virtual machines.

During Initial setup, we now detect if you use the right mouse button for clicking and offer to switch to a left-handed mouse button order. There's also a new view that will appear if your device doesn't have network access instructing you how to get connected.

<figure class="half" markdown="1">
![Left-handed Clicking in Initial Setup](/images/{{ page.slug }}/initialsetup-lefthand.png){: width="914" height="664"}
![Network page in Initial Setup](/images/{{ page.slug }}/initialsetup-network.png){: width="914" height="664"}
<figcaption markdown="1">
**Left:** Left-handed primary click is now detected | **Right:** Initial setup guides you to connect to the Internet
</figcaption>
</figure>

Onboarding includes a new view for configuring automatic updates, as well as the addition of a "Sunset to Sunrise" option for the dark style.

<figure class="half" markdown="1">
![Choose Your Look view of Onboarding](/images/{{ page.slug }}/onboarding-styles.png){: width="497" height="664"}
![Night Light view of Onboarding](/images/{{ page.slug }}/onboarding-nightlight.png){: width="497" height="407"}
![Housekeeping view of Onboarding](/images/{{ page.slug }}/onboarding-housekeeping.png){: width="497" height="407"}
![Updates view of Onboarding](/images/{{ page.slug }}/onboarding-updates.png){: width="497" height="407"}
<figcaption markdown="1">
New features and settings are offered during onboarding like scheduled dark mode and automatic updates
</figcaption>
</figure>

### Office Productivity

Mail now sports a more-modern flatter design as a first-step towards work on making it more responsive. The unified inbox now supports Microsoft 365 accounts. And multiple potential crashes and freezes have been resolved.

<figure markdown="1">
![Mail](/images/{{ page.slug }}/mail.png){: width="1161" height="750"}
<figcaption markdown="1">
Mail now has a flatter design
</figcaption>
</figure>

Tasks now has offline support for newly created task lists and it makes sure to synchronize your remote lists when the network becomes available again. Plus it now sends notifications when a task is due. Online Accounts settings now also includes offline support for CalDAV accounts and the ability to choose a refresh rate for IMAP accounts.

A long asked-for feature, you can now choose to select folders with a single click instead of activating them in Files, Windows style. Quite a bit of work has gone into making sure multiple click modes are supported and working as expected. We've also spent extra attention dialing in the behavior of keyboard shortcuts, especially regarding copy/paste and selection shortcuts across different view modes and with different types of file selections.

<figure class="full-bleed" markdown="1">
![Files](/images/{{ page.slug }}/files.png)
<figcaption markdown="1">
Files now has a double-click option
</figcaption>
</figure>

Printer settings received special attention with several redesigns as well as new features like being able to clear the print queue per printer and a much clearer ink levels view.

<figure markdown="1">
![Printer Settings](/images/{{ page.slug }}/settings-printer.png){: width="1024" height="720"}
<figcaption markdown="1">
Redesigned printer settings with more control over the print queue
</figcaption>
</figure>

We're also shipping the latest Archive Manager and Document Viewer from GNOME 43. These releases improve support for dark mode, Flatpak portals like the native file chooser, as well as fix bugs and improve reliability.

## Multimedia

As music streaming services have emerged, there's been a shift away from the old paradigm of importing music from CDs, carefully curating playlists, and syncing music from your computer to mobile devices. We've received lots of feedback that Music wasn't meeting folks needs and the old code base was becoming prone to issues.

<figure class="card" markdown="1">
![Music 7](/images/{{ page.slug }}/music.png)
<figcaption markdown="1">
The new Music with a much more focused design
</figcaption>
</figure>

This cycle we've completely rewritten Music from scratch with a much more focused design built around quickly queuing up and playing individual audio files or your local music collection. We've heard that the new design is better for folks who just need a fast way to preview audio files that they're using in their other projects, as well as for folks that still carefully curate their own local music collection and don't want to compete with an app for fine grained control of their library's organization scheme.

The new Music 7 already has better support for reading track metadata such as album art, works as you'd expect with system-wide media controls, and can be tiled and resized to fit small and large displays. We're excited to shape future versions of this app with your feedback, so make sure you let us know what kind of features you'd like to see!

<figure class="card" markdown="1">
![The sound indicator](/images/{{ page.slug }}/panel-sound.png){: width="430" height="323"}
<figcaption markdown="1">
Videos can now be controlled from the sound indicator
</figcaption>
</figure>

Likewise, Videos now appears in the sound indicator alongside other media players. And in both System Settings and the Panel, we now use more information to assign accurate icons to audio devices.

### System Settings

In elementary OS, settings are meant to make the operating system more accessible to a wider range of people with various needs and ways of working.

<figure class="half" markdown="1">
![Power Settings](/images/{{ page.slug }}/settings-power.png){: width="1024" height="720"}
![Shortcut Settings](/images/{{ page.slug }}/settings-shortcuts.png){: width="1024" height="720"}
<figcaption markdown="1">
**Left:** New power profile management | **Right:** Redesigned shortcut settings
</figcaption>
</figure>

This release provides power profiles management, including a performance mode for devices that support it. Expect much improved battery life for mobile devices with Power Saver mode. And you can now scroll both horizontally and vertically on the power indicator to change display brightness.

We've added powerful features like the ability to set custom Terminal commands for each hotcorner and a redesign keyboard shortcuts settings makes it easier to disable shortcuts or revert them to defaults, as well as much better custom shortcut management. You can now also launch the Shortcuts app from the applications menu and we've added the option to open and close the Multitasking view using the Super key.

<figure markdown="1">
![Multitasking Settings](/images/{{ page.slug }}/settings-multitasking.png){: width="1024" height="720"}
<figcaption markdown="1">
Multitasking settings with per-corner Terminal commands
</figcaption>
</figure>

Keeping your device secure is paramount, which is why we've added a new option to forbid new USB devices from connecting while your device is locked, we've updated network settings and the network indicator to support WPA3 networks, and we've added support for offline firmware updates.

Our localization team has also been hard at work and Central Kurdish is now available as an installable language, we now support installation and removal of languages with 3-letter codes, and we support the Rime input method for Chinese

### Performance

I want to make a special note here about performance. In just about every section I could have individually written about performance over and over again. The team has spent quite a bit of time tracking down slowdowns, reworking old code, and optimizing to make everything happen as quickly and responsively as possible and in the most extreme scenarios. I can't emphasize enough how big a part reducing latency plays in our vision for empowering you to do your best.

## Evolving our developer platform and design language

We always try to strike a balance between staying up on modern design concepts while avoiding trendiness to create our unique style. With OS 7 you should notice a push towards responsive app design—ensuring that apps can be used on both small and large displays—and a big change to unify the design of app icons. Part of this shift is enabled by using the latest technology in our platform like Gtk 4 and we're motivated by making sure elementary OS runs well on the kinds of devices that power your everyday life.

### Iconography

Nearly all app icons have been redesigned to be based on a uniform tile shape with some elements overlaid or layered. The new design language for app icons feels more modern while still retaining the pixel-fitted charm you're used to and allowing for playful expression. We hope this change in direction makes it simpler for app developers to create high quality app icons that feel like they fit in on elementary OS.

<figure markdown="1">
![App Icons](/images/{{ page.slug }}/icons-apps.png)
<figcaption markdown="1">
Redesigned app icons
</figcaption>
</figure>

In addition to modernizing app icons, several color and symbolic system icons have been updated to match the latest brand colors, to use the same tile base shape as app icons, to soften out shapes, and to improve legibility as always.

<figure class="half" markdown="1">
![Color Icons](/images/{{ page.slug }}/icons-color.png)
<picture>
  <source srcset="/images/os-7-available-now/icons-symbolic-dark.png" media="(prefers-color-scheme: dark)">
  <img alt="Symbolic Icons" src="/images/os-7-available-now/icons-symbolic-light.png"/>
</picture>
<figcaption markdown="1">
System icons have been updated with softer corners, new brand colors, and more
</figcaption>
</figure>

There's now also an Icon Browser app available in AppCenter where you can see all of the icons shipped with the elementary platform. You can search or view icons by category as well as see what sizes and styles an icon comes in and even get a quick code snippet to use in your app.

<figure class="constrained" markdown="1">
![Icon Browser](/images/{{ page.slug }}/iconbrowser.png)
<figcaption markdown="1">
The new Icon Browser app
</figcaption>
</figure>

### Gtk 4 & Responsive Design

Building great modern apps requires a modern toolkit. Gtk 4 brings a ton of performance and rendering improvements on its own as well as features that make it easier to make apps responsive and animated. We're excited to push the limits of the toolkit and we'll be staying up to date with point releases of Gtk 4 as part of our Flatpak platform. Several apps and desktop components have already been ported to Gtk 4 such as Calculator, Sideload, Shortcuts, Music, and Onboarding and several more Gtk 4 ports will land throughout the life cycle of OS 7.

As mentioned a few times already, a big part of our design language going forward will be informed by making sure apps run great on both large and small displays. More and more we do our computing from tablets and mobile devices as well as our desktops and notebooks. With OS 7 we've worked to make apps much more tile-able on desktops as well as notebooks with even very small display resolutions. Apps like AppCenter and Music work much better when space constrained and efforts here have even resolved issues in virtual machines, for example. Expect more updates throughout the life cycle of OS 7 working towards responsiveness across the entire operating system.

### Granite

The latest version of our app framework Granite as well as our system stylesheet have been updated to support Gtk 4 and come with a host of new features and API changes to make building apps quick and straightforward.

In Gtk 4, style class constants have moved from Gtk itself into the platform frameworks. This means that all of the supported style class constants in the elementary stylesheet are now provided by Granite. This includes classes you're familiar with like the ones for setting text colors as well as the ones for setting background colors on sidebars or in views, plus some new ones like `RICH_LIST` for setting up padding and margins on ListBoxes.

A new Granite.Placeholder widget was introduced to replace AlertView and Welcome with a single more flexible widget. It supports all the usual cases like welcome screens with buttons, embedded alerts, and placeholders for lists. It supports markup in descriptions and you can even uses style classes like `ACCENT`, `WARNING`, or `ERROR` to automatically color title text.

Plus, widgets have been reworked to set all of their margins and padding from Gtk.CSS—meaning they scale appropriately with the system text size—and several widgets have been made more responsive for large and small displays.

Every release comes with removals and this migration to Gtk 4 comes with quite a few of them. We're excited to remove several utilities that are better supported in Gtk and GLib upstream, including the Settings class, Logging, Command Launching, several drawing functions now covered by Gtk.CSS, DynamicNotebook since you can now get a great tab bar widget from Adwaita, and others. In each case we looked at existing apps and made sure they could migrate to Gtk 4 without losing functionality and in many cases their code was made more robust and more simple by using functions provided by upstream libraries.

### Tools

Code has also been the focus of responsiveness efforts and can now be tiled even on tiny notebook displays. The first changes you might notice are the full-height project sidebar and the new elementary light and dark styles for the source view. Code now also optionally follows the system-wide dark style preference.

<figure class="half" markdown="1">
![Code in light mode](/images/{{ page.slug }}/code-light.png){: width="1173" height="703"}
![Code in dark mode](/images/{{ page.slug }}/code-dark.png){: width="1173" height="703"}
<figcaption markdown="1">
Code in light and dark styles
</figcaption>
</figure>

Both Find on Page and Find in Project are now available from the app's menu instead of in the headerbar and they both now support regular expressions. Project-wide searches are now also pre-filled with the selected text and the number of search results is now present in the search bar. Options for hiding and showing panels are now all present in a compact set of linked buttons in the app's menu as well. Hidden folders are now shown in your project's tree in the sidebar and manually selecting a project will hide tabs associated with other projects.

<figure class="half" markdown="1">
![Terminal in light mode](/images/{{ page.slug }}/terminal-light.png){: width="789" height="557"}
![Terminal in dark mode](/images/{{ page.slug }}/terminal-dark.png){: width="789" height="557"}
<figcaption markdown="1">
Terminal in light and dark styles
</figcaption>
</figure>

Terminal gains the ability to both follow the system dark style preference as well as create custom color palettes. The new default light and dark styles are now fully opaque and have been updated to match the latest upstream values from the Solarized themes for improved legibility. We've also added the keyboard shortcut <kbd>Alt</kbd> + <kbd>1—9</kbd> for switching tabs and you can quit Terminal with <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Q</kbd>

## Special Thanks

There are tons of other small improvements, bug fixes, and more that didn't make it into this release blog post. I'd like to give a special thanks to our volunteer community for their continual commitment to making a great open source operating system. I'd also like to particularly call out our localization team that works hard to make every release available in dozens of languages, including right-to-left languages, Asian character languages, and more. This release also wouldn't have been possible without the work of developers running Pantheon on other distros like Fedora and NixOS and their participation upstream. And speaking of upstreams, I'm always grateful for the work that goes into the Ubuntu releases that we build upon. I'm very proud of what a diverse community can build together and this release is definitely something to be proud of. Thank you all so much for being a part of it!

---

<figure markdown="1">
![elementary OS 7 Horus](/images/{{ page.slug }}/card.png)
</figure>

## Get elementary OS 7

elementary OS 7 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 7 FAQ](https://github.com/elementary/os/wiki/elementary-OS-7-FAQ){: .button.flat }
[Download elementary OS 7][elementary.io]{: .button.suggested }
</div>

### Devices

Our hardware retailers [Laptop with Linux], [Slimbook], and [Star Labs] will all offering elementary OS 7 out of the box soon. Visit retailers' individual sites for more information.

<div style="text-align: center" markdown="1">
[Shop Devices][store]{: .button }
</div>

[elementary.io]: https://elementary.io
[Laptop with Linux]: https://laptopwithlinux.com/?ref=36&utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Slimbook]: https://slimbook.es/?utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Star Labs]: https://starlabs.systems/?rfsn=4227837.e8f025
[store]: https://store.elementary.io/
