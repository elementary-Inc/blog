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
>- Never
>- Infrequently (less than weekly)
>- Frequently (approximately weekly)
>- Daily (multiple times per week)

Of the respondents, 10% responded that they _never_ click or tap on an app in an app launcher to open frequently-used apps. 25% responded _infrequently_, 22% responded _frequently_, and the largest group at 43% responded _daily_. With some simple grouping, we can look at the results in another way:

- Over 90% of respondents click/tap on an app in an app launcher to open their frequently-used apps _at least sometimes_.

- Around 65% of respondents frequently or daily click/tap on an app in an app launcher to open their frequently-used apps, while around 35% do so infrequently or not at all.

<!-- TODO: split by traditionally mobile vs. desktop OSes -->

>**How often do you use search to open your frequently-used apps?**
>
>e.g. searching by name or function in the Applications Menu on elementary OS, Spotlight on macOS, search on Windows, etc.
>
>- Never
>- Infrequently (less than weekly)
>- Frequently (approximately weekly)
>- Daily (multiple times per week)

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
>- Yes
>- No
>- Not sure

86% responded _yes_, 13% responded _no_, and 2% responded _not sure_. As a result, the following questions in this section received 2,431 responses.

>**How often do you use a dock or taskbar to open your frequently-used apps?**
>
>- Never
>- Infrequently (less than weekly)
>- Frequently (approximately weekly)
>- Daily (multiple times per week)

Of those who use a dock or taskbar, 3% responded they _never_ use it to open their frequently-used apps, 5% responded _infrequently_, 14% responded _frequently_, while the largest group at 79% responded _daily_.

>**Do you remove or replace the default items on the dock or taskbar?**
>
>- None
>- A few (less than half)
>- Most (half or more)
>- All

2% responded they remove or replace none of default items on the dock or taskbar. 21% responded they remove or replace _a few_ (less than half), 58% responded they remove or replace _most_ (half or more), and 19% responded they remove or replace _all_ the default items.

>**Do you add or pin apps you use frequently to the dock or taskbar?**
>
>- Yes
>- No

93% responded _yes_, while 7% responded _no_.

These questions lead me to initially believe customization of the dock is important and heavily-used by users, and the vast majority of dock or taskbar users do use it to launch their most common apps—which makes a lot of sense! It _could_ also mean that the default apps on the dock aren't as useful to users, though it's important to remember that the default items also serve as a way to advertise/expose what apps are available on the system—and clearly based on these responses, users aren't hitting substantial issues in replacing them if they want.

<!-- TODO: look at elementary OS stats specifically -->

### Files and folders

Next, we dug into files and folders—especially as they relate to the dock. This section was a select-all-that-apply and had 2,843 responses.

>**How do you typically open files and folders?**
>
>- OS-wide search
>- File manager app (e.g. Files on elementary OS, Finder on macOS, Explorer on Windows, etc.)
>- Taskbar or dock (e.g. pinned files or shortcuts)
>- From inside apps (e.g. opening a document from inside a word processor app)
>- Files and folders are kept on the desktop'
>- _Other…_ (free-form response)

96% responded _file manager app_, 43% responded _OS-wide search_, 15% responded _taskbar or dock_, 13% responded _desktop_. Of the _other_ responses, many were clarifications about the choices, but we have been able to collate the most popular being 7% of responses mentioning some form of terminal or CLI. 4% answered _other_ without expanding on the answer.

<!-- TODO: look at elementary OS stats specifically -->

### Multitasking

This section gets into how respondents multi-task, e.g. switch between apps and windows. Our interest here is specifically to understand how the dock fits into multitasking and window management, but we didn't want to lead responses in one direction or another. This section was select-all-that-apply and had 2,843 responses.

>**How do you usually tell which apps are currently open in the background?**
>
>- Dock or taskbar
>- Alt+tab or window switching
>- Multitasking view (e.g. Multitasking View on elementary OS, Mission Control on macOS, Task View on Windows, Activities view on GNOME, etc.)
>- _Other…_ (free-form response)

69% responded _dock or taskbar_, 41% responded _alt+tab or window switching_, 59% responded _multitasking view_. 2% answered _other_ without expanding on the answer.

<!-- TODO: collate "other", look at elementary-specific responses -->

>**How do you usually switch between open apps?**
>
>- Dock or taskbar
>- Alt+tab or window switching
>- Multitasking view (e.g. Multitasking View on elementary OS, Mission Control on macOS, Task View on Windows, Activities view on GNOME, etc.)
>- _Other…_ (free-form response)

53% responded _dock or taskbar_, 73% responded _alt+tab or window switching_, 52% responded _multitasking view_.

<!-- TODO: collate "other" responses -->

>**How do you usually switch between open windows of the same app?**
>
>- Dock or taskbar
>- Alt+tab or window switching
>- Multitasking view (e.g. Multitasking View on elementary OS, Mission Control on macOS, Task View on Windows, Activities view on GNOME, etc.)
>- _Other…_ (free-form response)

43% responded _dock or taskbar_, 62% responded _alt+tab or window switching_, 45% responded _multitasking view_. 4% answered _other_ without expanding on the answer.

<!-- TODO: collate "other" responses -->

We also asked, "Anything else to share about how you use multitasking?", and we've been digging through these free-form responses. Some of the highlights for me have been mentions of multiple displays, tiling, and multi-touch gestures.

### Closing apps

We wanted to be sure to cover how the dock is used for closing apps, but didn't want to ask leading questions; as such, we asked how people typically close apps and included the dock as one of many options. This section was select-all-that-apply and had 2,843 responses.

>**How do you usually close apps that are open?**
>
>- Closing with a button in the app/on its titlebar
>- Using a context menu on the dock/taskbar
>- Keyboard shortcuts (e.g. Ctrl+Q or Alt+F4)
>- From a multitasking view (e.g. Multitasking View on elementary OS, Mission Control on macOS, Task View on Windows, Activities view on GNOME, etc.)
>- _Other…_ (free-form response)

85% responded _a button in the app/on its titlebar_, 23% responded _context menu on the dock/taskbar_, 62% responded _keyboard shortcuts_, 29% responded _multitasking view_. 1% responded _other_ without expanding on the answer.

### App actions

>To jump to a specific section or function of an app \*without opening the app first.\* For example, "New Incognito Window" for a web browser or "Compose Message" for an email client.

As above, we wanted to be sure to cover how the dock specifically is used for app actions, but didn't want to ask leading questions. This first question was used as a filter for the following questions; people who responded "yes" received the follow-up actions-related questions, while anyone who responded "no" or "not sure" skipped the rest of the section.

>**Do you use app actions or shortcuts?**
>
>e.g. searching by name or function in the Applications Menu on elementary OS, Spotlight on macOS, search on Windows, etc.
>
>- Yes
>- No
>- Not sure

54% responded _yes_, 34% responded _no_, and 13% responded _not sure_. As a result, the following questions in this section received 1,595 responses.

<aside markdown="1">
**Note**: when the study first launched, the logic for skipping the next questions was not working correctly; as such, we received a lot of "N/A" type responses for the next question. The issue was corrected after 136 responses and I don't believe it largely affected the results, but wanted to share for transparency.
</aside>

>**How do you usually use app actions?**
>
>- Search (e.g. searching for actions by name in an app launcher)
>- Context menu in app launcher (e.g. right-clicking or long-pressing an app icon in the Applications Menu, Start menu, etc.)
>- Context menu on dock (e.g. right-clicking or long-pressing an app icon on the dock or taskbar)
>- _Other…_ (free-form response)

41% responded _search_, 53% responded _context menu in app launcher_, 66% responded _context menu on dock_.

We also asked, "Anything else to share about how you use app actions?", and we've been digging through these free-form responses. Some highlights were about them being more used on mobile OSes, that they wish more apps supported them, that they forget this is a feature, and how they work on other OSes.

### Glanceable information

These questions were again to look at how the dock is used, but were written to be non-leading and to include the dock as one of multiple options. Unlike previous questions, these were also select any that apply _without_ a free-form "other" option.

>**Where do you look to check the status of long running tasks?**
>
>e.g. the progress of a download
>
>- Notifications
>- Progress bar on the app's dock/taskbar icon
>- In the app window itself

45% responded _notifications_, 60% responded _progress bar_, and 74% responded _in the app window_. Less than 1% skipped the question.

<!-- TODO: really want to separate out mobile vs desktop users here -->

>**Where do you look to see items that need action in an app?**
>
>e.g. outstanding tasks, or new messages
>
>- Notifications
>- Badge on the app's dock/taskbar icon
>- In the app window itself

67% responded _notifications_, 59% responded _badge_, and 60% responded _in the app window_. Less than 1% skipped the question.

<!-- TODO: really want to separate out mobile vs desktop users here -->

### Anything else?

Lastly, we asked "Anything else to share about the topics of this study?" and asked if we may send follow-up questions or future UI studies to the email address provided.

## What's Next

We've started using this data to plan for our new Wayland-compatible dock; more on that effort soon!

_Wording and self-reporting from the user interface study might affect results, and I don’t pretend that this sample speaks for the entirety of FreeDesktop users. However, it’s a useful dataset of 2,843 responses that can help identify larger patterns. Percentages from the study are rounded to the nearest percent, so you may see things adding up to 101% or similar if there are half-percents involved._

