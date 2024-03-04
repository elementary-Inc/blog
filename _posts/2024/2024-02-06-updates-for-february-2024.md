---
title: OS 8 Now Available in Early Access
description: Plus a new version of Code
author: danrabbit
image: /images/updates-for-february-2024/settings-system.png

tags:
  - horus
  - updates
---

I'm super excited to let you know that OS 8 builds are available in Early Access and they are now installable! While we highly recommend you don't run these experimental builds in production, they're perfect for trying in a virtual machine or a spare computer. Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for as little as a $1/mo sponsorship](https://builds.elementary.io/). Again beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).

## System Updates

The headlining feature this month is the brand new mechanism for operating system updates. Instead of being a part of updates in AppCenter, system updates now live in the System page of System Settings. The new updates mechanism is super fast and includes an option to download updates automatically. It will also let you know explicity if security updates are part of the updates package. Shoutouts to [Leonhard](https://github.com/leolost2605) for his work here.

<figure markdown="1">
![Operating System view of System Settings](/images/{{ page.slug }}/settings-system.png)
<figcaption markdown="1">
System updates now live in System Settings and can be updated automatically
</figcaption>
</figure>

There's a few reasons why we would want two separate update mechanisms in elementary OS. Under the hood, apps in elementary OS are Flatpak packages and system packages are managed by PackageKit. Flatpak apps are sandboxed from the system and can be reliably updated while your computer is running. System packages are best installed offline, when your computer restarts, to make sure services are restarted correctly and to prevent issues. By splitting apart the updates experience, it is much clearer which updates will require you to restart your computer: app updates in AppCenter will never require a restart, while system updates in System Settings will always require a restart. It also makes the underlining code much less complex and speeds up processes like checking for new updates. It also means an error in one system won't cause updates in the other system to fail. Overall the updates experience in OS 8 will be faster, more reliable, and easier to understand, as well as being easier to automate.

## System Settings

Search in System Settings has been improved to return more relevant results and the titles of those results now reflect both the exact setting name they are matching and the path to that setting.

<figure markdown="1">
![System Settings search](/images/{{ page.slug }}/settings-search.png)
<figcaption markdown="1">
Search in System Settings now ranks results better
</figcaption>
</figure>

Shortcuts settings now include a new "Keyboard Layouts" section where you can set a custom shortcut to change keyboard layouts as well as change the shortcuts for emoji and unicode typing modes. And some cleanup was done in Mouse &amp; Touchpad settings to make layouts more responsive, provide additional explanation text, and improve screen reader support.

<figure markdown="1">
![System Settings app icon](/images/{{ page.slug }}/settings-icon.png){: width="128" height="128"}
<figcaption markdown="1">
System Settings has a new app icon
</figcaption>
</figure>

Plus we're using a new SettingsPage widget to improve consistency between settings views, and System Settings got an icon redesign. Finally, we've almost wrapped up porting System Settings to GTK 4; Network and Printer settings are in review, and Display settings is partially ported, with only Wacom settings having not been started.

## Window Manager

The Multitasking View has seen a number of design updates, the most noticeable of which is that instead of a plain dark grey background, it now features a blurred version of your wallpaper that is either lightened or darkened for light and dark modes respectively. You'll also notice that the workspace cards now have rounded corners and the switcher UI at the bottom of the screen has been updated for light and dark modes as well. Thanks to [Leo](https://github.com/lenemter) for working on this design update!

<figure class="card half" markdown="1">
![Multitasking View in light mode](/images/{{ page.slug }}/multitasking-light.png)
![Multitasking View in dark mode](/images/{{ page.slug }}/multitasking-dark.png)
<figcaption>Multitasking View now features a blurred background and an updated switcher UI design</figcaption>
</figure>

Plus, the Dock has a new multitasking feature: when multiple windows of the same app are opened, selecting that app's icon in the dock will open a window spread instead of hiding those windows.

## And More

The Login &amp; Lock screen now has a smoother fade in animation and will respect your orientation lock settings thanks to [Leo](https://github.com/lenemter). And we've improved screen reader support in Initial Setup &amp; Onboarding. Meanwhile, [Jeremy](https://github.com/jeremypw) has been hard at work on porting Files to GTK 4. And there are plenty of other improvements and new features that are still currently in review.

---

# Updates for OS 7

This month we have just one update for OS 7: a new version of Code. This new release brings a new optional "Fuzzy Finder" plugin which can be launched with the keyboard shortcut <kbd>Alt</kbd> + <kbd>F</kbd> and can be used to search the files of all opened projects in the sidebar. Plus improvements for dark mode, better save and restore of pane positions, new commandline features, as well as various bug fixes.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get the new version of Code plus your regular security, bug fix, and translation updates.

---
