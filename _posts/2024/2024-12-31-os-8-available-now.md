---
title: elementary OS 8 Available Now
description: 
author: danrabbit
image: /images/os-8-available-now/card.png

tags:
  - circe
  - updates
  - release
---

Today, we're proud to announce that OS 8 is available to download now and shipping on several high-quality computers.

<figure class="card" markdown="1">
![elementary OS 8](/images/{{ page.slug }}/desktop-onboarding.png)
</figure>

With OS 8, we've focused in on:

-
-
-

To get elementary OS 8 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---




# Privacy, Security &amp; Consent

Time spent on your computer should be as free of stress and anxiety as possible. When computers act in ways that are unpredictable or leave you vulnerable, it can be deeply frustrating. Over the past several years we've been building features to improve the trust relationship with your computer by requiring your explicit informed consent and disallowing untrustworthy behavior on a technical level. We've done that by embracing technologies like Flatpak and Portals which confine apps to a sandbox, and now we're extending that story with both new settings to put you in control of the system features apps can access and a new Secure Session powered by Wayland.

<figure markdown="1">
![Application Portals](/images/{{ page.slug }}/portals-screenshot.png)
<figcaption markdown="1">
In the Secure Session apps need your explicit permission to see the pixels on your display
</figcaption>
</figure>

On the lock screen, you'll now see a gear menu next to the password field that gives you the option of Classic or Secure sessions. If you select the Secure Session, elementary OS will use Wayland, a modern and secure method for apps to draw themselves and accept your input. In the Secure Session, apps will be more restricted and will require your consent for system features. When an app wants to listen in the background for your keystrokes, take a screenshot, record the screen, or even pick up the color from a single pixel, you will be asked first to make sure that it's okay. The Secure Session also comes with other modern features like support for Mixed DPI modes—A hotly requested feature for folks using a HiDPI notebook or tablet with a LoDPI external display—and improved support for multi-touch gestures on touch screens and tablets. You might also experience improved performance and smoothness, especially on low-powered hardware.

<aside markdown="1">
>OS 8 will use the Classic Session by default and apps will work and behave as they always have
</aside>

Portals are the standardized system interfaces that apps use to access features in a way that respects your privacy and requires your explicit consent. Four new Portals are now supported in OS 8: Color Picker, Screenshot, Screencast, and Wallpaper. These Portals are essential for enabling modern apps to work in the Secure Session when they don't have direct access to the pixels on your display. Since some apps haven't yet made use of the Portals required to operate under the Secure Session, OS 8 will continue to use the Classic Session by default. Apps will work and behave as they always have there, with the same level of system access you're used to from OS 7 and before. If you rely on certain accessibility features, you may find that those are not yet available under the new Secure Session as well. However, we highly encourage you to give the Secure Session a try and you might be surprised to find that the apps and features you use are already compatible.

<figure markdown="1">
![Application Settings](/images/{{ page.slug }}/settings-applications.png)
<figcaption markdown="1">
System Settings → Applications has expanded options
</figcaption>
</figure>

Application settings has an all-new design that expands your control over permissions. We now support adjusting the run-time permissions in Flatpak's Permissions Store—these are set when an app explicitly asks for your permission to access a feature while it's running. So if you've previously denied an app access to run in the background or granted an app permission to set the wallpaper, you can change your mind at any time and adjust permissions here. We've also adjusted the language of install-time permissions—aka sandbox holes—to be more clear that these represent advanced system access and the implications of adjusting them. Plus the descriptions of several individual items were changed based on your feedback to use less technical language. And app permission pages now show the app's icon and description.

# Getting Apps You Need &amp; Staying Up to Date










we're now shipping Flathub as an available Flatpak remote. This means you will be able to access both apps made for elementary OS and cross-platform apps for Linux out of the box.

Pages now draw their own individual headers, which means we can show more contextual controls and have more design freedom. You'll notice that options related to updates have now moved to the Updates &amp; Installed Apps page, for example. On App info pages, main action buttons like Install and Open are now always available from the headerbar, and when you scroll past an app's banner a smaller icon and app title will appear.

<figure class="third" markdown="1">
![AppCenter home page](/images/{{ page.slug }}/appcenter-home.png)
![AppCenter updates page](/images/{{ page.slug }}/appcenter-updates.png)
![AppCenter app info page](/images/{{ page.slug }}/appcenter-appinfo.png)
<figcaption>AppCenter has a flatter design where each page has unique headerbar contents</figcaption>
</figure>

The links section of App Info pages has also been redesigned, featuring colorful iconography and an expanded set of supported links. We now show a Sponsor link for apps who monetize outside of AppCenter and we show a link directly to the app's source code for apps that provide it.

Plus we've made a ton of cleanups, bug fixes, and performance improvements, especially around updates. And AppCenter now starts much faster








Instead of being a part of updates in AppCenter, system updates now live in the System page of System Settings. The new updates mechanism is super fast and includes an option to download updates automatically. It will also let you know explicitly if security updates are part of the updates package.

<figure markdown="1">
![Operating System view of System Settings](/images/{{ page.slug }}/settings-system.png)
<figcaption markdown="1">
System updates now live in System Settings and can be updated automatically
</figcaption>
</figure>

There's a few reasons why we would want two separate update mechanisms in elementary OS. Under the hood, apps in elementary OS are Flatpak packages and system packages are managed by PackageKit. Flatpak apps are sandboxed from the system and can be reliably updated while your computer is running. System packages are best installed offline, when your computer restarts, to make sure services are restarted correctly and to prevent issues. By splitting apart the updates experience, it is much clearer which updates will require you to restart your computer: app updates in AppCenter will never require a restart, while system updates in System Settings will always require a restart. It also makes the underlining code much less complex and speeds up processes like checking for new updates. It also means an error in one system won't cause updates in the other system to fail. Overall the updates experience in OS 8 will be faster, more reliable, and easier to understand, as well as being easier to automate.

Now that System Updates and Drivers have moved to System Settings, AppCenter has become Flatpak only! This greatly reduces code complexity and improves stability and performance. Plus it will make it easier for us to introduce new features in the future. Since OS Updates are now handled in System Settings, we've also removed that functionality from AppCenter which greatly improves performance and has enabled us to really simplify some of the backend code here.

Plus, you can now opt-in to automatic OS updates during Onboarding and automatic App updates are now opt-out.

A new option to the system shutdown dialog so you can choose to skip a pending update, even when automatic updates are enabled.

<figure markdown="1">
![Shutdown Dialog](/images/{{ page.slug }}/shutdown.png)
<figcaption markdown="1">
You can choose to skip updates when shutting down or restarting
</figcaption>
</figure>










# Multitasking &amp; Window Management

We've added support for horizontal swipe gestures for switching windows

option to disable hotcorners for workspaces with fullscreen apps

A small visual change, when switching workspaces docks and panels will no longer move with the switch. made sure that there's audio (or visual depending on your settings) feedback when we're unable to cycle workspaces in response to the keyboard shortcut.

Option to switch workspaces by scrolling over the panel

A new Dock rewritten from scratch. Uses the latest technology. Renders on the GPU for better performance. Made for Wayland. Based on survey

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "2021-ui-study-results-dock-multitasking" | first %}
{% include featured.html post=post %}
</div>

When multiple windows of the same app are opened, selecting that app's icon in the dock will open a window spread instead of hiding those windows.

Focusing a single open window of an app on click instead of opening new windows

We've also implemented a middle-click system that is aware of the FreeDesktop.org SingleMainWindow app launcher hint, so we can more reliably open new app windows when middle-clicking an app's icon.

The end result is a much more predictable experience that is centered on bringing you to the app you've clicked and an improved workflow for multi-window apps.

you can now launch pinned apps with <kbd>Super</kbd> + <kbd>1­</kbd>—<kbd>9</kbd>, a hotly requested feature.

reveal from any part of the screen edge

# Inclusivity &amp; Accessibility

Notifications now appear on the left for RTL languages

implemented the accessibility interface in the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher

<figure markdown="1">
![Onboarding](/images/{{ page.slug }}/onboarding.png){: width="497" height="438"}
<figcaption markdown="1">
Navigation in Onboarding has been rewritten for improved accessibility and with a neat progress bar
</figcaption>
</figure>

On the heels of some of our recent accessibility work, I'm proud to say that navigation in Onboarding has been rewritten for much improved keyboard navigation and screen reader compatibility. This was a show stopper when [Florian](https://www.twitch.tv/ic_null) took [a look at OS 8 in June](https://www.youtube.com/watch?v=7jOB4lZH3AE). Onboarding is such an important part of introducing a new operating system and making sure people new to elementary OS have a great time, so I'm particularly glad to improve this first impression for folks with vision-related disabilities.

And we've improved screen reader support in Initial Setup &amp; Onboarding

Illustrations in Notifications and Display settings are now higher contrast

If you're not a fan of overlaid scrollbars that disappear when not in use, there's a new setting to always show scrollbars in Desktop → Appearance

# Settings &amp; Customization

<figure class="card" markdown="1">
![Quick Settings](/images/{{ page.slug }}/quick-settings.png){: width="256" height="209"}
<figcaption markdown="1">
Quick Settings joins the panel
</figcaption>
</figure>

Quick Settings has also made it into the default package selection, replacing the Session and Accessibility indicators. It also currently provides toggles for Dark Mode and, when running on a device with an accelerometer, Screen Rotation Lock. This sets the foundation for including more quick toggle features as well as helps us clean up extra panel indicators.

System Settings got an icon redesign. Settings panes are now in charge of drawing their own window controls, which means several settings have already been updated to use a more modern paned design and others are able to use space more efficiently in their own way. You can expect further design refinements to continue to land throughout the OS 8.x cycle

<figure markdown="1">
![System Settings app icon](/images/{{ page.slug }}/settings-icon.png){: width="128" height="128"}
<figcaption markdown="1">
System Settings has a new app icon
</figcaption>
</figure>

Search in System Settings has been improved to return more relevant results and the titles of those results now reflect both the exact setting name they are matching and the path to that setting.

<figure markdown="1">
![System Settings search](/images/{{ page.slug }}/settings-search.png)
<figcaption markdown="1">
Search in System Settings now ranks results better
</figcaption>
</figure>

Redesign of Applications settings. The new split-paned design brings it in line with other settings pages and makes navigating much faster by exposing the list of installed apps at the top level of navigation.

Shortcuts settings now include a new "Keyboard Layouts" section where you can set a custom shortcut to change keyboard layouts as well as change the shortcuts for emoji and unicode typing modes

And some cleanup was done in Mouse &amp; Touchpad settings to make layouts more responsive, provide additional explanation text, and improve screen reader support.

Display settings received a big update to the way we do arranging and snapping which should be much smoother and more reliable with 3 displays.

<figure markdown="1">
![Power Settings](/images/{{ page.slug }}/settings-power.png){: width="678" height="901"}
<figcaption markdown="1">
System Settings → Power has new options and shows battery charge status
</figcaption>
</figure>

Power settings now shows charging level and status for internal batteries and theoretically supports multiple internal batteries—though I'm not sure that's been tested so please send feedback if you have a device with multiple internal batteries. You can also now choose to automatically set different power profiles based on whether your device is plugged in or on battery power. We've cleaned up some old code here quite a bit along the way and solved some issues with system hangs while getting permission for lid close settings.

And power modes can also now be quickly changed from the power indicator.

<figure class="card" markdown="1">
![Power Indicator](/images/{{ page.slug }}/indicator-power.png)
<figcaption markdown="1">
Power modes now appear in the power indicator
</figcaption>
</figure>

network settings now shows the name of connected wireless networks in the sidebar and Automatically select active network when opening

<figure markdown="1">
![Network Settings](/images/{{ page.slug }}/settings-network.png)
<figcaption markdown="1">
System Settings has a new modern design
</figcaption>
</figure>

Network Indicator was released and now shows cellular modems as toggle buttons like it does with other devices.

<figure class="card" markdown="1">
![Power Indicator](/images/{{ page.slug }}/indicator-network.png)
<figcaption markdown="1">
Cellular modems now show as toggle buttons
</figcaption>
</figure>

The Do Not Disturb setting in Notifications settings no longer blocks the whole view and we've updated the design of this pane to better reflect modern design patterns and support RTL language layouts

<figure markdown="1">
![Notification Settings](/images/{{ page.slug }}/settings-notifications.png)
<figcaption markdown="1">
Do Not Disturb no longer blocks Notification settings
</figcaption>
</figure>

A new paned design has landed for Desktop settings. This also includes wallpaper previews on the "Appearance" page. You'll notice that the "Dim Wallpaper With Dark Style" option has also moved to the Appearance page where you can see a preview of its effect.

<figure markdown="1">
![System Settings → Desktop → Appearance](/images/{{ page.slug }}/appearance.png)
<figcaption markdown="1">
Desktop settings have been redesigned
</figcaption>
</figure>

System got a redesign of external links similar to the one in AppCenter, with clearer help and documentation links as well as a better call for contributions.

<figure markdown="1">
![](/images/{{ page.slug }}/settings-system.png)
<figcaption markdown="1">
Operating System settings has a redesigned links section
</figcaption>
</figure>

Locale settings with a new setting for automatically selecting the temperature unit based on locale, fixed freezing while getting advanced permissions, and it will no longer prompt system administrators for a password unnecessarily for setting the system language. Plus we made some improvements to error handling and other feedback.

Language &amp; Region settings now has searchable dropdowns. We've also received some feedback from some folks that indicates they were looking here for Keyboard Layout or Date &amp; Time settings, so we more clearly link to both of those locations to help you find what you're looking for.

# The Desktop

We're also making a major change to our default keyboard shortcuts. Pressing <kbd>⌘</kbd> will now open the Applications menu instead of the Shortcuts overlay and <kbd>⌘</kbd> + <kbd>Space</kbd> will now switch keyboard layouts by default. This brings us more in line with the defaults from other desktops and operating systems and will hopefully be more comfortable for folks who rely on these shortcuts. Of course you can always change the <kbd>⌘</kbd> key behavior and keyboard shortcuts in general in System Settings → Keyboard.

and sound change confirmations will no longer appear over the sound indicator if it's open.

# Design

Gave attention to cursors and introduced more color into their design. This resulted in an almost complete redraw of our cursors and closed several old issue reports. We also got new, colorful "Find" icons as well as a new design for the "Save As" icon.

<figure markdown="1">
![New Cursors](/images/{{ page.slug }}/cursors.png){: width="192" height="192"}
<figcaption markdown="1">
Cursors have been almost completely redesigned with more color
</figcaption>
</figure>

We have two new wallpapers to share, ["A Large Body of Water Surrounded By Mountains"](https://unsplash.com/photos/a-large-body-of-water-surrounded-by-mountains-Dxod5pdRtsk) by [Peter Thomas](https://unsplash.com/@lifeof_peter_) and ["A Trail of Footprints In The Sand"](https://unsplash.com/photos/a-trail-of-footprints-in-the-sand-of-a-beach-A9mr3TPoj0k) by [David Emrich](https://unsplash.com/@davidemrich). Both of these images have been slightly edited for use as wallpapers in elementary OS and are distributed under the permissive Unsplash license.

Plus, opaque panel styles received some attention and now have a soft shadow 

<figure class="card half" markdown="1">
![Panel in light style](/images/{{ page.slug }}/panel-light.png)
![Panel in dark style](/images/{{ page.slug }}/panel-dark.png)
<figcaption>The Panel's opaque styles now have a soft shadow</figcaption>
</figure>

The Lock Screen now features a larger and bolder clock and it looks really great with our new default wallpaper for OS 8! The Login &amp; Lock Screen now features a blurred background similar to the Multitasking View

The Login &amp; Lock screen now has a smoother fade in animation

<figure class="card" markdown="1">
![The new Lock Screen](/images/{{ page.slug }}/lock.png)
<figcaption markdown="1">
A larger and bolder clock on the Lock Screen
</figcaption>
</figure>

<figure class="card" markdown="1">
![Login &amp; Lock Screen](/images/{{ page.slug }}/greeter.png)
<figcaption>The Login &amp; Lock Screen now shows a blurred version of your wallpaper in the background</figcaption>
</figure>

The Multitasking View has seen a number of design updates, the most noticeable of which is that instead of a plain dark grey background, it now features a blurred version of your wallpaper that is either lightened or darkened for light and dark modes respectively. You'll also notice that the workspace cards now have rounded corners and the switcher UI at the bottom of the screen has been updated for light and dark modes as well.

<figure class="card half" markdown="1">
![Multitasking View in light mode](/images/{{ page.slug }}/multitasking-light.png)
![Multitasking View in dark mode](/images/{{ page.slug }}/multitasking-dark.png)
<figcaption>Multitasking View now features a blurred background and an updated switcher UI design</figcaption>
</figure>

## Hardware Support

Pipewire

Lock Screen will respect your orientation lock settings

If you have a mixed-dpi setup—like a HiDPI laptop or tablet and a LoDPI external monitor—You can now set per-display scaling in the Secure Session thanks to [Leonhard](https://github.com/leolost2605).

Plus, we fixed a missing icon for some wireless headphones in Bluetooth settings.

Driver management has moved to System Settings → System. The new design for drivers should be more in line with how drivers are managed on other operating systems and be easier to work with

<figure markdown="1">
![System Settings → System → Drivers](/images/{{ page.slug }}/drivers.png)
<figcaption markdown="1">
Drivers are now managed from System Settings
</figcaption>
</figure>

OS 8 also includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.8

## Updated Apps

Web 46 brings a new flatter design and tons of bug fixes. Document Viewer gets the latest bug fixes while Archive Manager now uses GTK 4.

## Font Viewer

We're also now shipping Font Viewer as a Flatpak app. This means we can continually ship the latest GNOME Font Viewer in elementary OS built against our Flatpak runtime so that it fits in stylistically. The new Fonts looks fantastic and has much better performance, and it will continue to receive updates just like our other apps shipped as Flatpak. fixing a styling regression, ensuring we can continually ship the latest version of Font Viewer throughout the OS 8 life cycle, and that it can be automatically updated without requiring a system restart.

<figure markdown="1">
![The Fonts app](/images/{{ page.slug }}/fonts.png)
<figcaption markdown="1">
The updated Fonts app is available from AppCenter
</figcaption>
</figure>

## Photos

Photos 8 has been released to AppCenter as a Flatpak app. This means you can continue to receive updates to Photos by installing the Flatpak version from AppCenter even on older versions of elementary OS, and Photos is now [easily available](http://flatpak.elementary.io/repo/appstream/io.elementary.photos.flatpakref) to folks running Linux distributions other than elementary OS.

## Videos

<figure class="half" markdown="1">
![Videos player view](/images/{{ page.slug }}/videos.png){: width="1045" height="605"}
![Videos library view](/images/{{ page.slug }}/videos-library.png){: width="1045" height="605"}
<figcaption>Videos has a new modern and minimalist design</figcaption>
</figure>

Videos now sports a more modern and minimal design which is especially apparent on the player page. On the library page it uses larger landscape format thumbnails and the app now follows the system light and dark style preference. The upgrade to GTK4 also brings performance improvements. Major shoutouts to [Leonhard](https://github.com/leolost2605) for his work modernizing this code base.

Videos—like all of our Flatpak apps—is of course also available to download as a Flatpak for folks running Linux distros other than elementary OS:

<div style="text-align: center" markdown="1">
[Download Videos as Flatpak](https://appcenter.elementary.io/io.elementary.videos/){: .button.suggested }
</div>

## Mail

Email aliases have arrived in Mail! You can now secondary click on an account in the sidebar and select "Edit Aliases…" to configure them. Plus Mail now also handles replying and forwarding to the correct address for senders who use aliases. And bugs related to certain emails blanking or certain attachments not downloading have been fixed. Shoutouts to [Leonhard](https://github.com/leolost2605) for his work here.

## Music

Music can now open individual audio files from within the app instead of requiring you to open them from within Files and it gains the now-familiar sticky toolbar style when scrolling in the queue.

---

# Developer Platform

The elementary Flatpak Platform 8 has been released and is available now in the AppCenter Flatpak remote. If you're an app developer, that means you can update your app to the latest Platform today! We recommend doing so as soon as possible so that your app doesn't have an "Outdated" badge next to it in AppCenter on release day.

Platform 8 is based on the GNOME 46 platform and includes all of the same library updates as well as the latest Granite, elementary Stylesheet, and elementary Icons. Plus we're now including LibPortal, a library that makes it easy to use platform APIs for things like background &amp; autostart, taking screenshots, and setting wallpapers. Platform 8 includes the latest LibAdwaita with `Adw.ToolbarView` and the elementary stylesheet now supports it as well. Plus `Granite.Toast` now includes a new `dismissed ()` signal with  dismissal reasons, a new `STYLE_CLASS_SUCCESS` constant, and you can now use markup in `Granite.HeaderLabel`. We now also load widget fallback styles when using `Granite.init ()` that should improve your apps' cross-platform compatibility.

Another thing that we need to prepare in order to release is the elementary OS Flatpak platform and SDK. Platform 8 is based on the same libraries as included in the GNOME 46 platform with the addition of elementary-specific goodies like Granite, our stylesheet, and icons, plus we're now including LibPortal. LibPortal is a convenient way for developers to add desktop integration features using secure portals such as the Screenshot and Wallpaper portals, as well as handling things like Backgrounding. When Platform 8 is published, we'll need to rebuild of all our Flatpak apps against it and we'll be able to ship GNOME Web 46, which includes a flatter UI design.

## Developer Tools

Code now uses the LibHandy tab bar widget which brings improved animations and drag-n-drop behavior. The Terminal pane can now open to your preference of project subdirectory by default. The preferences dialog was slightly redesigned to fit more modern platform conventions and improve screen reader compatibility. And we fixed a dozen reported issues!

There's a new setting in Terminal for event alerts on invalid input and we now do a better job saving tab state. Plus man page documentation has been improved.

Restoring tabs from last time is now optional in Files and it now supports hiding files and folders via a `.hidden` file, a feature you may be familiar with from other file manager apps.

---

# Get elementary OS 8

elementary OS 8 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 8 FAQ](https://github.com/elementary/os/wiki/OS-8-FAQ){: .button.flat }
[Download elementary OS 8][elementary.io]{: .button.suggested }
</div>

## Get A New Computer

Our hardware retailers [Laptop with Linux], and [Star Labs] are offering elementary OS 8 out of the box starting today! Visit retailers' individual sites for more information.

<div style="text-align: center" markdown="1">
[Shop Devices][store]{: .button }
</div>

[elementary.io]: https://elementary.io
[updates]: {{ site.baseurl }}/tags/#updates
[Laptop with Linux]: https://laptopwithlinux.com/?ref=36&utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Star Labs]: https://starlabs.systems/?rfsn=4227837.e8f025
[store]: https://store.elementary.io/
