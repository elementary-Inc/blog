---
title: Updates for April, 2023
description: New features and settings, improved performance, and fewer bugs
author: danrabbit
image: /images/updates-for-february-2023/card.png

tags:
  - horus
  - updates
---

This month we have a mix of new design and feature updates, another big batch of fixed bugs, and even some performance improvements.

# Mail

The headliner this month is Mail which does a better job handling newly added online accounts and includes fixes for a couple of potential crashes, plus a ton of code cleaning under the hood and even a few performance improvements. The composer now always opens in a separate, non-modal window making it much easier to reference a message you're replying to or manage multiple drafts at the same time.

<figure class="half" markdown="1">
![Mail](/images/{{ page.slug }}/mail.png)
![Composer Window](/images/{{ page.slug }}/mail-compose.png)
<figcaption markdown="1">
Subtle design changes in Mail include floating headers and a flatter compose window
</figcaption>
</figure>

It also features quite a few more keyboard shortcuts for text formatting, adding attachments, etc. You might also appreciate some subtle design tweaks like placing the conversation list filter next to the search bar or how headers now appear to float over scrolled content. Major thanks goes to [Leonhard](https://github.com/leolost2605) for his hard work on this release.

# Web

The latest GNOME Web 44.2 has now been ported to Gtk 4 and features much improved performance and web standards compatibility, plus a new saved passwords popover. I'm especially thankful to [Alice](https://github.com/exalm) for working with us to ensure that Adwaita-using apps still look and feel at home on elementary OS. With Firefox sync, web apps, and performance that matches major mainstream competitors, there's never been a better time to try this community-made web browser.

# Window Management

We had yet another great release of our window manager, Gala, this month. This release brings the total number of fixed reported issues since OS 7 in this component alone to nearly 40! Highlights from this release include adding the keyboard shortcut <kbd>Alt</kbd> + <kbd>~</kbd> for switching between windows of the same app, navigating with the arrow keys while holding down <kbd>Alt</kbd> + <kbd>Tab</kbd>, and several more animations now respect your preference to disable them. Plus, the team has been working hard to prepare for Mutter 44 which will bring fractional and per-display scaling support on Wayland, so look forward to seeing that in a future version of elementary OS. Thanks again to [Corentin](https://github.com/tintou), [David](https://github.com/davidmhewitt), and [Leo](https://github.com/lenemter) for all of their work here.

# System Settings

The latest release of Desktop settings includes some new options for switching workspaces via hotcorners as well as a new feature to dim wallpapers in dark mode thanks to [Leo](https://github.com/lenemter)! You'll also notice that the setting for disabling animations has moved to the "Appearance" tab and has been renamed to "Reduce Motion".

<figure class="constrained" markdown="1">
![Appearance Settings](/images/{{ page.slug }}/settings-appearance.png) {: width="1101" height="769"}
<figcaption markdown="1">
The "Reduce Motion" setting has moved to the "Appearance tab"
</figcaption>
</figure>

A new version of Locale settings has also been released that prevents Fcitx 5 from being automatically pulled in with some languages and fixes a potential issue with acquiring permissions to set system-wide locale settings.

# Onboarding

A fresh version of Onboarding has been released with several redesigned pages including a fancy dynamic icon featuring the release wallpaper on the Welcome page, a much more prominent explanation of Sideloading, some new icons, and bolder typography.

<figure class="half" markdown="1">
![Welcome view of Onboarding](/images/{{ page.slug }}/onboarding-welcome.png){
![Apps view of Onboarding](/images/{{ page.slug }}/onboarding-apps.png)
![Early Access view of Onboarding](/images/{{ page.slug }}/onboarding-earlyaccess.png)
![Guest Session view of Onboarding](/images/{{ page.slug }}/onboarding-guest.png)
<figcaption markdown="1">
Onboarding features bolder typography, colorful icons, and a more prominent explanation of Sideloading
</figcaption>
</figure>

Plus, it has better handling for Early Access builds, and Onboarding now handles the Guest account warning as well. We're always looking at your feedback to figure out the best way to help you get started with elementary OS, so keep sending in reports!

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Developer Platform

The latest stylesheet brings support for Adw.AboutWindow and Adw.MessageDialog and the latest icons adds several icons expected by Adwaita-using apps such as `adw-external-link` and the row drag handle icon. There are also some subtle updates to a few symbolic icons. These improvements will land soon in a minor version bump to the 7.2 Flatpak platform so you won't need to adjust your manifest to get them.

## Early Access Preview

Coming soon to early access, location portal support! We're retiring our location agent, the old method for granting apps location access, and replacing it with Portals, the standard for accessing system services for Flatpak apps. If you've previously had trouble with location access features in apps, be sure to check System Settings → Security & Privacy to make sure Location Services is turned on. Also watch out for more improvements to Mail, including better offline support and the ability to move messages between folders. There may also be some design changes coming to AppCenter, so look out for those!

Early Access is a great way to help us test new features and find bugs before they roll out to everyone. If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/).
