---
title: elementary OS 8.0.2 Available Now
description: More reliable and accessible than ever
author: danrabbit
image: /images/os-8-0-2-available-now/card.png

tags:
  - circe
  - release
---

It's been about 6 months since our last minor release and the team has been busy! For all of the details about what's new since OS 8.0.1, make sure to check out our posts from [May](https://blog.elementary.io/updates-for-may-2025/) until now. In this post I'll just be covering our progress over the last month up until the release of OS 8.0.2. OS 8.1 is due to be released before year end and that post will be The Big One™ that wraps up every change since OS 8.0. So without further delay, let's dive into what we did last month that made it in OS 8.0.2!

## Installer &amp; Initial Setup

The latest Installer incorporates fixes for a number of issues raised during [accessibility testing](https://blog.elementary.io/updates-for-july-2025/). The "Before Installing", "Try or Install", "Choose a Disk", and "Encryption" views should all have much improved accessible labels, things like password quality feedback will now be read aloud by the screen reader, and we fixed a couple instances where the screen reader would announce text style markup. Plus, [Leo](https://github.com/lenemter) added a few more safety checks for the custom install view that should prevent crashes with certain complex partition layouts, and the Installer should now always appear centered on screen.

Initial Setup also includes the same password quality feedback improvements for screen readers and it will always appear centered on screen. Plus trailing hyphens and underscores are now allowed in usernames and we use a more reliable source of information for keyboard layouts, thanks to [Ryo](https://github.com/ryonakano).

## Music

The latest release of Music includes a number of important new features for managing the queue, including performance improvements for large queues. You can now remove individual track from a track's context menu or clear the entire queue thanks to [Oowoosh0](https://github.com/Oowoosh0). [Jeremy](https://github.com/jeremypw) and [Leonhard](https://github.com/leolost2605) implemented searching by track name. The queue and the last played track will be saved and restored thanks to [Stella](https://github.com/teamcons), and she added the keyboard shortcut <kbd>Ctrl</kbd>+<kbd>O</kbd> to add new files. [Ryan](https://github.com/zeebok) added the <kbd>Ctrl</kbd>+<kbd>Q</kbd> shortcut to quit, and album art will now show in media controls in the panel and elsewhere. Plus [Oowoosh0](https://github.com/Oowoosh0) fixed a couple of issues with long artists names or when using large system fonts.

## Terminal

[Leo](https://github.com/lenemter) Fixed an issue that caused keyboard focus to not be inside the first tab when opening a new window, and he fixed an issue where dropping in text that contain `#` would be cut off. [Jeremy](https://github.com/jeremypw) also fixed an issue with incorrect line breaks when pasting or dropping text while a process is running, made sure to always clear process finished icons when a tab is selected, and removed an old misfeature that would cause window sizes to be odd on certain display sizes.

## Hardware Enablement

OS 8.0.2 includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.14. This new version of the Linux kernel brings improved performance—especially while gaming, reduced power consumption for certain AMD and Intel chipsets and GPUs, new security features, and support for more gamepads, wifi devices, microphones, [and more](https://www.omgubuntu.co.uk/2025/03/linux-kernel-6-14-released-delivers-big-boosts-to-linux-gaming).

## And More

Main menus are now properly marked in Camera, and Videos and can be opened with the keyboard shortcut <kbd>F10</kbd>. In Calculator, [Alain](https://github.com/alainm23) replaced the "Del" button with an icon, and the "New Window" action now shows in icon in places like keyboard shortcut settings. [Trevor](https://github.com/Tbusk) fixed a crash with screenshots which are much taller than they are wide and [Ryo](https://github.com/ryonakano) fixed an issue that caused screenshots not to be saved to custom locations.

---

# Get elementary OS 8.0.2

elementary OS 8.0.2 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<div style="text-align: center" markdown="1">
[OS 8 FAQ](https://github.com/orgs/elementary/discussions/categories/q-a){: .button.flat }
[Download elementary OS 8.0.2][elementary.io]{: .button.suggested }
</div>

Sponsors have been able to download OS 8.0.2 release candidates since the beginning of the month, so if getting things before anyone else is important to you, consider [sponsoring us on GitHub](https://github.com/sponsors/elementary)

[elementary.io]: https://elementary.io

---

## And Even More

Expect another blog post soon detailing all of the new features that have been released since OS 8.0.2 was built and what's available to test in Early Access—there are a number of big ones!
