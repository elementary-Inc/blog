---
title: elementary OS 6 Beta Available Today
description: What’s a beta, and what’s new for developers?
author: cassidyjames
image: /images/updates-for-july-2020/card.png
tags:
  - early-access
  - odin
  - devs
---

Developers and testers, it's the day you've been waiting for: elementary OS 6 Beta is available now! We first started [talking publicly about elementary OS 6](/updates-for-july-2020) in August of last year. In the time since, we've been hard at work tackling the ambitious scope of work we laid out for ourselves while also dealing with the fallout of a global pandemic, travel restrictions, and loss in our own circles of family and friends.

Despite all of that, we're proud of the work we've done and are excited to get it into the hands of developers and testers as we work to complete the stable release.

## What’s a beta?

Before we get into what's new, a refresher on what "beta" means. There are generally three phases of development of elementary OS:

- Early Access
- Beta
- Release Candidate

Early Access builds are considered "bleeding edge," use the daily repositories, and are made available as soon as possible without the standard human testing process that goes into stable builds. In the case of elementary OS 6, we started building Early Access builds all the way back in August, 2020. Sponsors of elementary have had access since then, but we do not recommend anyone uses Early Access builds on their day-to-day computer as there are frequently breaking issues due to the nature of early development. Because they use the daily repos, it is not possible to cleanly upgrade from Early Access builds to the stable release.

Beta releases are a snapshot of Early Access builds once the developer platform has stabilized. At this point, we invite app developers to begin building and testing their apps on elementary OS. They're still built on the daily repos, so we still caution against using beta releases as your daily driver, and it is still not possible to cleanly upgrade to the stable release. But things should be more stable—especially around developer-facing APIs. **You are here.**

<aside markdown="1">
>Beta releases are a snapshot of Early Access builds… we still caution against using beta releases as your daily driver
</aside>

Release Candidates are what they sound like: candidates for the stable release. These are built on the stable repositories, benefiting from the more vigorous human testing that goes into stable releases. At this point, we consider the release "complete," and any further work is finding and fixing remaining bugs before the stable release.

Once we are comfortable with the state of the latest Release Candidate, we promote it to the stable release.

## What's new?

Lucky for developers, we've been detailing the changes in elementary OS 6 since August of last year. To start, you might want to check out the very first blog post about elementary OS 6, where we highlight what's to come:

<div>
{% assign post = site.posts | where:"slug", "updates-for-july-2020" | first %}
{% include featured.html post=post %}
</div>

But here's a recap for you all in one place, as well as links to more detailed individual blog posts if you missed them.

### Platform Changes

There is _a lot_ new under the hood in elementary OS 6. The new Settings Daemon improves reliability and enables new features like the automatic time-based dark style preference. The new screen shield improves reliability of suspend, locking, and unlocking while enabling new features like continued music playback even when your display has gone to sleep. A new screenshot interface simplifies the Screenshot app, improves consistency between the app and using keyboard shortcuts, and even enables new features like taking a screenshot of an app from its window context menu. An all-new notifications system brings native GTK features to notifications bubbles as well as a new multi-touch friendly design for the notifications indicator.

<div>
{% assign post = site.posts | where:"slug", "platform-changes-in-elementary-os-6" | first %}
{% include featured.html post=post %}
</div>

Speaking of multi-touch, there are two major new platform inclusions: Touchégg and LibHandy. Touchégg enables multi-touch gestures in the window manager—e.g. for switching between workspaces, while the inclusion of LibHandy also enables easy multi-touch gestures throughout apps.

<div>
{% assign post = site.posts | where:"slug", "multitouch-gestures-in-elementary-os-6" | first %}
{% include featured.html post=post %}
</div>

For app developers, we encourage you to look into LibHandy and some of the first-party apps on elementary OS 6 to see how we're using it for multi-touch. In particular, replacing Gtk.Stack with Hdy.Deck will enable swipe gestures for navigation, while Hdy.Carousel is great for pagination while supporting multi-touch swipes.

### Look & Feel

elementary OS 6 is coming with an all-new system stylesheet that retains the essential feel of elementary OS while honing in on the use of elevation and shadow—all while enabling great new user-facing features like system-wide accent colors and a dark style preference. We've also refreshed typography, unifying on the Inter typeface in various weights. App developers, be sure to test your apps against the new stylesheet and typography to ensure your app looks and feels as good as possible—and consistent with our first-party apps.

We're also making heavy use of LibHandy throughout the default apps, and we encourage you to look into it as well; there are new Hdy.Avatars, Hdy.Window enables rounded bottom corners and easy dragging from any widget, and Handy includes a few layout helpers to make it easier to adapt your app's interface across small to large displays.

<div>
{% assign post = site.posts | where:"slug", "look-and-feel-changes-elementary-os-6" | first %}
{% include featured.html post=post %}
</div>

And as we've been teasing quite a bit, elementary OS 6 introduces a dark style preference for the first time. Importantly, this is **opt-in** for app developers; by default, your app will behave the same as in previous versions of elementary OS, using the light or dark variant of the stylesheet—whichever it requests. But in elementary OS 6, your app can bind to [Granite.Settings.ColorScheme](https://valadoc.org/granite/Granite.Settings.ColorScheme.html) to respond to the user's preference, e.g. by requesting the dark stylesheet variant and providing alternate in-app styles. For most apps, we recommend just going along with the user's preference by default—but if your app has a specialized use or multiple color schemes, you should start considering how your app will respond to the user's preference.

<div>
{% assign post = site.posts | where:"slug", "dark-style-progress" | first %}
{% include featured.html post=post %}
</div>

### New & Updated Apps, Other User-facing Features

While we'll save the full rundown of new features for the stable release blog post, we do have some new apps and features that we'd love beta tester feedback on.

Mail has been completely rewritten; instead of relying on the custom Geary mail back-end, it now uses the system's Evolution Data Server which brings much wider mail server compatibility. Tasks is a new app that also talks to Evolution Data Server, enabling seeing and synchronizing your to-dos to various services. Currently, **setting an account up requires installing Evolution from AppCenter** and configuring it there; for the stable release this will be set up in Online Accounts settings, but that work is incomplete.

Files has a rewritten sidebar and—after a lot of testing and user feedback—a new navigation mode: single-click to navigate within the app with a double click to open files in their default app. Files has always been single-click to open, but this new hybrid approach strikes a balance between fast, consistent navigation while avoiding accidental opens of large files.

We've also redesigned a few System Settings views, and welcome feedback about them: Desktop has gotten a lot of attention to the Appearance tab with the new dark style preferences, accent colors, and dyslexia-friendly text setting. The Hot Corners tab has also been renamed to Multitasking with the addition of toggles for moving windows to a new workspace when entering fullscreen or maximizing. New gestures preferences have been added to Mouse & Touchpad settings. Date & Time settings have been redesigned with an easier to use time zone selection and new controls for what to show in the Date & Time indicator on the Panel. The "About" view in System Settings has been renamed "System" and completely redesigned with the important addition displaying and updating device firmware.

### Installer

The [new installer for elementary OS](/meet-the-upcoming-installer) is finally here and brings much faster and more straightforward installs for both end users and OEMs. This is an area we would appreciate a lot of testing across different hardware and configurations, so if you are able to spare a non-primary machine for elementary OS testing, start by installing it!

<div>
{% assign post = site.posts | where:"slug", "meet-the-upcoming-installer" | first %}
{% include featured.html post=post %}
</div>

## Developer Experience

With any release comes updates to the developer experience, documentation, and publishing workflow—and elementary OS 6 is no different! We've been working hard to update the [Human Interface Guidelines](https://docs.elementary.io/hig) to better answer developer questions and include newer design patterns

## Release Schedule

At this stage of development, we don't have a release date set for elementary OS 6; that will come once we receive and address beta feedback from users and early testers. We do expect a second beta release and at least one Release Candidate before the stable release.

## Get It

If you're an app developer or eager tester, you can get elementary OS 6 Beta today from our Early Access site. While Early Access builds are typically limited to GitHub Sponsors, beta releases are being made available to the general public in the interest of wider testing and app development.

<div style="text-align: center" markdown="1">
[Download elementary OS 6 Beta](https://builds.elementary.io){: .button }
</div>

- We **do not recommend using beta builds on your primary device**, as irrecoverable crashes and data loss are possible.

- **It will not be possible to upgrade to the stable release** from beta builds.

- Several **user-facing features are unfinished** and in rapid development; beta releases are intended for developers.
