---
title: Let's Talk OS 8
description: Development on the next major version of elementary OS has begun
author: danrabbit
image: /images/lets-talk-os-8/card.png

tags:
  - early-access
---

One month ago today [we released elementary OS 7.1](https://blog.elementary.io/os-7-1-available-now/) which provides new personalization options that make it more inclusive and accessible, protects your privacy and ensures apps always operate with your explicit consent, and addresses your feedback with over 200 bug fixes, design changes, and new features. This point release concludes our feature focus on the OS 7 series and development focus has now shifted to OS 8! Let's take a look at what that means and the progress we've made in the last month.

## What happens to OS 7?

Folks running elementary OS 7 should expect fewer updates from this point forward. We do our best to continue to provide bug fix updates for as long as is reasonable—which sometimes extends into the lifecycle of the next major series—but the OS 7 series should largely be considered complete. There are a number of large architectural changes and transitions expected for the OS 8 series which means that some components will not be able to be backported to OS 7. All apps provided as Flatpak packages however will continue to receive updates indefinitely. That means all AppCenter apps, sideloaded Flatpak apps, and a decent portion of pre-installed apps—Calculator, Camera, the Captive Network Assistant, Videos, Music, Screenshot, GNOME Web, Document Viewer, and Archive Manager—will all continue to receive both bug fix and feature updates effectively forever. And since we build elementary OS from the Ubuntu Long Term Support repositories, you'll continue to receive security and bug fix updates from Canonical until 2027. So while OS 7 is no longer our development focus, you can still expect regular maintenance for quite some time!

## OS 8’s Roadmap &amp; Predicted Release Date

If you're familiar with the development cycle of elementary OS, you will know that **we don't predict release dates** ahead of time and instead opt to release a new version of elementary OS when we feel it is ready. This next major version of elementary OS is being built from the Ubuntu 24.04 repositories which means that at the earliest OS 8 won't be released until at least April of 2024, but historically it takes several months of additional work before a major new series is ready to debut. We have a number of very ambitious goals for OS 8, so while my hope is that we can complete this work in the next 6 months, the focus will always be on releasing when it's ready.

We have a [release planning project on GitHub](https://github.com/orgs/elementary/projects/128/views/1) which you can use to follow along with the status of development. This project contains the list of goals targeted for OS 8 as well as our progress on completing those goals. At the moment, we're deep in the planning phase which means this project board is very messy and has some very broad draft items on it. Over time we'll refine this down to very granular action items and some of the proposals on this list may not make it into the initial release. But the most important thing to know is that OS 8 won't be released until this project board is cleared. So you can use this board to get a picture of how close or far we are away from releasing.

## The Idea Phase

Since we're at the very start of the development cycle, this is the perfect time for you to get involved and share your vision for the next major version of elementary OS! We have a GitHub Discussions section where [you can submit your proposals at any time](https://github.com/orgs/elementary/discussions/categories/ideas), as well as see and vote on the ideas that others have proposed. This is a great way to communicate to the team what you feel is most important. We have our own ideas of the things we'd like to accomplish, but we love hearing directly from you!

## Wayland

One the largest and most ambitious goals we have for OS 8 is to use the Wayland display server protocol by default. This is a transition that we have been planning and working towards for several years and we're finally in the home stretch. Folks in our [Early Access](https://builds.elementary.io/downloads) program know that we have an experimental Wayland session of Pantheon available to test right now. We're currently tracking issues related to completing the Wayland transition in [this GitHub project](https://github.com/orgs/elementary/projects/118). Wayland will bring us improved performance, better app security, and opens the doors to support more complex display setups like mixed DPI multi-monitor setups.

As part of the Wayland transition, Pantheon needs a new Dock. Plank was written in a time long before many modern APIs and depends on a window matching library that is both incompatible with Wayland's security model and has proved to be increasingly inaccurate with some sandboxed apps. In both design and implementation we need a new solution. You may remember that we [conducted a survey in 2021](https://blog.elementary.io/2021-ui-study-results-dock-multitasking/) which resulted in [this project board](https://github.com/orgs/elementary/projects/99/views/1) and I'm happy to report that some initial work on the new Dock has begun [here](https://github.com/elementary/dock), including a new wayland-compatible window matching API that talks directly to Gala. There's also a Discussion post about the new Dock [here](https://github.com/orgs/elementary/discussions/337) if you'd like to share your ideas.

## GTK 4

You may be aware that we started our GTK 4 transition as part of the OS 7 development cycle and are currently shipping several GTK 4 components and apps. This transition continues into the OS 8 cycle where we're already planning to land or have landed several more ports. The Captive Network Assistant, Initial Setup, and Videos have all landed GTK 4 ports in their development main branch. The port for AppCenter is near completion, and ports for several other apps and components are in progress. Notably, System Settings has just over half of its panes ported to GTK 4 in its development main branch. We're [tracking GTK 4 porting in GitHub here](https://github.com/orgs/elementary/projects/95) so you can follow along with our progress.

The transition to GTK 4 has required some pretty major rewrites in some components and ties in heavily with making things Wayland-ready. Along the way we've been modernizing code that has existed in Pantheon for the past decade, adopting the latest code style, development patterns, and libraries, fixing old bugs, improving performance, and resolving accessibility issues. We've also implemented more responsive design patterns that work on large and small displays, as well as addressing UX concerns, and improving multitouch gesture support. So you can expect a vastly improved Pantheon in every area as part of our transition to GTK 4.

## Settings

As part of our work on [Responsive Design](https://github.com/orgs/elementary/projects/109), System Settings will need some major design changes. There are some prototypes for modernizing its design and navigation but the number of views here makes this a very challenging project. We've made a lot of progress but there's still quite some ways to go for System Settings to be usable on something like a phone.

Likewise, the design of the indicator area has remained largely the same since OS 0.4 which was released in 2016. In recent years every mainstream operating system has adopted a Quick Settings menu design which lends itself much better to responsive contexts as well. There's quite a bit more background and prior art in [this discussion post](https://github.com/elementary/wingpanel/discussions/446), and we have some very early development work towards a Quick Settings menu design for Pantheon [here](https://github.com/elementary/quick-settings). This is a project that I will caveat may be too ambitious to complete before the release of OS 8, but thanks to the modular nature of our Panel, it might be possible to have something of a transition period. We'll have to see how development evolves!

## And More

These are just some of the big picture ideas and most visible and ambitious projects that we're pursuing and the ones which we've taken concrete steps towards. There are other things that we're experimenting with, like the possibility of an immutable OS, and there are more mundane things that will certainly happen like shipping Pipewire. You'll also see on the project board that we're looking to replace the onscreen keyboard and it's time to re-evaluate some things like SystemD Boot. You can expect lots more little features to be detailed over the coming months. What I hope is clear is that we're looking at some of the largest changes to the design of Pantheon and its underlying architecture in quite some years for OS 8.

## Funding

Of course to make this and more happen we need to talk about funding! elementary is a super tiny software company that currently only has one full-time employee. Like many tech companies right now, sales have been a bit of a struggle and we've been working on tightening up our budget. One of the biggest ways you can help is by purchasing a copy of elementary OS or [sponsoring us on GitHub](https://github.com/sponsors/elementary). We use these funds to hire contractors and sponsor our community members as well as for purchasing hardware for testing and enablement. So if you're particularly interested in running elementary OS on ARM or tablet devices or with things like pen input, having a hardware budget is a great help. We also need funds to be able to attend major developer summits like GUADEC so that we can continue to collaborate effectively with the larger FreeDesktop ecosystem. And with enough funding it would be great to expand our full-time development team.

## Get Experimental Builds Now

[Sponsors on GitHub](https://github.com/sponsors/elementary) can download the latest daily builds of elementary OS and experimental builds for platforms like Raspberry Pi and Pinebook Pro. This is the best way to support our development and follow along yourself. And very early builds of OS 8 built from Ubuntu 24.04 repositories are available to download in Early Access right now! They aren't currently usable, but they will be soonish. Hang tight for more updates there. I think we're moving quite quickly as Launchpad builds for Ubuntu Noble only became available last week!

<div style="text-align: center" markdown="1">
[Get Early Access][Early Access]{: .button.suggested }
</div>

[Early Access]: https://builds.elementary.io
