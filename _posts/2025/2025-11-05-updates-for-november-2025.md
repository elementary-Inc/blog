---
title: Who Monitors The Monitor?
description: Updates for OS 8 and Early Access
author: danrabbit
image: /images/updates-for-november-2025/monitor-system.png

tags:
  - circe
  - updates
  - earlyaccess
---

# Monitor

The first release of Monitor as an elementary OS default app is here! Monitor is an app for monitoring your system resources and running processes, including with optional panel indicators. Since its last release, we've completed the port to GTK4, rewrote the settings menu, and a ton more under the hood. Massive thanks to [Stanisław](https://github.com/stsdc), [Ryo](https://github.com/ryonakano), and more for their hard work here.

<figure class="half" markdown="1">
![Monitor Processes](/images/{{ page.slug }}/monitor-system.png)
![Monitor Resources](/images/{{ page.slug }}/monitor-processes.png)
<figcaption markdown="1">
In the Secure Session apps need your explicit permission for more things
</figcaption>
</figure>

Monitor should be automatically installed on your next update, but if you for some reason don't get it, you can install Monitor with the Terminal command `sudo apt install io.elementary.monitor`.

# Window Manager &amp; Dock

Another massive bug fix release of our Window Manager has landed with 19 fixed issues including improved performance, HiDPI support, and animations. We've fixed issues with dock menus sometimes appearing behind the dock, apps will now launch correctly when you switch between Classic and Secure sessions, and more.

<figure markdown="1" class="card">
![Desktop Blur](/images/{{ page.slug }}/desktop-blur.png)
<figcaption markdown="1">
Blur effects have landed in the window switcher and are coming to the Dock
</figcaption>
</figure>

Plus, this release introduces a new blur effect. You'll first notice it in the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher, but in future updates we will also blur behind the Dock and Notifications. Big thanks to [Leo](https://github.com/lenemter) and [Leonhard](https://github.com/leolost2605) for their hard work on this release.

# Icons

We landed a highly requested redesign of folder icons thanks to [newhoa](https://github.com/newhoa). The new folder design is more rounded and more closely matches the design of the Files app icon.

<figure markdown="1">
![Folder icons](/images/{{ page.slug }}/files.png)
<figcaption markdown="1">
Folder icons have been redesigned with rounded corners
</figcaption>
</figure>

Icons featuring a computer mouse have been slightly redesigned to include a scroll wheel. And, icons featuring a mouse pointer have been updated to match the new pointer design, thanks to [William](https://github.com/wpkelso).

<figure markdown="1">
![Pointer icons](/images/{{ page.slug }}/settings-mousetouchpad.png)
<figcaption markdown="1">
Mouse and Pointer icons have been updated
</figcaption>
</figure>

Plus a number of smaller clean ups including adding missing sizes for certain icons, adjusting lighting, and rounding a few edges. Finally, we now fall back to Adwaita icons when an app is missing a non-standard icon name, thanks to [David Lapshin](https://github.com/daudix).

# Code

In the symbols sidebar, tooltips for C language symbols are now more information like their Vala counterparts. When you clone a git branch, we now send an unobtrusive toast to let you know cloning has completed. Global searches now respect your search case sensitivity settings. Opening a second window no longer results in duplicate project entries in the project chooser. And the "Open Folder" keyboard shortcut has been fixed. Shoutouts [Jeremy](https://github.com/jeremypw) for his hard work on Code.

# Files

[Jeremy](https://github.com/jeremypw) also fixed a number of small issues with Files including expanding trashed folders in the list view, refreshing views properly when files are deleted, and preventing a potential freeze when the Templates folder contains too many files and subfolders. Plus, Files now shows a setting for Date &amp; Time format.

# And More

In Power settings we now show a small warning about increased energy usage with certain options. The Sound menu now uses a toggle icon like Quick Settings instead of a switch to quickly mute. And media keys for volume now work on the Lock Screen thanks to [Leo](https://github.com/lenemter).

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

We're laser focused on preparing to release OS 8.1.0 so big new features will almost exclusively be targeted to OS 9 from now on. We don't have OS 9 builds available yet for you to try, but we are working on them already! We'll let sponsors know first when OS 9 builds are available in Early Access to test. But for now, we have just one more thing.

64-bit Universal ARM builds from the *stable* updates channel are now available in on our [Builds website](https://builds.elementary.io/downloads). These builds replace the old specific builds for platforms like Raspberry Pi and Pinebook, plus they add support for other ARM devices supported by Linux. This is thanks to the hard work of [NN708](https://github.com/NN708) who has been dedicated to seeing this project through over the several months it took to complete.

---

## Sponsors

At the moment we're at 24% of our monthly funding goal and 324 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
