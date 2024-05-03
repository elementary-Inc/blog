---
title: Visualizing The Finish Line
description: OS 8 progress during April
author: danrabbit
image: /images/updates-for-may-2024/quick-settings.png

tags:
  - earlyaccess
  - updates
---

First things first, congratulations to Ubuntu on releasing version 24.04! If you're not already aware, we build elementary OS releases from the Ubuntu software repositories, so we now have a stable upstream to work from. That means it's time for us to focus in on finishing up elementary OS 8! Read ahead to find out what we accomplished towards that end over the last month.

## Release Planning

The [OS 8 Project Board](https://github.com/orgs/elementary/projects/128/views/1) has been scoped down to only include things that are essential for release. This is the place to watch to estimate how far out we are from a stable OS 8. When this board is empty, we're ready to release! We want to ship OS 8 as soon as possible, so we may find ways to further trim this list down if we aren't able to address everything in a timely manner.

## Design

We saw some great changes to Icons this month thanks to new and old contributors. [William](https://github.com/wpkelso) gave attention to cursors and introduced more color into their design. This resulted in an almost complete redraw of our cursors and closed several old issue reports. We also got new, colorful "Find" icons thanks to [Newhoa](https://github.com/newhoa) as well as a new design for the "Save As" icon.

<figure markdown="1">
![New Cursors](/images/{{ page.slug }}/cursors.png){: width="192" height="192"}
<figcaption markdown="1">
Cursors have been almost completely redesigned with more color
</figcaption>
</figure>

Our System Settings redesign work continues, and this month we merged in the redesign of Applications settings. The new split-paned design brings it in line with other settings pages and makes navigating much faster by exposing the list of installed apps at the top level of navigation.

<figure markdown="1">
![Application Settings](/images/{{ page.slug }}/settings-applications.png){: width="898" height="559"}
<figcaption markdown="1">
Applications Settings has a new split-paned design
</figcaption>
</figure>

## Desktop

A small visual change, when switching workspaces docks and panels will no longer move with the switch thanks to [Leonhard](https://github.com/leolost2605). Meanwhile [Leo](https://github.com/lenemter) fixed an incorrect default keyboard shortcut for moving windows to the last workspace, and made sure that there's audio (or visual depending on your settings) feedback when we're unable to cycle workspaces in response to the keyboard shortcut.

<figure markdown="1">
![Quick Settings](/images/{{ page.slug }}/quick-settings.png){: width="256" height="209"}
<figcaption markdown="1">
Quick Settings joins the panel
</figcaption>
</figure>

Quick Settings has also made it into the default package selection, replacing the Session and Accessibility indicators. It also currently provides toggles for Dark Mode and, when running on a device with an accelerometer, Screen Rotation Lock. This sets the foundation for including more quick toggle features as well as helps us clean up extra panel indicators.

## Upstream Library Updates

Early Access builds were disrupted for just over a month as a few migrations occured. The first being Ubuntu's move to 64 Bit time which fixes the [year 2038 problem](https://en.wikipedia.org/wiki/Year_2038_problem). We lost a bit of time to this as we encountered situations with incompatible packages and failing builds etc. The second was adapting to API changes in Mutter 46 and required rebuilds of our window manager, the panel, and the login &amp; lock screen. Mixed in was a secret third thing: the session managers migration to SystemD. We were already ahead of this in our regular session thanks to Pantheon's NixOS maintainer, [Bobby](https://github.com/bobby285271), but [David](https://github.com/davidmhewitt) discerned and provided the fix for our Installer session just 3 days ago. I'm happy to report that we've succesfully survived these migrations and Early Access builds are building and bootable again!

With the stabilization of upstream packages this is also the time for us to start building our OS specific patches, and that work is almost completed. These patches are minimally invasive and do things like set LSB information and make sure that we're compatible with things like DKMS and certain functions of the Apt package manager.

## Developer Platform

Another thing that we need to prepare in order to release is the elementary OS Flatpak platform and SDK. Platform 8 is based on the same libraries as included in the GNOME 46 platform with the addition of elementary-specific goodies like Granite, our stylesheet, and icons, plus we're now including LibPortal. LibPortal is a convenient way for developers to add desktop integration features using secure portals such as the Screenshot and Wallpaper portals, as well as handling things like Backgrounding. When Platform 8 is published, we'll need to rebuild of all our Flatpak apps against it and we'll be able to ship GNOME Web 46, which includes a flatter UI design.

## And More

Two new portals landed in OS 8: the Screenshot and Color Picker portals. Additionally Photos has been updated to use the Wallpaper portal. And another app will soon be shipped as a Flatpak in OS 8! We recently packaged up Font Viewer against the elementary Flatpak Platform, fixing a styling regression, ensuring we can continually ship the latest version of Font Viewer throughout the OS 8 life cycle, and that it can be automatically updated without requiring a system restart.

---

## Sponsors

At the moment we're just above 21% of our monthly funding goal and we've crossed 300 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

If you're not already in Early Access, you can be among the first to try the next release of elementary OS and give us your feedback by sponsoring elementary [for as little as $1/mo](https://builds.elementary.io/). Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
