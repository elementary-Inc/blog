---
title: Updates for October, 2019
description: Prepping for LAS, releasing ALL THE THINGS, and wrapping up Hacktoberfest
author: cassidyjames
tags:
  - updates
  - juno
  - flatpak
---

Welcome to November! A bit later this month we’ll be attending the [Linux App Summit](https://linuxappsummit.org) alongside folks from Canonical, CodeThink, Collabora, Endless, Flatpak, Fractal, GNOME, GStreamer, KDE, Krita, LibreOffice, Meson, Purism, Red Hat, Ubuntu and more in Barcelona, Spain to hang out and work with folks from across the open source community—plus we'll be giving a couple of talks about [Curb Cuts](https://conf.linuxappsummit.org/en/LAS2019/public/events/43) and [Growing Beyond the System Tray](https://conf.linuxappsummit.org/en/LAS2019/public/events/48).

We'll share more on that later, but first: let's take a look at all of the updates that went out to elementary OS users over the past month.

## Sideload & Flatpak

This month we have a brand new app for elementary OS to enable easier sideloading of apps. Sideload handles `flatpakref` files, like those you might find on [Flathub](https://flathub.org) or another third-party website providing a Flatpak app for download.

![Sideload screenshot](https://raw.githubusercontent.com/elementary/sideload/master/data/screenshot.png)

While we always recommend users visit AppCenter for quality curated apps made for elementary OS, we understand that there are some cross-platform apps that don't meet the requirements to be curated in AppCenter. Rather than leaving users out on their own to add insecure PPAs or run random scripts as root, Sideload facilitates a safer way to help users get sandboxed apps.

This also means that Flatpak is enabled out of the box on elementary OS now, and we've [submitted a pull request](https://github.com/flatpak/flatpak.github.io/pull/355) to simplify the Flatpak [quick setup instructions](https://flatpak.org/setup/elementary%20OS/) on Flatpak.org to reflect this.

Sideload is a new app and we have plans to iterate on it over time, but it's already super useful and straightforward. The first version was released in October and it will be rolling out to users soon.

## Updates Released

Towards the end of the month we also finalized our brand new automation-powered release process (more on that in an upcoming blog post), meaning we were able to easily queue up the releases of several apps and desktop components. Buckle up, we've got quite the ride ahead of us:

![Release ALL THE THINGS meme](https://i.imgflip.com/3epe6y.jpg)

### AppCenter: Flatpak, Non-Curated Warning, & Up to 10× Faster

The big AppCenter update is finally here! This release adds Flatpak support out of the box, meaning apps from any added remotes—including those added with Sideload—will show up automatically. Apps with multiple versions available (i.e. from both Flatpak and the Ubuntu repos) will show a drop-down to select the version of the app listing, and Flatpak updates will be included alongside normal updates.

![AppCenter](https://elementary.io/images/screenshots/appcenter.png){: srcset="https://elementary.io/images/screenshots/appcenter@2x.png 2x"}

With users adding more non-curated apps into AppCenter with an officially-supported method, we also took time to be more clear about the implications of installing non-curated apps with a new dialog, similar to the Sideload dialog. As with Sideload, this is a starting point and we plan to iterate on it further, especially exposing more specific Flatpak permissions.

![Non-curated warning](https://user-images.githubusercontent.com/611168/67596163-572e1800-f725-11e9-927b-24d23536cfa7.png)

We've also cleaned up and refactored a _ton_ of code in AppCenter, bringing massive performance improvements and numerous layout fixes. Paired with a newer version of PackageKit, AppCenter performs more actions in parallel. As a result, it's about 10× faster for certain operations like showing featured apps on the home page.

### Calendar: Iconography & Recurring Events

Certain events in Calendar now get a cute little icon like an airplane for flights, a car for road trips, a film strip for movie showings, a ring for weddings, etc. It adds some character but also helps distinguish them if you have many events. Calendar is also smarter about the default time for new events being created for the current day, using the next whole hour (or the last hour of the day if it's after 11 PM).

The release also includes major fixes for recurring events along with smaller fixes for various layout issues.

### Panel: Date & Time Redesign

In October we released a minor update to the top panel that fixes some reported focus and touchscreen issues.

We also released a major new design for the Date & Time indicator in the top panel. It includes more clear navigation, a dot for events on each day, plus a side pane with the selected day's events. It also includes the same recurring event fixes as Calendar.

### System Settings: Housekeeping & Bluetooth

We reworked the design of the Housekeeping settings in the Security & Privacy settings to better match the design of the new Onboarding app. The Bluetooth settings now include a new pairing agent to better handle devices that need a passcode or key to pair.

## Hacktoberfest 🍂️👩‍💻️🎃️

Besides releasing a ton of updates in October, this year we also saw great participation in [Hacktoberfest](https://hacktoberfest.digitalocean.com/) solving bitesize bugs across our projects and working with new contributors on their first ever contributions to elementary.

<!-- TODO: List some Hacktoberfest issues that were fixed -->

Thank you to all those contributors who made a difference, and thanks to the volunteers and maintainers who helped them out along the way.

## Get the Updates

As with each monthly update, you can also expect general bug fixes, performance improvements, and translation updates that we didn't detail here. Open up AppCenter and hit that "Update All" button to get the goods.

