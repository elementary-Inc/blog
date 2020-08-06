---
title: "Let's Talk elementary OS 6"
description: "Updates for July, plus early access to the next major version"
author: cassidyjames
tags:
  - updates
---

Unlike many operating systems—especially in the open source desktop space—elementary OS gets frequent updates _between_ major versions. This means throughout the elementary OS 5 lifecycle, we released [updates every month](/tags/#updates), oftentimes including not just fixes, but major features like a brand new first-run experience including a [new login/lock screen greeter](/say-hello-to-the-new-greeter/), initial setup, and [welcome](/get-settled-into-elementary-os-with-onboarding/); [Flatpak support](/updates-for-october-2019/) with Sideload and AppCenter; exposing keyboard shortcuts across the system; broad [accessible settings updates](/accessibility-features-are-just-features/); and much more. At the same time, curated apps designed for elementary OS are constantly released and updated by their developers on AppCenter.

This semi- "rolling release" cycle means elementary OS users get the latest features, fixes, and updates to their favorite operating system and apps very rapidly, without having to wait around for a new major release. However, there comes a time in the release cycle when we need to shift our resources and priorities to major updates that will bring a newer Ubuntu core and repositories, plus major technological improvements under the hood. And as we [mentioned last month](/updates-for-june-2020/), that shift has begun.

## Updates to elementary OS 5.1 Hera

Hera will continue to receive security and stability updates to its underlying libraries from the Ubuntu LTS repositories until April of 2028, courtesy of Canonical. But our primary focus at elementary has now fully shifted to OS 6.

<!-- TODO: Run down any updates released to users since the Updates for June post -->

## AppCenter for Everyone

In February, we ran launched the [AppCenter for Everyone](/appcenter-for-everyone/) crowdfunding campaign to take the indie, open source app store to the next level. Little did we know that the global COVID-19 pandemic would hit right when we planned to have our in-person sprint. We [smashed our goal](/appcenter-for-everyone-campaign-results/), but had to postpone the in-person sprint in favor of a smaller [remote sprint](/appcenter-for-everyone-remote-sprint/). And to clarify, we have still set aside the funds for an in-person AppCenter for Everyone sprint once it is safe to gather again.

One of the major backer rewards was "early access to elementary OS 6," which we've been hard at work to deliver. Which leads us to…

## Early Access Builds of elementary OS 6

Over the past week, we quietly launched [builds.elementary.io][builds]. This new website hosts early access daily builds of elementary OS as a way to ensure OEMs, developers, testers, supporters, and excited fans can get their hands on up-to-date builds. Now that elementary OS 6 is in an installable and bootable state, we've [begun adding](https://www.indiegogo.com/projects/appcenter-for-everyone/#/updates/21) $25+ AppCenter for Everyone backers to the allowlist, and any $10/month and higher [GitHub Sponsors](https://github.com/sponsors/elementary) get access automatically. And for clarity, the latest stable version of elementary OS will always be available from [elementary.io](https://elementary.io). If you're curious about or want to get your hands on early access builds, check out the new site:

<div style="text-align: center" markdown="1">
[Early Access Builds][builds]{: .button}
</div>

However, there's still _a lot_ of work to do on elementary OS 6 before release. Without going into a ton of detail, here are a few planned features that are still undergoing work:

- **Refreshed look and feel** including typography and the system stylesheet—which affects everything from the panel and system apps to curated apps in AppCenter. Expect improved contrast and a more refined design system while retaining the signature depth and shadows of elementary OS.

- **Dark style for system components** like the Dock, Panel indicators, Keyboard Shortcuts overlay, system dialogs, etc. We are still working out all of the details here, but work is progressing well.

- **User-chosen default accent color** across apps. Apps can still override this if they choose, but previous default blue accent color can be swapped out for a range of playful palette colors including Strawberry, Orange, Banana, Lime, Mint, Grape, and Bubblegum.

- **More multi-touch support** throughout apps, utilizing the Libhandy library. Somewhat related is the use of HdyWindow to enable rounded bottom corners in apps like Terminal and System Settings.

- **A major rewrite of Mail**, leaning on the well-supported and battle-tested Evolution data server instead of the custom Geary mail engine. This is still early and currently requires setting up an account in Evolution until the Online Accounts component is completed.

We'll share updates on elementary OS 6 development along the way, but that's a quick peek behind the curtain for now. As always, if you want to learn more, you're always welcome to [get involved](https://elementary.io/get-involved) and help shape the future of elementary OS.

[builds]: https://builds.elementary.io
