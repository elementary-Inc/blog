---
title: Updates for January, 2022
description: What’s new in OS 6.1, plus shifting development to OS 7
author: cassidyjames
image: /images/elementary-os-6-odin-updates-september-2021/card.jpg

tags:
  - updates
  - jolnir

sponsor:
  name: Colin Dean
  link: https://www.codeandsupply.co/
  hook: "Colin Dean is a software engineer, community builder, and non-profit leader from Pittsburgh, Pennsylvania in the United States."
---

We just [released OS 6.1](/elementary-os-6-1-available-now) in December, and this month we're back with a handful of updates and fixes.

An update to Mail brings support for the unified Inbox view to Microsoft 365 accounts, enabling more users to mix e.g. their work and personal inboxes into one super view. We also fixed a few rare freezes and crashes, and fixed duplicate sender addresses when composing messages. As a nice detail, the compose window now uses the subject as the window title to make things easier to find in the Multitasking View and the <kbd>Alt</kbd><kbd>Tab</kbd> window switcher.

<figure>
  {% include picture.html src="mail.png" dark="mail-dark.png" alt="Screenshot of mail compose window" width="651" height="571" %}
  <figcaption>Mail now uses the subject line as the window title when composing</figcaption>
</figure>

We added a confirmation dialog for deleting in Calendar to prevent accidentally wrecking your events—especially helpful for shared and recurring events. You can also now <kbd>Ctrl</kbd><kbd>Click</kbd> links and email addresses in event descriptions to visit them or send a new message.

And rounding out the office productivity apps, we pushed an update to Tasks adding notifications for due tasks so you're more likely to remember and accomplish your to-dos.

There were also a handful of smaller updates throughout the month: we pushed an update to Files to show keyboard shortcuts for New Tab and New Window actions in the context menu—and we fixed a couple of crashes and interaction issues along the way. An update to Network settings fixes an issue with wired connections repeatedly reconnecting. We fixed a potential crash in Videos with certain media codecs. And lastly, we updated our Portals component to fix a number of issues with focus, positioning, animations, and crashes.

## Shifting Development to OS 7

At this point in the development cycle, we've started to shift our focus to developing elementary OS 7, the next major release. OS 6.1 will continue to receive updates and security fixes to underlying components from the Ubuntu repositories, and we'll continue releasing updates to the core apps and components as we're able—but in some cases, we're focusing on new OS features that rely on underlying technologies that are not available in the OS 6 base.

All Flatpak apps will continue receiving regular updates in perpetuity; this includes default apps like Archive Manager, Calculator, Camera, Captive Network Assistant, Document Viewer, Screenshot, Videos, and Web. This also includes all curated apps from AppCenter as well as any sideloaded apps from other source like Flathub.

For OS 7 specifically, we've started a number of initiatives that we hope to see through to the final release. This is in no way a comprehensive or final list of features, but just what we're currently working on:

- **A major update and rethinking of the Music app.** We're hearing more often that users are relying on music streaming services and just want a simpler local audio player experience; we've begun work to rethink Music from the ground up as a simpler queue-based audio player that also takes advantages of new technologies like Flatpak and GTK4 from the start. It's still early days here, but the initial work is exciting.

- **Auto updates in AppCenter.** With Flatpak, it's much less risky to automatically update apps in the background because (unlike with Debian packages) the update isn't applied until it has completely succeeded and the app has been restarted. At the same time, we need to consider that non-curated Flatpaks could change their sandboxing out from under users with a simple update. We also need to consider the "try for free" use case for paid apps, where a user can install a paid app for $0 but is prompted to pay again upon an update. Some work in this direction has been merged into AppCenter already, but we still need to sort out the exact experience—and most importantly, messaging.

- **Power profile support in System Settings and the Panel.** You may be familiar with "power management" features on other desktops that enable choosing between power saver, a default balanced mode, and a performance mode. We're able to ship this functionality in elementary OS 7, hooking into the device's power management when supported to e.g. either extend battery life or crank up the performance at the expense of fan noise. There's work towards supporting this in the Power settings already, and we hope to also add a quicker way to change modes to the Panel indicator as well.

- **GTK4 and an improved developer platform.** OS 7 will come with GTK4 natively, and our updated Flatpak runtime includes everything developers need to start working with it today, including an updated system stylesheet. We're actively working to port a number of apps and desktop components to GTK4 to take advantage of newer features and improved performance; we've already completed simpler components like Onboarding and Shortcut Overlay, and have branches open for many more.

- **Super experimental: OS upgrades!** We debated mentioning this, but it's such a hugely-requested feature—and we are in the planning and experimentation phase. **It's possible this will not be ready in time for the release of OS 7**, but we're currently working on a way to prompt OS 6 users of an OS upgrade, to reboot to install the update "offline" (while not logged in), and then to reboot into OS 7. While early work is promising, it will require a _ton_ of testing to ensure it's production-ready. And again, it may or may not make the cut in time for the OS 7 release.

## Sponsors & Early Access

If you want to get your hands on super early builds of elementary OS 7, you're in luck! [Early Access] is up and running with experimental daily builds built from an Ubuntu 22.04 LTS alpha base and the elementary daily repositories, meaning you're getting multiple layers of bleeding-edge software. But if you're wanting to follow along with the development cycle, it's the best way to do so—just keep it off your production machines for now, as major issues are to be expected at this point.

As a reminder, all [GitHub Sponsors] at or above the $10 tier get ongoing Early Access as long as you're subscribed, and the Early Access site includes easy downloads of the latest:

- stable and release candidate builds
- bleeding-edge daily builds
- experimental builds for platforms like Pinebook Pro & Raspberry Pi 4

You also get access to the past month of daily builds for all platforms to aid in debugging or in case the latest build isn't working for you.

<div style="text-align: center" markdown="1">
[GitHub Sponsors]{: .button.flat }
[Get Early Access][early access]{: .button.suggested }
</div>

[early access]: https://builds.elementary.io/
[GitHub Sponsors]: https://github.com/sponsors/elementary
