---
title: Package Releases Are Almost Done, You Won't Believe What Happens Next!
description: A brief update with important features
author: danrabbit
image: /images/updates-for-september-2024/

tags:
  - earlyaccess
  - horus
  - updates
---

This month's update is fairly brief since a lot of what we did last month was minor bug fixes, regression testing, updating metadata, taking screenshots, and releasing packages. We're getting down to the last few items before we can release elementary OS 8. Read ahead to find out more!

# OS 7 Updates

Just a couple of small OS 7 updates this month! [Ryan](https://github.com/zeebok) backported a fix for an issue in AppCenter where the updates page would continue to show the loading screen after it was finished loading. And the latest Network Indicator was released and now shows cellular modems as toggle buttons like it does with other devices.

<figure class="card" markdown="1">
![Power Indicator](/images/{{ page.slug }}/indicator-network.png)
<figcaption markdown="1">
Cellular modems now show as toggle buttons
</figcaption>
</figure>

---

# OS 8 Updates

Continuing on with our work to vastly improve screen reader support this cycle, [Leo](https://github.com/lenemter) implemented the accessibility interface in the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher! [Leonhard](https://github.com/leolost2605) added a new option to the system shutdown dialog so you can choose to skip a pending update, even when automatic updates are enabled.

<figure markdown="1">
![Shutdown Dialog](/images/{{ page.slug }}/shutdown.png)
<figcaption markdown="1">
You can choose to skip updates when shutting down or restarting
</figcaption>
</figure>

If you have a mixed-dpi setup—like a HiDPI laptop or tablet and a LoDPI external monitor—You can now set per-display scaling in the Secure Session thanks to [Leonhard](https://github.com/leolost2605). And power modes can also now be quickly changed from the power indicator thanks to [Subhadeep](https://github.com/SubhadeepJasu).

<figure class="card" markdown="1">
![Power Indicator](/images/{{ page.slug }}/indicator-power.png)
<figcaption markdown="1">
Power modes now appear in the power indicator
</figcaption>
</figure>

## Release Planning

Last month we finished releasing nearly every component that makes up elementary OS—over 80 packages. The only thing left is the Login & Lock Screen which is blocked by two small issues. We also have just two more OS patches to complete. Once these issues are resolved and the Login & Lock Screen has a package release, we can build release-candidate images of elementary OS 8 from the stable updates channel—and these builds will be available to Sponsors in Early Access right away. There's still a couple more issues we want to try to solve before the final public OS 8 release, but we're very close! As always you can follow along with our progress towards the release of OS 8 in [this GitHub project](https://github.com/orgs/elementary/projects/128/views/1). When this project board is empty, it's public release time!

---

## Sponsors

At the moment we're at 20% of our monthly funding goal and 385 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
