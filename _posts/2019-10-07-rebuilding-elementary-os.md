---
title: Rebuilding elementary OS
description: Our road to a better release process, automated builds, and more
author: cassidyjames
---

If you've been following elementary OS, your top thought right now is probably, “Where’s 5.1?” If you've been following elementary OS for quite some time, you're _also_ probably familiar with our unofficial, “When it's ready” release schedule—we don't announce things until we're absolutely sure it's going to ship, and we don't release until we're very confident in the end result—even if that means we take a bit longer than people would like.

This work on our 5.1 release has been particularly difficult and lengthy. We ambitiously set the major milestone of completely reworking how the OS is both built by us and installed by users for our 5.1 release, and consequently there have been more roadblocks than expected. We're working through them, but we understand that people are getting antsy. That's partially on us; perhaps we should have had more discretion with sharing our goals, but we're very excited about this upcoming release and it's just been hard to keep quiet about it.

In an effort to get 5.1 out to users more quickly, we've decided to bump the new installer to a 5.2 release. Too many issues remain with the integration right now, and the existing Ubiquity installer—while perhaps a bit long in the tooth—continues to work as it always has. This means 5.1 will be focused around the new hardware enablement (HWE) stack, a new process for building ISOs, the new Greeter, the new Onboarding experience, major updates to core apps, updated libraries and developer tools, and refinements to the visual style; we've been working on these updates for the past year, and we're confident it's still a substantial update that existing and new users alike will love. We'll have the usual detailed release notes here on the blog once 5.1 is officially released.

Since elementary OS Juno is effectively rolling, many of these updates have actually already rolled out to users. As mentioned in the August updates, the new HWE can be installed manually on existing installs, but will be included by default with new 5.1 installs.

## Documentation

One major hurdle with all of this work is that there was a substantial lack of documentation around our ISO building and release process. Consequently, only one person was responsible for or even knowledgeable about how we actually bake elementary OS into the final product we deliver to users. That was unacceptable, and we're well on our way to fixing it.

First, we've documented the current package release process on the [OS wiki](https://github.com/elementary/os/wiki/Release-Process). As we discussed and documented it, we realized how much was one-off human labor that could be largely automated. So at the same time, we came up with and documented a more ideal process that uses our CI integrations to create the right files, tag the release, and trigger builds. There's still a bit of human interaction, but it's much less work and fits into our regular development workflow much better. Work towards this more ideal process is underway and we look forward to starting to use it in production for upcoming package releases.

Next, we've been working on documenting and moving the ISO building process to GitHub CI as well. Before, there were disparate scripts and lengthy docs scattered about from nearly a decade of building elementary OS, but no definitive, “this is how we do it today.” We're happy to be working with dedicated volunteers and contributors like Keli Grubb, Martin Wimpress, and Corentin Noël to get things into shape.

## The New Way

So, how is elementary OS built now?

…

## 





