---
title: Updates for October, 2022
description: Oh yeah, it's all coming together
author: danrabbit
image: /images/updates-for-april-2022/card.jpg

tags:
  - horus

sponsor:
  name: Marco Teixeira
  link: https://github.com/marcoPTTeixeira
---

This month featured a slew of minor updates and translation updates on OS 6.1 as a side effect of preparing stable builds of OS 7, but the focus for the team is solidly on putting the finishing touches on the new major release.

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

If you've been following along on the [OS 7 Project Board](https://github.com/orgs/elementary/projects/94/views/1), you'll have noticed that all of the blocking window manager issues have now been resolved! Major shoutouts to [Corentin Noël](https://github.com/tintou) and [David Hewitt](https://github.com/davidmhewitt) here for finishing those off. I also want to give a special thanks to [Bobby Rong](https://github.com/bobby285271), the maintainer of Pantheon on NixOS, for noticing a couple of regressions that slipped through the cracks and quickly reporting them upstream.

At this point the outstanding tasks for releasing OS 7 largely have to do with builds, infrastructure, etc. We're really in the home stretch now! But that doesn't mean we can't try to sneak in some last minute polish. I've been revisiting the [App Icon Redesign Project](https://github.com/orgs/elementary/projects/110) and have several outstanding branches here that will hopefully make it into 7.0. [Micah Ilbery](https://github.com/micahilbery) and I have been working on modernizing the look of app icons on elementary OS, including increasing the border radius of tile icons, improving contrast and use of color, and adding a bit more dimensionality to icons that make use of overlaid glyphs.

<figure class="card" markdown="1">
![The Dock](/images/updates-for-october-2022/dock.png)
<figcaption markdown="1">
A uniform dock featuring some of the new and proposed app icons
</figcaption>
</figure>

Also to be expected soon is the latest Flatpak platform. Platform 7.1 is based on the GNOME 43 platform and brings a number of improvements for Gtk 4. We're excited to get it published and available for use in your apps right away as well as updating the GNOME apps we ship to their latest releases. Thanks to the magic of Flatpak, OS 6.1 users can expect to receive this update as well.

I was tempted to spend more time this month talking about what will be in the stable releases you can expect to be using in OS 7.0, but I'll save the more in-depth look into changes for each app and system component for the OS 7 release blog post. I can't wait to roundup all of the great new features and changes that have landed over the last year of development. Looking forward to seeing you in that post soon!

## Early Access Preview

If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/).
