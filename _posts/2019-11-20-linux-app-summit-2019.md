---
title: Linux App Summit 2019
description: Talking apps and platforms in Barcelona, Spain
author: cassidyjames

tags:
  - event
  - flatpak
  - gnome
  - gtk
  - las

sponsor:
  name: System76
  link: https://s76.co/ElementarySponsorship
  image: /images/sponsors/system76.png
  image-2x: /images/sponsors/system76@2x.png
  hook: "If you're looking for a new Linux laptop, desktop, or server, head their way!"
---

Earlier this month we attended the third-annual LAS with folks from across open source desktop ecosystems including GNOME, KDE, Flatpak, Snap, and companies like CodeThink, Red Hat, Canonical, Purism, Endless, Pine64, and more. For the first two years, the summit was called the "Libre Application Summit," but the organizing committee slightly rebranded as the "Linux App Summit" this year.

Name aside, the summit has doubled in size each year and is becomming a real force in cross-desktop collaboration and community. We [attended last year]({% post_url 2018-09-11-were-back-from-libre-application-summit-2018 %}) in Denver, Colorado, and this year it definitely felt like even more projects, companies, and platforms were well represented. We look forward to continuing to be involved in the years to come.

The summit was organized into three days of talks, a panel, and one day of BoFs (Birds of a Feather sessions).

## Our Talks

Daniel and I each gave a talk this year, bringing our insights and perspectives from helping to build elementary OS and our AppCenter app ecosystem.

### Growing Beyond the System Tray

Daniel presented a bit of history behind the concept of a "System Tray," why it has been problematic for platforms and users, and the better APIs that have replaced it for a better user experience without removing functionality.

{% include youtube.html v='fPFdV-Z69Lo' %}

Dan has also contributed to [islinuxabout.xyz/systray](https://islinuxabout.xyz/systray/) which takes a look at the APIs that exist for better integration across desktops.

### Curb Cuts

Curb cuts—the slopes on sidewalks designed to make traversal with a wheelchair possible—improve the experience for everyone, regardless of any specific ability or impairment. Similarly, digital accessibility features should be ubiquitous and well-supported.

In this talk I share how some "accessibility" features have become ubiquitous on other platforms, and how to keep the needs of your users in mind when creating apps and platforms.

{% include youtube.html v='YQBuFm4gx7s' %}

We've also been tracking this effort across elementary OS in an [organization-wide GitHub Project](https://github.com/orgs/elementary/projects/35) so you can follow along!

## More Talks

There were a ton of great talks this year from a variety of perspectives. Below are the talks we were able to attend, but be sure to check out the [LAS YouTube channel](https://www.youtube.com/channel/UCjSsbz2TDxIxBEarbDzNQ4w) for recordings of even more talks.

### The Economics of FOSS

### Distributing Freedesktop SDK applications to Flatpak and Snapd

### Why can't we all be friends?

### Ubuntu Kylin Practice on Application Construction for Linux Ecosystem

### Are we missing something?

### Desktop Services as Flatpak

### How Linux World Can Benefit from Product Managers?

### Building an App Store with Flathub

### How to 10x grow the number of Linux Desktop Apps

### How I Squeezed GNOME Into Your Pocket

### There is no "Linux" Platform

### Humanspeak

### Portals: Priciples & Practice

### The Year of the Virtual Linux Desktop

### Bad Language

### Maintaining a Flatpak Repository

## Panel: The Future of Linux Apps

## BoFs

Overall, the Birds of a Feather sessions felt a little lightweight this year, and we'd love to see even more cross-desktop collaboration here in the future. Perhaps we were all very tired from the previous night's social event.

### Organizing & Engagement

We did attend the LAS Organizing BoF, as elementary is interested in getting more involved in LAS next year. We had a retrospective look at what went well and what could be improved, then talked a bit about potential locations. Afterwards, that BoF split/morphed into two smaller groups, the LAS Engagement BoF and the GNOME Engagement BoF.

### Flatpak Payments

Earlier in the week we also had an impromptu BoF focused around Flatpak and supporting payments. We've supported pay-what-you-want app purchases in AppCenter with our current infrastructure, but Flathub and other parties would also like the ability to let app developers ethically monetize their software. We discussed the current work targeting the 1.6 release of Flatpak, which is a generic OAuth-like token system for Flatpak that can be backed by anything like a payment system, a limited beta system, or existing enrollment systems. We discussed what the API for clients would look like, and ensured it would serve the native integration required for elementary OS as well as a web-based integration that would be required for Flathub using different authenticators.

---

<figure markdown="1">
![Sponsored by GNOME Foundation]({{ site.baseurl }}/images/elementary-at-guadec-2019/sponsored.png)
</figure>

We were able to attend this summit thanks in part to [The GNOME Foundation](https://www.gnome.org/foundation/) who partially sponsored our travel.
