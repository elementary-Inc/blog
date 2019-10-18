---
title: Rebuilding elementary OS
description: Our road to a better release process, automated builds, and more
author: cassidyjames
tags:
  - github
  - infrastructure
  - juno
---

If you've been following elementary OS, your top thought right now is probably, “Where’s 5.1?” If you've been following elementary OS for quite some time, you're _also_ probably familiar with our unofficial, “When it's ready” release schedule—we don't announce things until we're absolutely sure it's going to ship, and we don't release until we're very confident in the end result—even if that means we take a bit longer than people would like.

This work on our 5.1 release has been particularly difficult and lengthy. We ambitiously set the major milestone of completely reworking how the OS is both built by us and installed by users for our 5.1 release, and consequently there have been more roadblocks than expected. We're working through them, but we understand that people are getting antsy. That's partially on us; perhaps we should have had more discretion with sharing our goals, but we're very excited about this upcoming release and it's just been hard to keep quiet about it.

## The Scope of 5.1

In an effort to get 5.1 out to users more quickly, we've decided to bump the new installer to a future release. Too many issues remain with the integration right now, and the existing Ubiquity installer—while perhaps a bit long in the tooth—continues to work as it always has. This means 5.1 will be focused around five key areas:

1. A brand new Greeter and Onboarding experience
2. Flatpak support with Sideload and AppCenter
3. Major updates around accessibility and System Settings
4. Iterative improvements across several apps
5. The latest hardware enablement and support

Under the hood, 5.1 will also bring an entirely new process for building ISOs that is faster, better documented, and more reproducible.

We've been working on these updates for the past year, and we're confident 5.1 will be a substantial update that existing and new users alike will love. We'll have the usual detailed release notes here on the blog once it's officially released. Since elementary OS 5 Juno is effectively rolling, many of these updates have actually already rolled out to users, and users of 5.0 will be upgraded to 5.1. As mentioned in the August updates, the new HWE can be installed manually on existing installs, but will be included by default with new 5.1 installs.

## Documenting Processes

One major hurdle with all of this work is that there was a substantial lack of documentation around our ISO building and release process. Consequently, only one person was responsible for or even knowledgeable about how we actually bake elementary OS into the final product we deliver to users. That was unacceptable, and we're well on our way to fixing it.

### Package Releases

Every piece of a software update for elementary OS is delivered to users' devices as a "package" of compiled code. This package is built from the source code we host on GitHub, but delivered via the Launchpad infrastructure. When we feel a specific component is ready to be sent out as an update, we create a "release" on GitHub, that snapshot of the code is pulled in and built by Launchpad, it's placed into the Lauchpad repository, users' devices regularly query that repository for available updates, then the package is downloaded and installed.

This process is a bit complex, so we've started by documenting the current package release process on the [OS wiki](https://github.com/elementary/os/wiki/Release-Process). As we discussed and documented it, we realized how much was one-off human labor that could be largely automated. So at the same time, we came up with and documented a more ideal process that uses our CI integrations to create the right files, tag the release, and trigger builds. There's still a bit of human interaction, but it's much less work and fits into our regular development workflow much better. Work towards this more ideal process is underway and we look forward to starting to use it in production for upcoming package releases.

### ISO Building

If you thought package releases were complex, ISO building is on a whole other level. When we want to make a downloadable version of elementary OS, we use a collection of scripts to build the OS from Debian Live Build, packages from the Ubuntu repositories, and packages from our Launchpad repos. Some packages are built by taking the upstream source code and applying our own patches, since the original code was designed for Ubuntu and not elementary OS. Once the OS is built, the resulting ISO must then be tested to ensure it: boots across a variety of hardware; installs successfully BIOS, UEFI, Secure Boot, with and without Internet, etc.; and ends up with a correct install.

This process had no real documentation or visibility, so we've been working on documenting and moving the ISO building process to GitHub CI as well. Before, there were disparate scripts and lengthy docs scattered about from nearly a decade of building elementary OS, but no definitive, “this is how we do it today.” We're happy to be working with dedicated volunteers and contributors like Keli Grubb, Martin Wimpress, and Corentin Noël to get things into shape.

A functional ISO building process has been documented and is being tested in the [OS repo on GitHub](https://github.com/elementary/os). We're still working out some kinks, but getting this information documented and public has given us a baseline to build from.

## What's Next

Now that we have a baseline for both package releases and ISO builds, we're testing them and starting to use them in production. 5.1 will feature this work, and be released once we are confident it is robust and reliable. Updates to 5.0 in the meantime will also begin to use the updated package release process.

If you're interested in getting involved in this work, we highly recommend checking out the [OS repo] and [release process on the wiki]. You can also jump into our [Community Slack] to get in touch with the team.
