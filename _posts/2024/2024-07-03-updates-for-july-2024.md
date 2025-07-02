---
title: It's Disability Pride Month! Let's Get Accessible
description: OS 8 progress and community updates from June
author: danrabbit
image: /images/updates-for-july-2024/settings-system.png

tags:
  - earlyaccess
  - horus
  - updates
  - accessibility
---

This month we have several community updates, a couple of Flatpak releases available on OS 7, and plenty of OS 8 news.

## Disability Pride Month

It's disability pride month, which means making space to talk about how we can build communities and systems that better accommodate people with disabilities. Last year for disability pride month we announced [color deficiency assistance filters](https://blog.elementary.io/updates-for-june-2023/) and a new feature that reads out the keyboard shortcut for the screen reader during Installation &amp; Initial Setup. You might also be familiar with our [Curb Cuts](https://blog.elementary.io/accessibility-features-are-just-features/) initiative that was started a few years ago and how we [completed it in OS 7.1](https://blog.elementary.io/os-7-1-available-now/). We also expanded the number of places affected by the Reduce Motion setting, increased the upper intensity limit for Night Light, and made sure accommodations were present on the Lock Screen.

This year we had the pleasure of being introduced to [Florian Beijers](https://www.twitch.tv/ic_null) who describes himself as a fully blind cybersecurity enthusiast. You may have heard him recently on [Linux After Dark](https://latenightlinux.com/linux-after-dark-episode-72/) talking about accessibility on Linux desktops generally. [A couple weeks ago](https://www.youtube.com/watch?v=7jOB4lZH3AE), he took some time to take a look at the state of OS 8 with regards to accessibility for someone who has no vision at all, and I'll be honest we were definitely humbled by his experience. We took notes, filed issue reports, and I'm proud to say we've already taken meaningful steps towards addressing his feedback with fixes across the desktop and in our platform libraries, but there's clearly a long way for us to go! If you want to follow along or help us address accessibility issues in elementary OS, we'd love your help! We're tracking issues in [this GitHub project](https://github.com/orgs/elementary/projects/111). If you discover a new issue—accessibility related or otherwise—we'd love to get your feedback and we have a handy contributor guide to help you [file a report here](https://docs.elementary.io/contributor-guide/feedback/reporting-issues).

## Community

We've moved our recommended community chat from Slack to Discord! You may know that we've had quite a bit of trouble keeping the invite link for Slack active which has really prevented that community from growing and staying vibrant. There's also been issues with the policies for Slack's free tier around keeping/deleting messages and generally we recognize that at its core Slack is a product for workplaces, not for building communities. So after a bit of poking around and discussion, we're now recommending folks join the [community Discord server](https://discord.com/invite/kwRyqGCzm5) instead. So far we're already at over 330 members and it's been a much more active and lively place than the Slack was. Plus, we have dedicated moderators besides the core team of developers. Thanks to [Tiana](https://kakii87.net) and [Tony](https://thattonybo.com) for creating this community and being our mods!

<div style="text-align: center" markdown="1">
[Join us on Discord](https://discord.com/invite/kwRyqGCzm5){: .button.suggested }
</div>

Fedora is asking for contributors to join the [Pantheon special interest group](https://fedoraproject.org/wiki/SIGs/Pantheon). If you're interested in running our desktop environment on Fedora or contributing to maintaining it on Fedora, they'd love to hear from you!

## OS 7 Updates

Photos 8 has been released to AppCenter as a Flatpak app. This means you can continue to receive updates to Photos by installing the Flatpak version from AppCenter even on older versions of elementary OS, and Photos is now [easily available](http://flatpak.elementary.io/repo/appstream/io.elementary.photos.flatpakref) to folks running Linux distributions other than elementary OS. This new version of Photos is largely a maintenance release so don't expect any major design changes or new features, but it now uses the Wallpaper and Open Directory portals improving cross-platform compatibility.

The Captive Network Assistant was also updated to version 8. This release contains the update to GTK4 and the latest WebKit which improves its performance and web compatibility as well as a couple of bug fixes.

---

## AppCenter

Another couple of big design updates landed in AppCenter in June! Pages now draw their own individual headers, which means we can show more contextual controls and have more design freedom. You'll notice that options related to updates have now moved to the Updates &amp; Installed Apps page, for example. On App info pages, main action buttons like Install and Open are now always available from the headerbar, and when you scroll past an app's banner a smaller icon and app title will appear.

<figure class="third" markdown="1">
![AppCenter home page](/images/{{ page.slug }}/appcenter-home.png)
![AppCenter updates page](/images/{{ page.slug }}/appcenter-updates.png)
![AppCenter app info page](/images/{{ page.slug }}/appcenter-appinfo.png)
<figcaption>AppCenter has a flatter design where each page has unique headerbar contents</figcaption>
</figure>

The links section of App Info pages has also been redesigned, featuring colorful iconography and an expanded set of supported links. We now show a Sponsor link for apps who monetize outside of AppCenter and we show a link directly to the app's source code for apps that provide it.

Plus we've made a ton of cleanups, bug fixes, and performance improvements, especially around updates. And AppCenter now starts much faster thanks to [Leonhard](https://github.com/leolost2605).

## System Settings

Locale settings saw the biggest improvements with a new setting for automatically selecting the temperature unit based on locale, fixed freezing while getting advanced permissions, and it will no longer prompt system administrators for a password unnecessarily for setting the system language. Plus we made some improvements to error handling and other feedback.

<figure markdown="1">
![](/images/{{ page.slug }}/settings-system.png)
<figcaption markdown="1">
Operating System settings has a redesigned links section
</figcaption>
</figure>

System got a redesign of external links similar to the one in AppCenter, with clearer help and documentation links as well as a better call for contributions. Plus, network settings now shows the name of connected wireless networks in the sidebar and we fixed a missing icon for some wireless headphones in Bluetooth settings.

## And More

The Screencast portal landed this past month, meaning screen recording applications are now able to capture the screen in the Wayland session, thanks again to [Leonhard](https://github.com/leolost2605).

Code now uses the TabBar widget from LibHandy instead of the deprecated widget from Granite, an important step in porting to GTK 4. There's also been a lot of progress towards using GLib.Action and modernizing menus thanks to [Colin](https://github.com/colinkiama).

And we have [a new GitHub project](https://github.com/orgs/elementary/projects/138) for tracking issues with hardware that ships with elementary OS, including the [StarLite Mk V](https://us.starlabs.systems/pages/starlite).

## Release Planning

At this point OS 8 is almost finished! We're currently making releases for every single one of the nearly 150 repositories that make up Pantheon and elementary OS. This involves things like writing release notes, taking screenshots, checking for regressions and merging last minute fixes etc. Some of these releases will trickle back to OS 7, but many of them will be OS 8 exclusive as they rely on big under-the-hood changes that can't easily be backported.

We're also putting the finishing touches on our Wayland session and fixing the last few major bugs and regressions there. We're nearly at parity with the X11 session and I've personally been using it every day with only minor issues! But don't worry the X11 session will be sticking around if you need it. One small concession we've needed to make is that we'll almost certainly be shipping our fork of Plank for use in the X11 session. So the dock experience between Wayland and X11 will be slightly different in this release and you'll only get the features of the new dock when running under Wayland.

As always you can follow along with our progress towards the release of OS 8 in [this GitHub project](https://github.com/orgs/elementary/projects/128/views/1). Hang tight, we're almost there!

---

## Sponsors

At the moment we're just above 21% of our monthly funding goal and we're at 365 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

We're also now automatically building monthly release candidate quality stable builds! These builds are created on the 1st of every month and include all stable updates for the current stable OS series. They have not been reviewed by a human, but should usually be of high quality. Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier!

Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
