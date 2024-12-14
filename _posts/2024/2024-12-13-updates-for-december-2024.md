---
title: Happy Holidays! We Come Bringing Gifts!
description: It's already time for OS 8 updates
author: danrabbit
image: /images/updates-for-december-2024/settings-system.png

tags:
  - circe
  - updates
---

It's only been a little over 2 weeks since we released elementary OS 8, but we're already back with updates just in time for the holidays!

# Terminal

The headliner this month is Terminal which comes with a bunch of fixes and new features thanks to [Jeremy](https://github.com/jeremypw). It now uses the more modern tab bar widget you're used to from Web, Files, and Code. There's an overlay bar that shows the current zoom level when it changes. We do a better job of handling URIs which contain spaces. And we now show unsafe paste warnings for Drag n Drop operations. Plus, we now show the unsafe paste warning for more commands like `doas` thanks to [Elsie](https://github.com/Elsie19) and there's a new option in the gear menu to toggle unsafe paste alerts thanks to [Stella and Charlie](https://github.com/teamcons). [Michal](https://github.com/cshaa) upped the contrast for gray in our default style and [Igor](https://github.com/igordsm) made sure we focus the relevant tab when notifications are clicked. Plus, we now replace notifications from the same tab and withdraw notifications when a tab is focused, so your notification center should be a lot less noisy. This release was really a group effort with several new contributors, so major shoutouts to everyone who worked on it!

# AppCenter

<figure markdown="1">
![AppCenter](/images/{{ page.slug }}/appcenter.png)
<figcaption markdown="1">
AppCenter will use Dark Mode screenshots when available
</figcaption>
</figure>

Thanks to [Italo](https://github.com/edwood-grant), AppCenter will now use provided dark mode screenshots and brand colors when developers provide them. Plus, he addressed a visual bug with release notes. And [Juan](https://github.com/kerunaru) added support for the latest Appstream Developer tag, so we're staying up on standards.

# Window Manager &amp; Dock

In the Window Manager, [Leo](https://github.com/lenemter) fixed an issue where the dock could sometimes still be clicked when hidden in the Classic session, while [Leonhard](https://github.com/leolost2605) contributed some performance improvements.

In the Dock, [Leonhard](https://github.com/leolost2605) made sure launcher bounces don't run too long for apps that don't notify on startup. [Leo](https://github.com/lenemter) fixed an issue where launchers with large icons could become clipped while they bounce and made sure running indicators have a bit more room to breath. Plus the dock now also respects the "Panel Translucency" setting, making it completely solid when requested for added contrast.

# System Settings

[Alain](https://github.com/alainm23) added some visual polish to the System view as well as a new progress bar that represents how close we are to meeting our monthly sponsorship goal. Plus [Leonhard](https://github.com/leolost2605) made sure automatic updates won't download on metered networks, and we avoid checking for system updates altogether in Demo Mode.

<figure markdown="1">
![System Settings → System](/images/{{ page.slug }}/settings-system.png){: width="869" height="559"}
<figcaption markdown="1">
We now show monthly funding goal progress right in System Settings
</figcaption>
</figure>

You can now prevent Apps from sending notifications from Applications → Permissions, even for apps that don't report their notification usage in Notification settings. and the check mark next to the current language in Language &amp; Region settings will now follow your accent color thanks to [Leo](https://github.com/lenemter).

# Installation &amp; Onboarding

[David](https://github.com/davidmhewitt) fixed a crash with certain partitioning schemes in the Installer's custom install view, and the encrypt view was simplified. Onboarding will now always stay centered on the screen, even when resized.

# Icon Browser

A new version of the Icon Browser for app developers is available in AppCenter that includes the latest icons for Platform 8 as well as a quick button for copying code snippets thanks to [Ryo](https://github.com/ryonakano). And we now focus the search automatically when you start typing, thanks to [Alain](https://github.com/alainm23).

## And More

You can now close the captive network assistant with the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>Q</kbd>, thanks to [Stanisław](https://github.com/stsdc). [Alain](https://github.com/alainm23) fixed copying screenshots to the clipboard. And there a ton of translation updates, especially including traditional Chinese thanks to [Kisaragi](https://github.com/kisaragi-hiu).

---

## Sponsors

At the moment we're at 22% of our monthly funding goal and 430 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
