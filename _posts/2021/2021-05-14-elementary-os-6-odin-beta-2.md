---
title: elementary OS 6 Beta 2 Now Available
description: Here's what’s new since Beta 1
author: cassidyjames
image: /images/updates-for-july-2020/card.png
tags:
  - early-access
  - odin
  - devs
---

Developers and testers, elementary OS 6 Beta 2 is available now! For a refresher on what a beta is, the release schedule, and how to provide feedback, see the [Beta 1 announcement].

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "elementary-os-6-odin-beta" | first %}
{% include featured.html post=post %}
</div>

## What's New Since Beta 1

So, what have we been up to for the past couple weeks? The biggest changes in beta 2 are related to the OS installer and Flatpak.

### Installer

We've been putting lot of polish and cleanup into the installer UI. We've insured the various views no longer resize the window, we reworked the layout in a few of the views to be more consistent with one another, and we added a pleasant animation to the installation progress view instead of just a static icon. We've also improved disk detection and error handling when failing to install on certain setups.

Since the installer is such a critical part of the OS, we highly encourage you to reinstall from Beta 2 if you have been developing on and testing elementary OS 6. It's important we ensure it works well across a wide variety of hardware so people can enjoy the latest elementary OS on their devices.

### Flatpak

We've continued our efforts to ship first-party apps as Flatpak in Beta 2. Compared to Beta 1, Beta 2 now comes with Screenshot as a Flatpak app. As a user, it's entirely transparent: keyboard shortcuts and the window context menu work as they did before for taking screenshots since they're handled by Gala, and the Screenshot app itself launches and behaves just as before—it just happens to be packaged in a different way under the hood. As the beta process progresses, we plan to transition even more apps over from Debian packages to Flatpaks provided by our Flatpak repository.

A major fix since Beta 1 is the inclusion of FreeDesktop Flatpak extensions in Beta 2; this ensures things like rendering in Web works correctly on more web pages—if you had tab crashes in Beta 1, you'll want to get Beta 2 for the fix.

## Get It

If you're an app developer or eager tester, you can get elementary OS 6 Beta 2 for 64-bit AMD/Intel today from our builds site. While Early Access builds are limited to GitHub Sponsors, beta releases are being made available to the general public in the interest of wider testing and app development.

<div style="text-align: center" markdown="1">
[Download elementary OS 6 Beta 2](https://builds.elementary.io){: .button }
</div>

**We encourage all testers of Beta 1 to perform a fresh install**; some configuration changes and Flatpak fixes will not be automatically applied on Beta 1 since they are implemented when the OS image is built.

## Disclaimer & Known Issues

As with any pre-release software, there are are some known issues in this beta release. Check the [public project board] for known regressions, as well as the progress towards the stable release. And as always:

- We **do not recommend using beta builds on your primary device**, as irrecoverable crashes and data loss are possible.

- **It will not be possible to upgrade to the stable release** from beta builds.

- Some **user-facing features are unfinished** and in rapid development; beta releases are intended for developers.

[Beta 1 announcement]: /elementary-os-6-odin-beta
[public project board]: https://github.com/orgs/elementary/projects/55
