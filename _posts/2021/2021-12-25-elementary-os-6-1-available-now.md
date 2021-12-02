---
title: elementary OS 6.1 Available Now
description: Our biggest Christmas release yet
author: danrabbit
image: /images/elementary-os-6-1-available-now/card.png
tags:
  - odin
  - release

---

Just four months after the initial release of elementary OS 6, we're proud to announce OS 6.1 jam packed with new features, bug fixes, performance improvements, and more, all based on your feedback! If you're already an OS 6 user, most of this wrapup will be familiar to you as it includes an overview of all of the updates released since 6.0, but there are few new treats in your stocking too! Before we get to all the goodies, we'd like to quickly report that OS 6 has been downloaded from our website [over 226,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-08-10&to=2021-12-02&props=%7B%22Version%22%3A%226%22%7D)—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page.


## AppCenter

If you checked out AppCenter on release day and found it a little sparse, it's time to check again! App developers have been hard at work and you can currently find [90 curated apps](https://appcenter.elementary.io/) in AppCenter. We're also happy to report that many developers have been pushing out rapid and frequent updates to existing apps with new features and bug fixes, as they're in control of their own update schedule. Our shift from Debian packages to Flatpak for both curated and non-curated apps means we're able to lean more on Flatpak features and we've been using this as an opportunity to make AppCenter much more engaging and informative right from the start.

<figure markdown="1">
![AppCenter Home Page](/images/{{ page.slug }}/appcenter-home.png){: width="1408" height="895"}
<figcaption>The refreshed home page</figcaption>
</figure>

For example, we've largely reworked the home page with banners featuring the most recently released and updated curated apps in a multi-touch swipable carousel. We've also added up to twelve more of the most recently-updated apps directly below. Rather than just showing the app's icon and name, we now also show each app's summary and an install button—including the developer's recommended price if it's a monetized app. Since we enforce accurate update information for curated apps, this data is populated locally from the apps' AppStream data rather than from a remote API as before. The result of this work is a faster home page with over three times the apps displayed, as well as the ability to purchase or install several apps with far fewer clicks.

<figure class="constrained" markdown="1">
![Category view](https://user-images.githubusercontent.com/7277719/141206268-5505f96e-39e4-436e-970c-e72b6369d6cc.png)
<figcaption>Newly redesigned category view in AppCenter</figcaption>
</figure>

Category views (like Audio or System) are now shown with a more space-efficient grid view. We also separate paid, free, and non-curated apps (if you've added a third-party remote like Flathub) into their own sections within categories. In an effort to better surface the interesting apps being submitted, we've added a new Privacy & Security category, and apps categorized as "Amusements" will now appear in the Games category. We've also been working closely with third-party developers to ensure that their apps list a more complete set of categories in their metadata so that they appear in the correct category pages.

<figure class="half" markdown="1">
![AppCenter Non-curated App Info Page](/images/{{ page.slug }}/appcenter-report-card.png){: width="1408" height="895"}
![AppCenter Related Apps](/images/{{ page.slug }}/appcenter-related.png){: width="1033" height="607"}
<figcaption markdown="1">
**Left:** A non-curated app info page and its "report card" | **Right:** Other Flatpak apps from the same developer as the selected app
</figcaption>
</figure>

We've also spent significant time improving individual apps' info pages. Rather than displaying a generic "explicit" warning dialog when installing an app with certain content warnings, we show this information ahead of time at the top of the page. We differentiate between and inform about several content warnings including things like violence, language, and nudity as well as privacy-related topics like online interactions and data collection. And since we validate this information for curated apps but can't make any guarantees about non-curated apps, we also more clearly inform ahead of time when an app is not curated with an additional badge. This new section works like a content and privacy "report card" you can use to learn more about apps and make informed choices while also reducing the road blocks to installing the apps you want. We also now show apps from the same developer at the bottom of app info pages regardless of packaging technology used, meaning it works equally well for first-party, curated, and non-curated apps.

<aside markdown="1">
>This new section works like a content and privacy “report card”
</aside>

As part of our effort to make AppCenter a better experience on small displays, there is the new progress indicator when installing, removing, or updating apps. Instead of a separate progress bar, progress is now indicated in a compact way over the cancel button. This greatly improves AppCenter with smaller window sizes and fixes layout issues in views that show a lot of apps like the home page and when showing other apps by an author on the app info page.

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/appcenter-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="AppCenter" src="/images/{{ page.slug }}/appcenter-light.png" width="1020" height="667" />
  </picture>
<figcaption>Progress is now shown in a small progressbar seen top right</figcaption>
</figure>

As we continue to work on AppCenter for Everyone, we've reworked the Install button to ease into the future flow that will use a Flatpak authenticator to handle purchases; rather than having a dropdown arrow with a popover to change the price, we're now more clear about how "Pay What You Can" works and include changing the amount to pay in the payment dialog itself—and validated entries now show a green check and invalid ones show a red error so it's much clearer when card info has been entered incorrectly. And since we use this same widget on the home page, on app info pages, and in lists of apps, it's consistent everywhere.

<figure markdown="1">
![AppCenter payment dialog](/images/{{ page.slug }}/stripe-dialog.png){: width="568" height="379"}
<figcaption>Redesigned payment dialog</figcaption>
</figure>

Several more improvements permeate throughout AppCenter: fallback colors for apps that don't provide their own brand colors—including non-curated apps—now get a pleasant and more subtle look based on your selected system-wide accent color including better support for the dark style. We've also worked with downstreams like Fedora and Pop!_OS to test these updates using the same build flags they use, including adding automated testing to ensure things continue to build using the non-default options when we change the code for elementary OS. And since the redesigned home page relies on local data rather than a remote API, we no longer disable it on builds targeting Fedora or other non-elementary platforms; as a result, AppCenter is much more engaging and useful for any downstream. 

Finally, we've been putting a lot of work into the first run experience, especially with regards to apps from third-party stores like Flathub since we know many of you are sideloading. For example, apps from freshly-added remotes now show in AppCenter without needing to restart your device. We've also added a reminder about Sideload when searching returns no results with the same language that is used in the Welcome app. We now ensure that apps predictably default to installing per-user when selected from the home page, and both AppCenter and Sideload can now use system-wide installed app runtimes for per-user app installs; as a result, the first time you install a new app should now be an even faster, smaller download.

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/appcenter-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="AppCenter showing no results found" src="/images/{{ page.slug }}/appcenter-light.png" width="1169" height="729" />
  </picture>
<figcaption>AppCenter now reminds of Sideload when a search has no results</figcaption>
</figure>

If you're not running elementary OS but still want to get AppCenter apps, we've made it much easier with a recent update to our [AppCenter website](https://appcenter.elementary.io/): Free apps now include a "Download as Flatpak" button that will give you a Flatpak reference file which you can sideload on your operating system of choice. Enjoy!

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/badger-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Badger on AppCenter" src="/images/{{ page.slug }}/badger-light.png"/>
  </picture>
<figcaption>Free apps like Badger now show a button "Download as Flatpak"</figcaption>
</figure>

## The Desktop

You can now stash the picture-in-picture window by pushing it off screen—and we fixed a potential crash while changing wallpapers. We also fixed a handful of small visual issues across the desktop: legacy/server-side decorated windows should no longer have clipped shadows and we've fixed an issue that prevented the window border and shadow from being included in screenshots. We isolated the workspace "nudge" animation (when trying to navigate past the last workspace) to only show on the primary display, and we improved that nudge animation to work with the mouse wheel in addition to touchpads, touchscreens, and the keyboard.

### Quick Window Switching

Possibly the most obvious update to our window manager is the redesigned <kbd>Alt</kbd><kbd>Tab</kbd> quick window switcher.

Previously, quick window switching re-used the dock to show which app windows you'd switch between, and dimmed out the rest of the desktop to highlight just the newly-focused window. However, over time and based on a lot of real world feedback, we found that looking down at the dock—or even across physical space to the primary display in the case of multi-display users—was less intuitive and overloaded the dock's purpose. Dimming the desktop and visually focusing windows also meant a lot of flashing if you switched quickly which was inelegant at best, and could be an accessibility issue for people with certain types of photo-sensitivity. Thanks to [Aral Balkan](https://ar.al/2021/11/08/my-three-month-long-elementary-os-6-upgrade-adventure-in-three-parts-part-1-catts/), we kicked off a project to rework quick window switching—and the initial work has been released this month!

<figure class="half" markdown="1">
![Old](/images/{{ page.slug }}/gala-old.gif)
![New](/images/{{ page.slug }}/gala-new.gif)
<figcaption markdown="1">
**Left:** Old window switcher | **Right:** New window switcher
</figcaption>
</figure>

The new window switcher always shows centered on current display, making it much more likely to be near your gaze. It also features bigger icons, helping you more quickly identify apps. It includes window titles, helping to differentiate between multiple windows from the same app. We also ensured the new design helps you keep your context—and no longer flashes the screen. As a bonus, it follows both the dark style preference and your selected accent color, making your elementary OS installation feel even more personal.

### Dialogs

We also refreshed the interaction design of dialogs in elementary OS. First, you'll notice dialogs animate in from above on top of their parent window instead of shooting out from within their parent window. This helps reinforce that dialogs are a more transient interaction. We also dim the parent windows behind blocking modal dialogs to make it more clear which window it belongs to, and that the dialog needs to be addressed before proceeding.

<figure class="card" markdown="1">
![Dialogs](/images/{{ page.slug }}/dialogs.gif)
<figcaption>New dialog animation</figcaption>
</figure>

### Portals

We greatly improved the File Chooser portal that is used when apps request to open a file. We introduced new functionality like a New Folder action, a drop-down to filter the types of files shown, and an option to restrict the requesting app's access to a read-only version of the opened file. We also improved how the dialog is displayed in apps, fixing issues with focus and more reliably opening on top of the requesting app window.

<figure class="card" markdown="1">
![FileChooser dialog](/images/{{ page.slug }}/filechooser.png)
<figcaption>Improved file chooser, as used in Code</figcaption>
</figure>

In other exciting portal news, we also shipped a new AppChooser. You'll notice Flatpak apps which launch files in another app using the new design.

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/appchooser-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="AppChooser Portal" src="/images/{{ page.slug }}/appchooser-light.png" width="468" height="518" />
  </picture>
<figcaption>The new AppChooser portal</figcaption>
</figure>

### The Dark Style

You may recall that Cassidy [started the discussion](https://blog.elementary.io/the-need-for-a-freedesktop-dark-style-preference/) around the need for a FreeDesktop standard for the dark style a little over two years ago. We shipped the first iteration of an opt-in dark style preference in OS 6, and in 6.1 the dark style preference is now more widely respected across desktops.

<figure class="half card" markdown="1">
![Apps in light style](/images/{{ page.slug }}/fdo-color-light.png)
![Apps in dark style](/images/{{ page.slug }}/fdo-color-dark.png)
<figcaption markdown="1">
The dark style preference is now respected across desktops for GNOME and elementary OS apps
</figcaption>
</figure>

As before, this dark style preference is still opt-in for developers, which means it won't break apps that weren't tested against it. However, we're now using an agreed upon desktop-agnostic namespace in the Settings portal which works across application toolkits and desktop environments. What that means for you is that GNOME apps will begin respecting the dark style preference and we hope to see this compatibility spread to KDE apps and more in the future. It also means that those running AppCenter apps on GNOME 42 will have their dark style preference automatically respected on day one.

### And More

Along with all of the headlining features and fixes above, there are a few more minor updates. Shortcut Overlay will no longer crash if a keyboard shortcut has been set to blank. And on the Login & Lock screen, we now use the user's selected accent color for the logged-in checkmark for an additional splash of accent color.

The Notifications indicator will now use an app's name when a notification title isn't provided, bringing it in line with notification bubbles. The Power indicator includes a number of improvements such as showing the screen brightness level when scrolled, better matching the scroll behavior of other indicators, automatically showing the battery percentage when it's low, and showing "Fully Charged" when at 100% and plugged in. We fixed an issue with the network indicator that caused unwanted launches of the captive network assistant. The assistant also gained a new icon and is now shipped as a Flatpak for greater security. The Date & Time indicator now correctly updates the current day upon opening, and we fixed an issue with numbers becoming illegible when switching between the dark and light styles.

## Applications Menu

Now you can search right from the Applications Menu for bookmarked folders and locations like Downloads, Pictures, or even network shares. And following cross-desktop standards, this feature will work with whatever your default file manager is—whether or not it's the default elementary Files app.

<figure class="card" markdown="1">
![Bookmark search in Applications Menu](/images/{{ page.slug }}/bookmark-search.png){: width="888" height="689"}
<figcaption>Bookmark search in the Applications Menu</figcaption>
</figure>

The Applications Menu now shows a secondary-click menu on search result items, and we added support for launching apps on dedicated graphics on hybrid graphics systems (e.g. NVIDIA Optimus). Lastly, we've reworked the way the Applications Menu watches for changes in installed apps, so it should be more responsive about showing freshly installed-apps without a restart.

## Installer & Initial Setup

A couple of nice fixes landed in the Installer and Initial Setup that make it easier to set the name of your device. We now double check at install time that the default generated hostname is valid and you can change it to something you like more during initial setup. A formatted name like "Cassidy's StarBook" will be shown when possible—like in System Settings—and will automatically fall back to something more machine friendly like "Cassidys-StarBook" in places like Terminal.

<figure>
  <picture>
    <img alt="Initial Setup" src="/images/{{ page.slug }}/initial-setup.png" width="916" height="666" />
  </picture>
<figcaption>Initial Setup now helps you name your device</figcaption>
</figure>

We've also fixed a styling issue with "Unused" disk partitions in the custom install mode, added two-finger swipe to go back during Initial Setup, and changed the source of locale names to avoid some politically-charged naming of certain locales. Plus, we now hide the clock during Initial Setup since it often was covered

## System Settings

In addition to quite a few new features and improvements listed below, we spent some time resolving cross-platform issues in System Settings, which should make our desktop environment more easily portable to distros like Fedora and Nix OS. This also resulted in better support for locales that use 3-letter language codes and more reliable sidebar updates in User Accounts settings as well as some minor performance improvements.

### Online Accounts

In 6.0 we debuted a new Online Accounts system built around Evolution Data Server (EDS) and over the past several months we've rolled out quite a few improvements to our included productivity software. Firstly, we've make sure you can always navigate next when adding an account by pressing <kbd>Enter</kbd> and that you can close dialogs as expected with <kbd>Esc</kbd>. We fixed adding, editing, and removing lists in CalDAV apps like Tasks

Thanks to some helpful feedback from our community, we've made the process of detecting IMAP authentication methods much more robust. We also ensure the refresh interval for an IMAP account is set (which will let apps like Mail change this in the future). You can also edit existing IMAP accounts by selecting the pencil icon in its row.

<figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/onlineaccounts-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="System Settings → Online Accounts" src="/images/{{ page.slug }}/onlineaccounts-light.png" width="1044" height="740" />
  </picture>
<figcaption>IMAP accounts can now be edited in System Settings → Online Accounts</figcaption>
</figure>

### Displays & Scaling

In Display settings, we've fixed an issue that caused the "Use this display" switch to fail in certain multi-display setups. Changing display resolution should be quite a bit more convenient now since we now show resolutions with a different aspect ratio in a separate sub-menu. We've also tweaked the style of Displays settings to be slightly lower contrast in the dark style, and we fixed an issue that prevented display name tags from appearing on all workspaces.
 
 <figure>
  <picture>
    <source srcset="/images/{{ page.slug }}/displays-dark.png" media="(prefers-color-scheme: dark)">
    <img alt="Displays Settings" src="/images/{{ page.slug }}/displays-light.png" width="995" height="691" />
  </picture>
<figcaption>Resolutions with a different aspect ratio are now shown in a sub-menu</figcaption>
</figure>

To better support a wide variety of display sizes and resolutions, we also added more granular text scaling in the Desktop settings—and moved the text settings to their own page for clarity. As a reminder, text scaling in elementary OS affects both text and much of the UI while keeping pixel-perfect icons and strokes, so this update is a great alternative to fractional scaling for anyone with a display whose resolution sits in between the ideal loDPI and HiDPI ranges.

<figure class="half" markdown="1">
![New text scaling design](/images/{{ page.slug }}/text-scaling.png){: width="856" height="553"}
<figcaption markdown="1">
**Left:** Improved text scaling options
</figcaption>
</figure>

### Housekeeping

elementary OS has a Housekeeping feature where old temporary and trashed files can be automatically cleaned up to save space and help protect your privacy.

<figure class="half" markdown="1">
![Onboarding](/images/{{ page.slug }}/housekeeping-onboarding.png)
![Settings](/images/{{ page.slug }}/housekeeping-settings.png)
<figcaption markdown="1">
**Left:** Housekeeping in the Welcome app | **Right:** Housekeeping in System Settings
</figcaption>
</figure>

We improved Housekeeping with the addition of Downloads to the options, and a more clear and consistent design between both the Welcome app and System Settings.

### Sound

In the indicator, you'll notice new device icons to make it easier to find the right output. We also improved the scroll interaction on the volume slider to work with horizontal scrolling, and cleaned up invalid "analog" output devices that could appear in certain situations.

<figure class="half" markdown="1">
![Sound indicator](https://user-images.githubusercontent.com/7277719/140836056-d5cd00ad-8be4-4f43-a7e4-32a27d0f01bc.png){: .card width="750" height="473"}
![Sound settings](https://raw.githubusercontent.com/elementary/switchboard-plug-sound/5bc331aa0c099c40d5940d1211403e1397e39395/data/screenshot.png){: width="929" height="689"}
<figcaption markdown="1">
**Left:** Sound indicator with device icons | **Right:** Sound settings with similar icons
</figcaption>
</figure>

In Sound settings, you'll see similar but larger, full-color device icons to distinguish devices, as well as an easier-to-scan multi-line layout.

### Keyboard

In Keyboard settings, we improved the custom shortcuts view with a more straightforward design and menu for changing or deleting shortcuts, and added an on-screen keyboard switch to the Layouts tab.

<figure class="half" markdown="1">
![Custom keyboard shortcuts design](/images/{{ page.slug }}/custom-shortcuts.png){: width="909" height="601"}
<figcaption markdown="1">
Improved custom keyboard shortcuts design
</figcaption>
</figure>

For those of you using advanced keyboard input methods, we now ensure IBus automatically starts on login.

### And More

In addition to the major improvements above, we fixed an issue in Applications settings with setting the incorrect app for certain files types, and don't overwrite custom permissions overrides when unnecessary. We fixed a crash in the Network settings for some hardware. We've fixed an issue in Power settings that could sometimes cause problems with resuming from sleep, and added a switch to show or hide the battery percentage in the Panel. We added a new toggle for “Double-tap and move to drag” in Mouse & Touchpad settings. In User Accounts settings, we fixed an issue with updating permissions when enabling and disabling accounts. In the System page, we now display more information for certain graphics chipsets, including Intel® Xe Graphics. And we also improved the way we remember Bluetooth state on restart and when resuming from suspend.

## Mail

6.0 also featured a brand new version of Mail built around EDS instead of the Geary mail engine. We've been working hard to play catch up on the most important features from the old Mail and we've made quite a lot of progress!

Mail will once again automatically notify you when new messages arrive, even when the window is closed. There's also clever grouping of notifications so that if several messages come in at once, we'll only send one notification per account.

Conversations in the list view have a handy secondary-click menu again, and the next conversation in the list is automatically selected after archiving or deleting the current conversation. We've also moved the in-app notification for "Undo" to be less intrusive. Conversations with unread messages now use your accent color for their titles to stand out a bit more. We've added a new inline toolbar with a "refresh" button to manually fetch new messages and togglable filters for unread or starred conversations. And we make sure that conversations get resorted by time and date when new messages are received.

We've fixed a number of reported crashes and rendering errors, improved search performance and startup times, and improved issues around saving drafts and deleting messages with various mail servers including Outlook.com. We've improved handling of `mailto:` links, better ensure the correct "From" address on replies when multiple accounts are set up, sent messages will no longer be marked as "unread", and messages will use your local time in their headers. Mail also now provides the email portal for apps that support it (replacing the previous Contractor contract on elementary OS), making it easier for sandboxed apps to prompt you to start composing a message.

## Tasks

We shipped a number of improvements to Tasks: to prevent accidental task deletion, we've replaced the Delete shortcut key with <kbd>Ctrl</kbd><kbd>Backspace</kbd> and added a confirmation dialog when deleting a task list; we've improved performance in lists with lots of completed tasks; we prevent account name headers from being displayed multiple times in the sidebar; we now truncate long descriptions at the end instead of the beginning; we ensure tasks are saved when the description is removed; and finally, we improved cursor placement in descriptions when editing.

As a note, if you were having issues adding, editing, or removing lists, try removing and re-adding your CalDAV account in _System Settings_ → _Online Accounts_ to take advantage of the improvements made there.

## Calendar

We've greatly improved Calendar's reliability with regards to sending notifications, including fixes for the Notifications indicator, opening Calendar when clicking notifications, and sending notifications for upcoming events while Calendar is closed. Time zones have been a major focus as well with improvements around getting and saving time zone information, including Windows-style time zones in synced events, and plugging memory leaks related to fetching time zone data. Plus, we've improved handling of all-day events and we do a better job of getting calendar colors from online accounts.

## Web

We made the leap from Web 3.38 to 40.3 which brings quite a number of improvements including a redesigned tab bar, several performance and stability fixes, and of course rounded window corners!

The preferences dialog itself has been redesigned and now includes search. Managing search engines and passwords have been completely redesigned. A setting to disallow local storage is now included, and there's a new optional Google search suggestions feature that is off by default. Appearance settings now include the ability to add custom JavaScript. Fans of Firefox sync should note that this feature has moved from the preferences dialog to the "Import and Export" menu.

The new tab bar includes slick animations when opening, closing, and reordering tabs. Drag and Drop is much improved. When there are many open tabs, they can now be scrolled through quickly instead of individually paged with arrows. Closing tabs waits to resize like elementary apps. And the new tab bar fully supports touch screens. For a deep dive into the new tab bar, check out [Alex's blog post](https://blogs.gnome.org/alexm/2021/03/13/reinventing-tabs/)

## Camera

Previously, Camera's resolution had been reduced for performance reasons; in the latest version Camera will continue to use a more performant resolution in the preview, but will save full-resolution pictures. We fixed saving and restoring the window size. We resolved issues with some cameras being unavailable when multiple cameras are connected, and we now default to a working camera if multiple cameras are connected but one is unavailable.

## Photos

Now when you open a photo in the previewer, we focus the photo itself instead of the save button; this enables navigating with the left and right arrow keys right away. The actions for "Toggle Sidebar" and "Toggle Photo Info" have been moved from the secondary-click menu of certain views to the main menu button, hopefully making these customization options more discoverable. We also fixed a potential crash when importing photos with invalid date and time info and we fixed "rubberband" selection styling.

# Calculator

When Calculator starts up, we now focus the main text entry so that entering numbers with the keyboard works right away. We've also improved the experience with multiple windows: there's now a "New Window" action when secondary-clicking Calculator in the Applications Menu or Dock, and we fixed an issue with showing advanced controls so that it only affects the currently focused window. Lastly, we now show the correct window title in the Multitasking View.

## Videos

Videos now supports the two-finger-swipe to go back gesture and navigation code has been cleaned up a ton. Window titles should be more accurate when navigating. Also, we're now shipping Videos as a Flatpak which should resolve some reported issues with certain video codecs.
















### Files

We released a significant update to Files this month with a handful of fixes and improvements.

We've also released a handful of improvements to Files itself. Files now uses the Send Mail portal for emailing files, which should open compatibility up to more third-party email clients and work better across other desktops. The "Connect to Server" dialog now allows blank passwords for remote connections, e.g. for connecting to an SSH server via a private key instead of a password. We restored the multi-select capability of rubber-band style file selection, meaning you can drag-to-select a group of files, hold <kbd>Ctrl</kbd>, and drag to select an additional group of files. And lastly, we improved the drag-and-drop to the sidebar for bookmarks, ensuring drop targets show up in the correct places.

We fixed an issue where some audio files would have a thumbnail placeholder forever instead of falling back to the audio file type icon when they have no album art. We also made sure the overlay bar in the bottom right doesn't briefly appear when switching between bookmarks. The names of bookmarked folders will now properly update if your language was changed. And we removed the message about reporting issues when running Files from Terminal.

We've released a handful of fixes to Files this month. You can now open bookmarks in a new tab with <kbd>Ctrl</kbd> Click, we fixed dropping paths onto storage devices and network locations in the sidebar, we fixed restoring tabs after a system restart, we ensure Files doesn't deselect a file or folder when secondary clicking the blank space around it, an we now show the folder context menu when secondary clicking outside of a selection.

Files includes a fix for issues regarding renaming bookmarks in the sidebar as well as with the bookmark shortcut <kbd>Ctrl</kbd><kbd>D</kbd>. We've also resolved an issue where secondary-click context menus on the pathbar were sometimes too small for their contents, and an issue where color tags were missing when thumbnails are hidden.



### Code

In Code, we now distinguish between projects with the same name in the sidebar by including their parent folder. The project/folder search dialog now shows centered over the window, and when scrolling to search results, we overshoot the result slightly for better visibility. We also made the "visible whitespace" setting simpler and more clear with a switch instead of a drop-down. We're also now using the File Chooser portal provided by Files instead of the default dialog from GTK; as a result, opening files and folders from within Code will benefit from the recent improvements in the portal, and will be more consistent with Flatpak apps.

If you use the Terminal extension, we fixed the visibility of Terminal button on Welcome page, fixed some keyboard shortcuts affecting unfocused document instead of focused Terminal, ensure the Terminal is closed if shell exited, and create a new Terminal if it's re-opened with no shell.

We released a small update to Code this month with an improvement for those who tile windows, especially on smaller displays: we now hide the project chooser button when hiding the sidebar, allowing a smaller minimum window width. We also better ensure files created from the sidebar are automatically opened, and fixed a potential crash when creating new window by dragging and dropping a tab.








## Developer Platform

In tandem with our work on portals is a new version of our Flatpak platform. This update includes a new version of Granite which automatically supports the FreeDesktop dark style preference; there's no additional work needed from developers to support the new standard. We do advise developers who added a sandbox hole for AccountsService to their Flatpak manifest to remove this line as it is no longer needed.

<aside markdown="1">
>Developers don't need to do any additional work to support the new FreeDesktop dark style preference
</aside>

The new version of Granite also automatically uses the Settings portal for a couple other things like date and time settings. This fixes an issue with time picker widgets not respecting AM/PM vs 24-hour time format preferences, for example. Finally, we also released a small update to the system stylesheet to support the Hdy.Tabbar widget and with a fix that makes sure `.titlebar` with the `.flat` style class automatically inherit the background color of their containers.

ARM builds have been enabled for Flatpak. This means we can start building first-party and AppCenter apps for 64-bit ARM platforms like Pinebook Pro and Raspberry Pi 4 again. Stay tuned for more info on this as we continue the work.

<aside markdown="1">
>We can start building apps for platforms like Pinebook Pro and Raspberry Pi 4
</aside>

We fixed a couple of issues discovered in the system stylesheet; namely, the accent color in IBus candidate window and the font style for labels in header bars for Japanese characters. We updated the Network indicator to prevent blank lines in the list of VPNs. And as always, there are translation updates, code cleanups, and other under-the-hood improvements included with these updates across the OS and apps.

For developers, we added a `min_length` property for `Granite.ValidatedEntry` and released a new `Granite.HyperTextView` for navigable URLs in text views. On the icons front, we released new `preferences-desktop-font*` icons, additional sizes for `playlist-queue` and `emblem-downloads`, redesigned the PDF file type, and removed arrows from Copy and Paste actions. Lastly, we released version 6.0.4 of the Flatpak platform with the latest Granite, icons, and stylesheet updates.




## Hardware Compatibility

Thanks to upstream developers working on Ubuntu, we're now shipping a fix for an issue that prevented some computers from being able to boot, including Dell devices with UEFI and some other models. If you weren't able to boot the initial release of OS 6, give it another shot! If you were able to get OS 6 installed, you're not affected by this issue and you don't need to re-install. This latest build inherits all the other great hardware compatibility improvements included in Ubuntu 20.04.3 release as well. Thanks Ubuntu!

If you've had trouble with device drivers that rely on DKMS, AppCenter will now automatically pull in the required Linux kernel headers when installing them. We've also fixed an issue that was preventing our bootloader GRUB from correctly updating to use newer kernels, and you should see less of GRUB in general when starting your computer normally.
