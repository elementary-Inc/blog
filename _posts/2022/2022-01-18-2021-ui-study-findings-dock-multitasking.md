---
title: 2021 UI Study Findings
description: Digging into the dock, multitasking, and more
author: cassidyjames
tags:
  - ui-study
  - ux
  - evergreen
---

Over the past couple of months we've conducted a user interface study to dig into how people multi-task on elementary OS as well as other desktop and tablet operating systems. In particular, we were interested in better learning how people use the dock, app launchers, and window management.

As we continue to iterate on the core experience of elementary OS, we are also aware of newer technologies like Wayland that we're actively adopting to improve privacy, security, and performance—but doing so requires reworking some components like the dock and window manager to use new protocols and APIs. As long as we're reworking some of these technical bits, it could be advantageous to rethink and improve upon the experience itself—plus, we can ensure we're not writing new code to support legacy designs just because that's how things worked in the past.

If that all sounds a bit ambitious… it kind of is! However, we've preciously worked on a [similar study](/user-interface-study-findings) around theming, dark styles, and night light modes that directly resulted in our implementation of a system-wide dark style as well as accent colors in elementary OS—and [our advocacy in that realm](/the-need-for-a-freedesktop-dark-style-preference) helped influence [GNOME's adoption of a cross-desktop dark style](https://blogs.gnome.org/alexm/2021/10/04/dark-style-preference/) that will work on both GNOME and elementary OS. That work has been years in the making, but the pay-off is well worth it.

At this point in the study, we have our raw data and have started digging into it to identify patterns and set priorities. Much like with the dark style study, the effects of this study may take some time to pan out, but I wanted to share our initial findings to kick the work off.

## Questions & Raw Stats

The study was conducted as a web survey posted to social media and open source forums from December, 2021 through January, 2022. The following questions were presented in these sections and this order:

### App launching & search

>e.g. the Applications Menu on elementary OS, Launchpad on macOS, Start menu on Windows, etc.

This section had 2,843 responses.

>**How often do you click/tap on an app in an app launcher to open your frequently-used apps?**
>
>Excluding using search, e.g. clicking an app icon in the Applications Menu on elementary OS, Launchpad on macOS, Start menu on Windows, etc.
>
> - Never
> - Infrequently (less than weekly)
> - Frequently (approximately weekly)
> - Daily (multiple times per week)

Of the respondents, 10% responded that they _never_ click or tap on an app in an app launcher to open frequently-used apps. 25% responded _infrequently_, 22% responded _frequently_, and the largest group at 43% responded _daily_. With some simple grouping, we can look at the results in another way:

- Over 90% of respondents click/tap on an app in an app launcher to open their frequently-used apps _at least sometimes_.

- Around 65% of respondents frequently or daily click/tap on an app in an app launcher to open their frequently-used apps, while around 35% do so infrequently or not at all.

<!-- TODO: split by traditionally mobile vs. desktop OSes -->

>**How often do you use search to open your frequently-used apps?**
>
>e.g. searching by name or function in the Applications Menu on elementary OS, Spotlight on macOS, search on Windows, etc.
>
> - Never
> - Infrequently (less than weekly)
> - Frequently (approximately weekly)
> - Daily (multiple times per week)

5% responded _never_, 13% responded _infrequently_, 18% responded _frequently_, and a clear majority at 64% responded _daily_. Similar to above, we can reframe this a bit:

- Around 95% of respondents use search to open their frequently-used apps _at least sometimes_.

- Around 82% of respondents frequently or daily use search to open their frequently-used apps, while around 18% do so infrequently or not at all.

<!-- TODO: split by traditionally mobile vs. desktop OSes -->

We also asked, "Anything else to share about how you launch apps and search?", and we've been digging through these free-form responses.

### Dock or taskbar

>e.g. the dock on elementary OS or macOS, the taskbar on Windows, a panel, etc.

This first question was used as a filter for the following questions; people who responded "yes" received the follow-up dock-related questions, while anyone who responded "no" or "not sure" skipped the rest of the section.

>**Do you use a dock or taskbar?**
>
>e.g. searching by name or function in the Applications Menu on elementary OS, Spotlight on macOS, search on Windows, etc.
>
> - Yes
> - No
> - Not sure

86% responded _yes_, 13% responded _no_, and 2% responded _not sure_. As a result, the following questions in this section received 2,431 responses.

>**How often do you use a dock or taskbar to open your frequently-used apps?**
>
> - Never
> - Infrequently (less than weekly)
> - Frequently (approximately weekly)
> - Daily (multiple times per week)

Of those who use a dock or taskbar, 3% responded they _never_ use it to open their frequently-used apps, 5% responded _infrequently_, 14% responded _frequently_, while the largest group at 79% responded _daily_.

>**Do you remove or replace the default items on the dock or taskbar?**
>
> - None
> - A few (less than half)
> - Most (half or more)
> - All

2% responded they remove or replace none of default items on the dock or taskbar. 21% responded they remove or replace _a few_ (less than half), 58% responded they remove or replace _most_ (half or more), and 19% responded they remove or replace _all_ the default items.

>**Do you add or pin apps you use frequently to the dock or taskbar?**
>
>- Yes
>- No

93% responded _yes_, while 7% responded _no_.

These questions lead me to initially believe customization of the dock is important or heavily-used by users, and the vast majority of dock or taskbar users do use it to launch their most common apps. It could also mean that the default apps aren't as useful to users, though it's important to remember that the default items also serve as a way to advertise/expose what apps are available on the system—and clearly users aren't hitting substantial issues in replacing them if they want.

## What's Next

We've started using this data to plan for our new Wayland-compatible dock; more on that effort soon!

_Wording and self-reporting from the user interface study might affect results, and I don’t pretend that this sample speaks for the entirety of FreeDesktop users. However, it’s a useful dataset of 2,843 responses that can help identify larger patterns. Percentages from the study are rounded to the nearest percent, so you may see things adding up to 101% or similar if there are half-percents involved._
