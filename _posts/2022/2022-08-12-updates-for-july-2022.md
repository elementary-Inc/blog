---
title: Updates for July, 2022
description: A big themes update for Terminal and OS 7 progress
author: danrabbit
image: /images/elementary-os-6-odin-updates-september-2021/card.jpg

tags:
  - horus
  - jolnir
  - updates
---

Firstly, thank you so much for your patience this month! I've been out sick with COVID for about 3 weeks, so I haven't been able to contribute much or organize releases this month. I want to give a special thanks to our volunteer community who has continued to make improvements and move forward on projects in my absence. I'm excited to catch up and get back to work to make the most of the rest of this month. Having said that, this is going to be a very brief updates post.

<figure class="constrained" markdown="1">
![elementary OS 6.1 Jólnir](/images/elementary-os-6-1-available-now/card.png)
</figure>

## Terminal

The latest release of Terminal can be summed up as a big styles update! Under the hood, we've completely reworked the way styles are loaded and saved to improve performance and make the code much more robust and flexible. There is now an option to follow the system style which will automatically toggle between Solarized Light and Terminal's Dark style depending on the system's dark style preference. We've also updated the default styles to use the latest values from Solarized upstream and by default Terminal is fully opaque to improve contrast and legibility.

<figure class="half" markdown="1">
![New quick settings options](/images/updates-for-july-2022/screenshot-light.png){: width="784" height="552"}
![Custom style dialog](/images/updates-for-july-2022/screenshot-custom-style.png){: width="374" height="554"}
<figcaption markdown="1">
**Left:** New quick settings options in Terminal | **Right:** Create your own custom palettes
</figcaption>
</figure>

A new circle button is available in the quick settings menu for a custom style where you can create your own color palette, choose a dark or light style for Terminal's window, and of course set background opacity to whatever value you feel is comfortable. We're excited to add some long-awaited personalization here and can't wait to here your feedback.

## Get These Updates

As always, pop open AppCenter on elementary OS 6.1 and hit "Update All" to get all these updates plus your regular security, bug fix, and translation updates.

---

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

## Gtk 4 Porting

A ton of energy in the community has gone into [Gtk 4 porting](https://github.com/orgs/elementary/projects/95) for OS 7 and beyond. The team is making steady progress on porting System Settings and we landed the Gtk 4 port for Sideload. We've also uncovered some style issues and gaps in style constants, so if you're working on porting your app to our Flatpak Platform 7, know that we'll be releasing some fixes soon.

I want to give some special acknowledgment to Owen Malicsi who has taken a lot of ownership over Gtk4 porting. Owen started contributing to elementary to improve his development skillset in preparation for college, and he's done an amazing job both in successfully porting components to Gtk 4 as well as identifying blockers and creating discussions around refactoring for Gtk 4 paradigms. I'm super proud of his growth and contribution and we wish him well in his studies! Thanks Owen!

## Responsive Design

I'd like to touch on this subject in depth in a future post, but for now I want to mention that something we've been working on lately is moving towards more [responsive interfaces in our apps](https://github.com/orgs/elementary/projects/109/views/1). This means both for small displays—potentially down to phone size—and large displays. In particular, AppCenter has had quite a lot of work put into reducing its minimum window width as well as improving the way screen space is used when maximized on large desktop displays. System Settings is another area that we've been chipping away at as part of Gtk4 porting. I'm really excited to show off more of the way our design language is adapting in this space, so look forward to more detail here in the future!

---

That's all for now, folks. Thanks again for your understanding this month and we'll see you in the next one!
