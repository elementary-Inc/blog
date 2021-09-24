---
title: elementary OS 6 Updates for September, 2021
description: Big updates to AppCenter
author: cassidyjames
image: /images/os-6-updates-for-august-2021/card.png
tags:
  - odin
  - updates


---

We're back with your report on the monthly updates to elementary OS 6! It was another incredibly eventful month as we continued fixing reported issues and focused in especially on AppCenter and Mail. But before we get to all the goodies, we're proud to report that OS 6 has been downloaded from our website [over 122,000 times](https://plausible.io/elementary.io?period=custom&goal=Download&from=2021-08-10&to=2021-09-24&props=%7B%22Version%22%3A%226%22%7D)—and as always, that's not including downloads from third parties or direct downloads via torrent that bypass our download page.

## AppCenter

Over the past month, we've been improving AppCenter from the inside out. Our shift from Debian packages to Flatpak for both curated and non-curated apps means we're able to lean more on Flatpak features; in addition to continued code cleaning and improvements, we've been using this as an opportunity to make AppCenter much more engaging and informative right from the start.

For example, we've largely reworked the home page with banners featuring the most recently released and updated curated apps in a multi-touch swipable carousel. We've also added up to twelve more of the most recently-updated apps directly below. Rather than just showing the app's icon and name, we now also show each app's summary and an install button—including the developer's recommended price if it's a monetized app. Since we enforce accurate update information for curated apps, this data is populated locally from the apps' AppStream data rather than from a remote API as before. The result of this work is a faster home page with over three times the apps displayed, as well as the ability to purchase or install several apps with far fewer clicks. The categories remain below if you prefer that route for browsing.

We've also spent some significant time improving individual apps' info pages. Rather than displaying a generic "explicit" warning when installing an app with certain content warnings, we show this information ahead of time at the top of the app's info page. We now differentiate between and inform about several content warnings including things like violence, language, and nudity as well as privacy-related topics like online interactions and information collection. And since we validate this information for curated apps but can't make any guarantees about non-curated apps, we also more clearly inform ahead of time when an app is not curated with an additional badge. This new section works like a sort of content and privacy report card users can use to learn more about apps and make informed choices while also reducing the road blocks to installing the apps you want..

Some improvements permeate throughout AppCenter: fallback colors for apps that don't provide their own brand colors—including non-curated apps—now get a pleasant and more subtle look based on your selected system-wide accent color

HumbleButton/StripeDialog

Fallback color

AppInfoPages
- Show content warnings on app info pages
- Show other apps by an author for Flatpak sources
- Replaced Explicit dialog

Downstreams

In addition, app developers have continued releasing their apps on [AppCenter for elementary OS 6](https://appcenter.elementary.io)—and several more are in the queue being reviewed. We're also happy to report that developers have been pushing out updates to existing apps with new features and bug fixes, as they're in control of their own update schedule. Third-party apps on elementary OS continue to get better with time.

## Mail

Marco

## Other Fixes & Updates

- Fixed a crash in the Network settings for some hardware

And as always, there are translation updates, code cleanups, and other under-the-hood improvements included with these updates across the OS and apps.

<aside markdown="1">
>You can send your feedback to the team using the Feedback utility on elementary OS 6
</aside>

If you're experiencing an issue that wasn't fixed in this month's updates—or if you have an idea for a new feature—we'd love to hear from you. You can send your feedback on elementary OS 6 by searching for "Feedback" in the Applications Menu or by navigating to _System Settings_ → _System_ and selecting "Send Feedback" at the bottom of the window. Alternatively, you can file an issue report or start a discussion on the appropriate repository on [our GitHub organization](https://github.com/elementary). We prioritize our work based directly off of the feedback we receive through the Feedback utility and GitHub, so those are the best ways to make sure your voice is heard.

If you'd like to follow along with development and see what we're working on and prioritizing for the next monthly updates, check out the [OS 6.1 project board on GitHub](https://github.com/orgs/elementary/projects/90).

## Get These Updates

As always, if you're running elementary OS 6 you can get all of these updates directly from AppCenter by opening up the "Installed" tab and selecting "Update All", and previous purchase links from your email receipt will be upgraded to the newest version.

If you're not yet running OS 6, we've published a new 6.0.1 download for a pay-what-you-can price that includes all of these updates [on our homepage](https://elementary.io).

## Special Thanks

I'd like to give special thanks this month to Marco for his work on Online Accounts and associated apps. You can read more [on his blog](https://www.marco.betschart.name/blog/2021-08-30-elementary-os-6-post-release-bugfixing) about the specific fixes and features that he worked on as well as a link to his [GitHub Sponsors page](https://github.com/sponsors/marbetschar). He's currently looking to expand his Open Source software work and could really use your help with funding!

David also deserves a shoutout for diving into the big under-the-hood issues and delivering this month's big AppCenter and Flatpak-related fixes as well tracking down the source of issues related to suspend and resume. You can also [sponsor his work on GitHub](https://github.com/sponsors/davidmhewitt).

You can thank Marius for his work on hostnames, fixing the "Open" button in AppCenter, and many other bug fixes! Check out his [GitHub sponsors page](https://github.com/sponsors/meisenzahl) too.
