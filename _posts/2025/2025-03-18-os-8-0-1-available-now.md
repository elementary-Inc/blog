---
title: elementary OS 8.0.1 Available Now
description: A bundle of bug fixes and a couple creature comforts
author: danrabbit
image: /images/os-8-available-now/settings-updates.png

tags:
  - circe
  - release
---

It's been a little over 100 days since elementary OS 8 was released, and we're proud to announce another round of updates, including a fresh new download. We've been hard at work this winter addressing issues that you reported and we've added a couple new creature comforts along the way. This bug fix release also includes the latest Ubuntu LTS Hardware Enablement Kernel, so it's worth checking out if you downloaded OS 8.0 and it disagreed with your hardware.

# AppCenter

We now properly use dark mode brand colors and dark mode screenshots thanks to [Italo](https://github.com/edwood-grant). Plus, when developers provide screenshots for multiple desktop environments, we now prefer the ones intended for our desktop environment, Pantheon. We support the new `<Developer>` Appstream tag, thanks to [Juan](https://github.com/kerunaru). And we now support the `contribute` URL type.

<figure markdown="1">
![Harvey on AppCenter](/images/{{ page.slug }}/appcenter-screenshots.png)
<figcaption markdown="1">
AppCenter now shows dark mode screenshots when available
</figcaption>
</figure>

[Italo](https://github.com/edwood-grant) also fixed some issues with release notes overflowing out of their container, and we slightly redesigned the release notes window in the Updates page. He also addressed a few other issues in the Updates page that could occur while things were being updated or refreshed and made sure AppCenter recovers gracefully when its cache is emptied.

<figure markdown="1">
![Releases notes on AppCenter](/images/{{ page.slug }}/appcenter-releases.png)
<figcaption markdown="1">
Release notes dialogs have been slightly redesigned
</figcaption>
</figure>

Search is also much faster thanks to [Leonhard](https://github.com/leolost2605). And for developers, [Ryo](https://github.com/ryonakano) fixed loading your local metadata for testing with the `--load-local` terminal option.

# Files &amp; Terminal

[Jeremy](https://github.com/jeremypw) fixed another half-dozen reported issues in Files including, an issue that prevented entering file paths in search mode, an issue that prented scrolling after deleting files, and an issue where files would disappear when dropped on an unmounted drive. The New file submenu now respects the hierarchy of folders in Templates. We now also respect the `admin://` uri protocol for opening a path as an administrator, and Files is now styled correctly when run as administrator.

He also fixed an issue where Terminal tabs took multiple clicks to focus, and an issue where keyboard shortcuts stopped working for tabs that had been dragged into their own new window. Plus, file paths and names are also now properly quoted when drag-and-dropped from Files into Terminal.

# System Settings

System Settings now allows configuring its notifications in System Settings → Notications. So you can turn off bubbles if you don't want to receive notifications about updates, for example. We'll also no longer automatically download updates when on metered connections and send a notification instead, thanks to [Leonhard](https://github.com/leolost2605). Plus we no longer check for updates in Demo Mode.

<figure markdown="1">
![System Settings → System](/images/{{ page.slug }}/settings-updates.png)
<figcaption markdown="1">
Updates now show their download size and you can see progress towards our monthly sponsorship goal
</figcaption>
</figure>

In System, [Vishal](https://github.com/vjr) made sure we show how large an update will be before downloading it and that we skip held-back packages—such as phased or staged updates—when preparing the updates bundle so that it will more reliably succeed. [Alain](https://github.com/alainm23) added a progress bar while downloading. And [Ryo](https://github.com/ryonakano) made sure the last refresh time is more accurate when no updates are available. [Alain](https://github.com/alainm23) also added a new progress bar that represents how close we are to meeting our monthly sponsorship goal.

In Applications, you can now disallow notifications access. This is especially useful for apps which use the notifications portal, but don't properly report their notification usage and can't be controlled in the Notifications settings page.

<figure markdown="1">
![System Settings → Applications](/images/{{ page.slug }}/settings-apps.png)
<figcaption markdown="1">
Reign in apps that don't appear in Notifications settings
</figcaption>
</figure>

In Network there are two new settings: whether a network should be automatically connected to when available and whether to reduce background data usage when connected to that network.

<figure markdown="1">
![System Settings → Network](/images/{{ page.slug }}/settings-network.png)
<figcaption markdown="1">
Disable autoconnect or mark a network as metered
</figcaption>
</figure>

We also updated the pointer icons in Mouse &amp; Touchpad settings and the checkmarks in Locale settings will now respect your chosen accent color. Plus settings pages with sidebars now remember the width you adjusted them to, thanks to [Alain](https://github.com/alainm23).

# Installation &amp; Onboarding

[David](https://github.com/davidmhewitt) fixed a crash with certain partitioning schemes in the Installer's custom install view. And the Encryption step was redesigned to fit on a single page, solving an issue with confusing navigation. Plus, onboarding will now always stay centered on the screen, even when resized.

# Panel &amp; Quick Settings

[Ilya](https://github.com/lagoshn) fixed an issue with the panel height when using the Classic session and HiDPI displays. The app context menu in the Applications menu now shows a "Keep in Dock" checkbox, just like in the Dock thanks to [Stella](https://github.com/teamcons). In the Power menu, we now show the device model if available, and avoid erroneously showing an empty battery icon thanks to [Alain](https://github.com/alainm23). In the Sound menu, [Dmitry](https://github.com/EndarValuk) fixed loading album art from certain apps like Google Chrome, and we fixed an issue where player icons could become too large.

<figure class="card" markdown="1">
![Accounts in Quick Settings](/images/{{ page.slug }}/quicksettings-accounts.png)
<figcaption markdown="1">
See who else is logged in and quickly switch accounts from Quick Settings
</figcaption>
</figure>

In Quick settings, [Leonhard](https://github.com/leolost2605) fixed an issue with performing updates while shutting down. And [Alain](https://github.com/alainm23) added a new page where you can see which other people are logged in and quickly switch between accounts.

# Dock

[Leo](https://github.com/lenemter) added a bit more spacing between launchers and their running indicators, and fixed an issue where larger icons could be clipped at the peak of their bounce animation. Apps who don't notify on startup will no longer bounce in the dock indefinitely, thanks to [Leonhard](https://github.com/leolost2605). We fixed an issue where the dock would still receive click events while hidden in the Classic session. Plus the dock now has an opaque style when "Panel Translucency" is turned off in System Settings → Desktop → Dock &amp; Panel.

# Window Manager

We have another huge release of our window manager thanks to [Leonhard](https://github.com/leolost2605) and [Leo](https://github.com/lenemter). This release fixes five potential crashes, over a dozen reported issues, fixes related to both the Classic and Secure sessions, issues related to HiDPI, and more, plus performance improvements. It's worth reading the full release notes [on GitHub](https://github.com/elementary/gala/releases/tag/8.1.0) if you have been waiting for the fix for a specific issue.

# And More

OS 8.0.1 includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.11. This brings improved performance for AMD processors, support for Intel "Lunar Lake" processors, and filesystem performance improvements in some cases. Plus support for certain webcams, USB network devices, joysticks, [and more](https://www.omgubuntu.co.uk/2024/09/linux-kernel-6-11-released-this-is-whats-new).

[Leo](https://github.com/lenemter) fixed an issue where connecting Bluetooth devices could cause the Lock Screen to freeze. You can now close the captive network assistant with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>Q</kbd>, thanks to [Stanisław](https://github.com/stsdc). And [Alain](https://github.com/alainm23) fixed copying screenshots to the clipboard.

We fixed an issue where wired network connections could fail to connect due to a change in Ubuntu. We're [pursuing this issue upstream](https://code.launchpad.net/~tintou/network-manager/+git/network-manager/+merge/479821) and working on a way to ship the fix as an update, but for now fixing this issue requires either [manual intervention through Terminal](https://github.com/orgs/elementary/discussions/658) or a reinstall.

We also now pre-install an AppArmor profile that fixes a number of Flatpak-related issues like not being to install certain runtime updates or apps not launching in the guest session or Demo mode. Special thanks to [Uncle Tallest](https://github.com/UncleTallest) for investigating this issue and helping folks in our Discord who ran into it.

And of course this release comes with a ton of translation updates! Special thanks to our hard-working internationalization community and especially [Ryo](https://github.com/ryonakano) who fixed a number of issues with things that couldn't be localized properly in the previous release.

---

# Get elementary OS 8.0.1

elementary OS 8.0.1 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 8 FAQ](https://github.com/orgs/elementary/discussions/categories/q-a){: .button.flat }
[Download elementary OS 8.0.1][elementary.io]{: .button.suggested }
</div>

Sponsors have been able to download OS 8.0.1 release candidates since last week, so if getting things before anyone else is important to you, consider [sponsoring us on GitHub](https://github.com/sponsors/elementary)
