---
title: The System Settings Redesign Has Landed
description: OS 8 progress during March
author: danrabbit
image: /images/updates-for-april-2024/settings-notifications.png

tags:
  - earlyaccess
  - updates
---

This month the biggest story is System Settings, but we also have some great progress on the new Dock and Wayland. Plus a small change to default keyboard shortcuts that you might appreciate. Read ahead to find out the new developments you have to look forward to in the upcoming elementary OS 8!

## System Settings

The System Settings port for GTK 4 is now completed! And not only that, we've landed the first step in a major redesign. Settings panes are now in charge of drawing their own window controls, which means several settings have already been updated to use a more modern paned design and others are able to use space more efficiently in their own way. You can expect further design refinements to continue to land throughout the OS 8.x cycle

<figure markdown="1">
![Network Settings](/images/{{ page.slug }}/settings-network.png)
<figcaption markdown="1">
System Settings has a new modern design
</figcaption>
</figure>

The headliner this month is definitely Application settings. We now have support for adjusting the runtime permissions stored in Flatpak's PermissionsStore—these are set when an app explicitly asks for your permission to access a specific feature while it's running. So if you've previous denied an app access to run in the background or granted an app permission to set the wallpaper, you can change your mind at any time and adjust permissions here.

<figure markdown="1">
![Application Settings](/images/{{ page.slug }}/settings-applications.png)
<figcaption markdown="1">
System Settings → Applications has expanded options
</figcaption>
</figure>

We've also adjusted the language of install time permissions—aka sandbox holes—to be more clear that these represent advanced system access and the implications of adjusting them. Plus the descriptions of several individual items were changed based on feedback to use less technical language. And app permission pages now show the app's icon and description.

<figure markdown="1">
![Notification Settings](/images/{{ page.slug }}/settings-notifications.png)
<figcaption markdown="1">
Do Not Disturb no longer blocks Notification settings
</figcaption>
</figure>

Language &amp; Region settings now has searchable dropdowns. We've also received some feedback from some folks that indicates they were looking here for Keyboard Layout or Date &amp; Time settings, so we more clearly link to both of those locations to help you find what you're looking for. If you're not a fan of overlaid scrollbars that disappear when not in use, there's a new setting to always show scrollbars in Desktop → Appearance. The Do Not Disturb setting in Notifications settings no longer blocks the whole view and we've updated the design of this pane to better reflect modern design patterns and support RTL language layouts. And Housekeeping is now completely handled by elementary's Settings Daemon which uses SystemD timers under the hood.

## Desktop

We're closing in on a much better multitasking story for the new Dock. This month Leonhard implemented scrolling over an app's icon to switch between its open windows and focusing a single open window of an app on click instead of opening new windows. We've also implemented a middle-click system that is aware of the FreeDesktop.org SingleMainWindow app launcher hint, so we can more reliably open new app windows when middle-clicking an app's icon; This closes a 3-year-old feature request! This is in addition to the window spread feature that was implemented in January. The end result is a much more predictable experience that is centered on bringing you to the app you've clicked and an improved workflow for multi-window apps.

We're also making a major change to our default keyboard shortcuts. Pressing <kbd>⌘</kbd> will now open the Applications menu instead of the Shortcuts overlay and <kbd>⌘</kbd> + <kbd>Space</kbd> will now switch keyboard layouts by default. This brings us more in line with the defaults from other desktops and operating systems and will hopefully be more comfortable for folks who rely on these shortcuts. Of course you can always change the <kbd>⌘</kbd> key behavior and keyboard shortcuts in general in System Settings → Keyboard.

## Wayland

Our progress towards Wayland continues this month with several fixes in our window manager. Notifications are now launched as a client of the window manager thanks to Leonhard, meaning they are no longer in the center of the screen in the Wayland session. He also did some refactoring that ensures the Wayland session launches just as quickly as the X11 session, fixed an issue with the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher blocking mouse input, and fixed drag and drop icons not appearing.

---

## Security

A quick note about security in elementary OS 7! If you've heard about the recent xz vulnerability, rest assured that elementary OS was not affected. We're very fortunate to benefit from the hard work of Canonical's security team and Ubuntu LTS. If you're ever curious about the status of vulnerabilities you can check the [Ubuntu Security Notices](https://ubuntu.com/security/notices) website. You can find the Ubuntu version that system packages come from in System Settings → System on the Operating System Tab, just below the name of the current elementary OS release. As always, be sure to run your updates and avoid third party system software repositories. Choosing Flatpak for apps also keeps your computer secure and your information private with its built-in sandboxing.

## Sponsors

At the moment we're just above 21% of our monthly funding goal and we're very close to 300 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

If you're not already in Early Access, you can be among the first to try the next release of elementary OS and give us your feedback by sponsoring elementary [for as little as $1/mo](https://builds.elementary.io/). Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).

A quick note about currently daily elementary OS 8 builds, there's a big migration happening upstream to fix the [year 2038 problem](https://en.wikipedia.org/wiki/Year_2038_problem) so until that calms down we might have a disruption in builds. You can always access previous daily builds by scrolling down the bottom of the [Builds](https://builds.elementary.io/) page where you'll find the most recent succesful builds of elementary OS 8 and more.
