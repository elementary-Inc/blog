---
title: elementary OS 8.1.1 Available Now
description: Shedding bugs fresh out of the gate
author: danrabbit
image: /images/os-8-1-1-available-now/end-session.png

tags:
  - circe
  - release
---

New year, new minor release! elementary OS 8.1.1 is here with another round of bug fixes and the latest Ubuntu LTS Hardware Enablement Kernel. This update addresses a ton of small things you reported to us over the winter break. Read ahead to find out what's new!

# Dock

The dock now has more informative tooltips, including showing <kbd>Super</kbd> + <kbd>1­­–9</kbd> shortcuts for the first 9 apps, and a tooltip on the background apps item.

<figure class="card" markdown="1">
![Dock tooltips](/images/{{ page.slug }}/dock-tooltips.png)
<figcaption markdown="1">
The Dock now shows more informative tooltips
</figcaption>
</figure>

Workspaces now have an animated pressed state and expand to accept drops when in multitasking view. Plus, you can now uninstall apps or view them in AppCenter from their secondary-click menu, just like you can from the applications menu. And, we fixed issues with the dock's appearance in screenshots on HiDPI displays and where the dock could become invisible in Classic sessions.

# AppCenter

We now update badges in the Dock and Applications menu even if you run updates from another app store or via Terminal. We fixed an issue where pressing "Cancel" buttons might not give immediate feedback. And we now send notifications when an app is uninstalled and AppCenter is closed, such as when uninstalling from the applications menu or dock.

# Window Manager

System dialogs like password dialogs now have a blur effect in addition to the dim effect. Plus we made sure to disable hotcorners while they are present and fixed a bug that prevented using accessibility shortcuts—like zoom.

We fixed in issue where the window switcher could leave a non-interactive area on screen when closed, plus an issue where the 6th and 13th keypresses could be skipped while <kbd>Alt</kbd> + <kbd>Tab</kbd>ing. We fixed a couple of issues with multitasking, including ones with fullscreen windows not properly being moved, animations when reordering workspaces, and missing icons in the show all windows view. Plus we fixed blurry picture-in-picture resize icons on fractionally scaled displays.

# Panel

We fixed an issue that prevented the <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd> shortcut from opening the end session dialog until Quick Settings had been opened. And end session dialogs now have the same background dimming and blur effects as password dialogs.

<figure class="card" markdown="1">
![end session dialog](/images/{{ page.slug }}/end-session.png)
<figcaption markdown="1">
End Session dialogs now have a background dimming effect
</figcaption>
</figure>

We've also fixed an issue where apps where launched twice or could even possibly crash when pressing enter while searching the Applications menu.

# System Settings

We've made tweaks to several of our default settings in this release including defaulting to enabling automatic updates, turning off intrusive WiFi notifications, and removing the Multitasking View and System Settings launchers from the dock. System Settings is always available from Quick Settings and Multitasking View can be launched by selecting the already active workspace item in the dock. You can of course always change which apps are pinned to your dock and adjust other options in System Settings.

There's a new option in Applications → Defaults to select your default PDF viewer, and we've slightly tweaked the icon for Background Activity permissions to be a bit cuter.

<figure markdown="1">
![app permissions](/images/{{ page.slug }}/settings-apps.png)
<figcaption markdown="1">
Background Activity icons are just a little bit cuter
</figcaption>
</figure>

We've adding Pointing Stick options to Mouse &amp; Touchpad settings and a new setting for Touchpad drag lock. Plus we improved screen reader accessibility.

<figure markdown="1">
![Pointing Stick settings](/images/{{ page.slug }}/settings-pointingstick.png)
<figcaption markdown="1">
New settings for Pointing Sticks like ThinkPad's TrackPoint
</figcaption>
</figure>

We fixed an issue where "Driver Available" notifications were being sent for drivers that were already installed. And we've improved the reliability of remembering Bluetooth state between sessions. And "Wacom" settings has been renamed to "Pen &amp; Drawing" since it also provides settings for internal digitizers in devices like StarLab's StarLite.

# And More

The screenshot app got some new icons for screenshot modes, and those modes now have text labels. Plus we now remember the last selected screenshot mode—perfect for when you're taking multiple screenshots in a row.

<figure markdown="1">
![screenshot](/images/{{ page.slug }}/screenshot.png)
<figcaption markdown="1">
Screenshot has updated icons and labels for modes
</figcaption>
</figure>

We've improved screen reader accessibility and keyboard navigation in the Feedback app and fixed issues with custom installation types where the partition editor would appear behind the installer.

OS 8.1.1 also includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.17. This brings the latest Intel graphics drivers, better power management for AMD hybrid GPUS, performance improvements for gamers, support for more ARM devices, [and more](https://www.omgubuntu.co.uk/2025/09/linux-kernel-6-17-new-features).

---

# Get elementary OS 8.1.1

elementary OS 8.1.1 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 8 FAQ](https://github.com/orgs/elementary/discussions/categories/q-a){: .button.flat }
[Download elementary OS 8.1.1][elementary.io]{: .button.suggested }
</div>

Sponsors have been able to download OS 8.1.1 release candidates since last week, so if getting things before anyone else is important to you, consider [sponsoring us on GitHub](https://github.com/sponsors/elementary)

[elementary.io]: https://elementary.io
