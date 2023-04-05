---
title: Updates for March, 2023
description: Spring cleaning is in full effect
author: danrabbit
image: /images/updates-for-march-2023/sideload.png

tags:
  - horus
  - updates
---

March was all about bug fixes. This month don't expect too many new features, but instead get excited about improved stability and closed issue reports! The team has been hard at work sorting through your feedback and smoothing out all of the wrinkles.

## Sideload

Since sideloading is an expected and important part of installing apps on elementary OS, we've made a couple of changes to help you stay informed and be in control. Instead of describing sideloaded apps as "Untrusted", we've updated interface copy to instead ask for your trust. Additionally, we now show some basic feedback about the kinds of broad system permissions that a sideloaded app may request. This will likely get more fine-grained in the future, but for now we can warn about apps that request advanced permissions and let you know when an app is more tightly sandboxed.

<figure markdown="1">
![Files](/images/{{ page.slug }}/sideload.png){: width="502" height="334"}
<figcaption markdown="1">
Sideload now shows recommendations regarding sandbox permissions
</figcaption>
</figure>

## Mail & Online Accounts

Early in the month we made a release of Mail that fixed a notorious and pervasive crash thanks to [@leolost2605](https://github.com/leolost2605). This release also contained a fixed for creating links that include a `%` symbol. Look forward to future releases featuring more of their work!

Online Accounts settings was updated with a fix for setting the correct SMTP username when configuring IMAP accounts, thanks to [Stan](https://github.com/stan-janssen). And, [Leo](https://github.com/lenemter) made sure the icons there for Mail and Tasks were updated to their latest versions.

## Terminal

This release was extremely collaborative with quite a few commit authors. It contains fixes related to tab switching shortcuts and makes sure that context menus are updated when activated with the menu key thanks to [Lasne](https://github.com/Faelian) and [Ryo](https://github.com/ryonakano), respectively. [Stan](https://github.com/stan-janssen) also resolved an issue where shortcuts conflicted with some command line apps and added a new option to start Terminal hidden. [Jeremy](https://github.com/jeremypw) also fixed an issue with `#` characters in URLs. Finally, thanks to [Gustavo](https://github.com/marukesu) and [Corentin](https://github.com/tintou) for their work on unit testing and code cleanup in this release.

## Window Management

This is another great bugfix release for Gala with major thanks to [Leo](https://github.com/lenemter). Some of the highlights include fixes for notification windows—including showing them in Multitasking View, fixes for issues with keyboard shortcuts, fixes that prevent misclicks and accidentally triggering actions, performance improvements, fixes for visual glitches, and more. This is another great release to read the [full release notes](https://github.com/elementary/gala/releases/tag/7.0.2) since it closes another dozen reported issues.

## Files

[Jeremy](https://github.com/jeremypw) made a sizable bugfix release of Files including several fixes related to selections and the overlay bar as well as a couple of reported regressions, fixes related to git emblems, and a crash fix.

## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

## Developer Platform

We've released version 7.2 of our Flatpak platform, rebased on the GNOME 44 platform and including the latest Granite, Icons, and Stylesheet. Especially of note are fixes and better support for apps that use widgets from LibAdwaita. And of course this platform update includes the latest version of development libraries like Gtk that include their own bug fixes, performance improvements, etc.

This update is API-breaking in some cases, so Flatpak manifests will have to be updated from using version 7.1 of the runtime to version 7.2.

## Documentation

There were also a number of updates to developers docs including revamped [Actions](https://docs.elementary.io/develop/apis/actions) and [Notifications](https://docs.elementary.io/develop/apis/notifications) sections, and a brand new section on [Popovers](https://docs.elementary.io/develop/writing-apps/popovers). All three include new screenshots and full code samples and have been updated for Gtk 4. Plus, the section on including custom icons using [Gresource](https://docs.elementary.io/develop/apis/gresource) has been updated.

## Early Access Preview

Folks in Early Access may notice a number of large changes to the Onboarding app including new and redesigned pages. We've also been putting quite a bit of work into Code, especially around search. We'd love to get your feedback in GitHub before releasing these changes.

If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/).

## And More

Special thanks to [David](https://github.com/davidmhewitt) this month for his work on CI and CD systems in GitHub. We've now fully migrated from Dockerhub to using the GitHub container registry for our docker containers and he's set up several Dependabot workflows as well as started working with Flatpak external data checker to make sure we're keeping our workflows updated.

I also would like to draw attention to our [Github Sponsoring page](https://github.com/orgs/elementary/sponsoring) where you can see which developers and projects that we sponsor on a monthly basis! I'm hoping to grow this page as revenue allows but I'm excited to start here. I'm especially proud to sponsor [Fabio's](https://github.com/decathorpe) work on making Pantheon available for Fedora.
