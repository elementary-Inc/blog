---
title: elementary at GUADEC 2019
description: Hanging out with GNOMIES in Thessaloniki, Greece
author: cassidyjames
image: https://pixelfed.social/storage/m/375e65040b19b04b60a3cf824105a89aedf089df/cd4923591853d189595583ebde7866fc60062337/mkWPZ4yvtooKq2pS1xtL6h5YawWZax9G2393zSlM.jpeg
tags:
  - event
  - flatpak
  - gnome
  - gtk
  - guadec
thanks: true
---

<figure markdown="1">
![The Aegean Sea seen from Thessaloniki](https://pixelfed.social/storage/m/375e65040b19b04b60a3cf824105a89aedf089df/cd4923591853d189595583ebde7866fc60062337/mkWPZ4yvtooKq2pS1xtL6h5YawWZax9G2393zSlM.jpeg)
<figcaption>Sunset in Thessaloniki over the Aegean Sea</figcaption>
</figure>

GUADEC is the annual **G**NOME **U**ser **A**nd **D**eveloper ~~**E**uropean~~* **C**onference where contributors to GNOME and its downstreams get together for a week of sharing their work from the past year, planning the future of their individual components, and catching up with one another. The conference is organized into two main halves: three days of talks, and three days of BoFs (with the last BoF day being more of a social day).

elementary [attended for the first time]({% post_url 2018-07-18-things-we-learned-at-guadec-2018 %}) in Almería, Spain last year and had such a productive (and fun!) time that we made sure to be back again for 2019. This year Corentin Noël and I represented elementary, while Daniel took some time off to [celebrate his one-year anniversary](https://twitter.com/DanielFore/status/1163831738532941824) (congrats, Dan!).

Just like last year, due to the nature of GUADEC, this post might get a bit technical and is mostly future-looking. For even more reports from a diverse group of GNOME contributors, check out the [Planet GNOME blog aggregator](https://planet.gnome.org/). That aside, let’s dive in.

_* No longer restricted to Europe! In fact, a bid is being submitted to host GUADEC 2020 in Mexico. I guess we can retcon the E to stand for "Everywhere."_

---

## Talks

Corentin and I split up for most of the talks for maximum coverage. As such, we attended a _lot_ of talks. We've embedded the recordings below as well, since they recorded and uploaded all of them already (which is _awesome_).

### Desktop Secrets Management for the Future

Red Hat and GNOME engineer Daiki Ueno shared future improvements to the "secrets" API that manages things like passwords and encryption keys in GNOME, elementary OS, and other desktops.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b148f7api9muax/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

He focused specifically on the implications of sandboxing with Flatpak, and how a new version of the API could be designed for this more secure future. Much of the content was above my level of knowledge, but it was encouraging to see some of the remaining questions around Flatpak being actively worked on, and this is work that will benefit elementary OS in the future.

### Managing GNOME Sessions with systemd

Red Hat engineer Benjamin Berg and Canonical engineer Iain Lane shared their work with moving much of the session management out of GNOME Session and into systemd.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b137f3bbcudhop/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

This is an area we've begun exploring in elementary OS, but it was good to hear about their experiences, some cool side-effects, and issues they had to overcome. This is ongoing work, and we'll be following it to see how it applies to elementary OS in the future as well.

### GNHOME AUTTOMQATION

No, my cat didn't walk across the keyboard while I was writing the name of this talk; Nathan Willis presented his thoughts around how the GNOME desktop could better support modern home automation (and "smart home") user flows.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b148d79qoix9bi/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

I _think_ the title is a pun based on "GNOME" and the names of some of the popular open source home automation tools in wide use today. It was an interesting talk that got my gears turning with regards to how the smartest devices in our homes (our computers) are sometimes the least integrated.

### Portals: Principles and Practice

Portals are how sandboxed apps communicate with one another or request specific access to things they wouldn't normally get, like user files, location services, screen sharing, etc. In this talk, Red Hat manager and GTK developer Matthias Clasen shared a deep dive into Flatpak Portals, their architecture, the user experience, and what he's learned in the past year since Flatpak 1.0. He also collected suggestions for Portals that don't yet exist.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b148f36jtj6us1/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

We've been [moving toward Portals]({% post_url 2019-03-12-a-new-native-file-chooser %}) in elementary OS in preparation for [using Flatpak]({% post_url 2019-04-01-elementary-appcenter-flatpak %}), and it was good to see the wide variety of portals that exist and the design considerations behind them. One portal we suggested based on our work toward [a cross-desktop settings API]({% post_url 2016-12-08-making-system-settings-access-a-cross-desktop-feature %}) was a “Connect to Network” portal; rather than a “System Settings” portal that would need to handle every possible setting an OS might have, we came to the conclusion that individual portals for specific actions would be more flexible. A new network connection portal could be used in elementary OS to prompt a user to get connected when browsing AppCenter, for example, where an Internet connection is needed to install apps. It could also be used in apps designed for any desktop environment, like a web browser, torrent client, chat app, etc.

### Wineglass: How to Make Wine Accessible

elementary OS user and app developer Alex Angelou gave this unconference talk (unplanned and decided day-of) about his app [Wineglass](https://appcenter.elementary.io/com.github.aggalex.wineglass/).

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ad7c8e6dabqw92/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

It was a brief introduction to Wine prefixes (used to sort of sandbox Wine apps from one another), and how Wineglass works to make it faster and simpler to use Wine. It was fun seeing elementary OS up on the big screen at a GNOME conference, and his app was generally well received. During the Q&A session there were also some great discussions and suggestions, with issues being filed before we left the room.

### GNU Health: The Fight for our Rights in the Public Health System

This was the first "keynote" talk, presented by Founder & President of GNU Solidario.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ad7835ayrnms3e/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

It focused on the unique challenges of the global healthcare system, and how GNU Health tries to address them. Over all it was an interesting case study in open source software entering and taking hold in a market dominated by proprietary solutions.

### Packing Up Boxes

Not about Flatpak, and not about GNOME Boxes. 😉️ GNOME Foundation engineer and core GTK developer Emmanuele Bassi shared how to use constraint-based layouts to build user interfaces in GTK4.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6dc9dhybbpfg/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

This is something app developers have been asking for for a while, so it's exciting to see it come to GTK. I'm super interested in playing with this in my own apps and in the elementary apps once the GTK4 porting work begins.

### Simple is Hard: Creating Beautiful App Icons

Red Hat and GNOME visual designer Jakub Steiner presented the new GNOME icon style and a quick demo of creating a new icon using the new Icon Preview app and Inkscape.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6c813prh3adv/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

Jakub is always fun to chat with, and his goofy personality shines through in this talk. Even if you're not interested in designing GNOME icons (since elementary OS uses a different icon style), this talk is entertaining to watch.

### GNOME UX: Strategies & Tactics

Red Hat and GNOME UX designer Allan Day shared a lot of the design work that is going into GNOME as well as his vision for the future of GNOME.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6dbd2x865wc3/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

This talk was _so good_ and really shows the product management role that Allan and the design team serve within GNOME. I feel like this has always been the case to some extent, but is more prominent more recently. This also echoes how elementary is really a design-led organization, and many of the "tactics" he shares to improve GNOME can apply to elementary as well.

Specifically, the bits about developer and designer synchronicity, designer-developers, and development-conscious design are areas that we champion within elementary; much of the work Daniel and I have done lately has centered around prototyping and developing directly in Vala and GTK, which means we're far less likely to design something that is impractical from a technical level. It also means we're able to jump into a codebase and improve the UI directly: we don't have to make a mockup and wait for a "real developer" to come along and pick up the work. This has been a _massive_ improvement to the process within elementary.

Something that has enabled that is that we do have a single preferred language and code style, which means we don't have to be fluent in C, Rust, Vala, JavaScript, Python, etc. Once we have solved a problem in one app, it's pretty generalizable across all elementary apps. Of course we still lean heavily on experienced developers, but we're able to do a lot more as designers than ever before.

### Maintaining a Flatpak Repository

Red Hat, GNOME, and Flatpak developer Alexander Larsson shared how Flatpak remotes work and how to host one yourself.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6dd77i05j8rh/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

He gets pretty technical into how Flatpak works on the server side with details on OSTree (like git for your filesystem), how diff-based updates work, etc. Overall it was a great talk and is super relevant to elementary since we'll be hosting our own Flatpak remote for AppCenter. If you're interested in helping elementary move to the Flatpak future, I highly recommend you watch it!

### GNOME Foundation Annual General Meeting

Part of GUADEC is the GNOME Foundation's annual meeting where they go over the last year and share projections for the next year. GNOME Foundation members also get to vote on relevant topics, such as changing the term lengths of board members, and changing wording in the bylaws.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6ddf7r559xos/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

It was also an opportunity for an in-person question-and-answer session with the GNOME Foundation board.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0ae6ca4e9nojzh3/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

### The Need for a FreeDesktop Dark Style Preference

This was my talk! If you've read [my blog post]({% post_url 2019-05-17-the-need-for-a-freedesktop-dark-style-preference %}) on the topic, it's mostly review. But it was well-received and as a result, GNOME and GTK are moving forward to support a system-wide dark style preference.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af56c87sex078k/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

### Is the Linux Desktop Really Dead?

Robert McQueen

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af6044fmc08q4k/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

### Accessibility Features for Mutter/GNOME Shell on Wayland

Red Hat and GNOME software engineer Oliver Fourdan presented ongoing work within Mutter and Wayland to enable the same level of accessibility support as X11.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b148681aw5mihz/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

While elementary OS doesn't use GNOME Shell (which was demoed in this talk), we should be able to use the same Mutter features within Gala and elementary OS to ensure we don't regress in accessibility when we inevitably move to Wayland.

### Designing GNOME Mobile Apps

Purism and GNOME designer Tobias Bernard shared much of the ongoing work to port GNOME to mobile devices like the upcoming Librem 5.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af53a1fipzbiat/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

While elementary OS has no plans to develop a mobile version of the OS, some of the design patterns and especially the widgets in LibHandy are of great interest; better touch support and better layouts for small and large window sizes are always welcome. As a result of this talk (and playing with LibHandy afterwards), we've filed several issues for including LibHandy in elementary OS and using it within the shell and apps.

### Usability Testing

Clarissa Lima Borges

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af588eeqnwoffd/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

### Product Metrics & Respecting Privacy

Robert McQueen

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af5a8ffz4hc0b7/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

### Lightning Talks

Lightning talks are fast-paced and unplanned talks that are decided day-of and given a strict, short time limit.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0b1484a2718m3hh/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

The highlights for me were Alexander Larsson's GThree (a 3D rendering library for GTK) and Richard Brown's How to Survive a Speaker Having a Heart Attack on Stage.

### Free Software/Utopia

The closing keynote presented by Deb Nicholson, Director of Community Operations at the Free Software Conservancy.

<figure class="embed">
  <iframe src="https://guadec.ubicast.tv/permalink/v125d0af5f72dycbpzkw/iframe/" allowfullscreen="allowfullscreen"></iframe>
</figure>

## BoFs

BoFs, or "Birds of a Feather" sessions, are meetups that happen across the venue with people who are working on or with certain technologies—or just interested in a common topic. For example, the GTK BoF was organized by core GTK contributors, but attended by GTK developers, folks writing GTK apps, GTK stylesheet authors, etc.

### GTK

Speaking of the GTK BoF, this was the big all-day one that took most of our time on the first day. Matthias directed the discussion and opened the floor for GLib wishlist items (like an OS info API), the status of GTK4, and even the Dark Style implementation.

A lot of time was spent discussing GTK4—primarily if there were any more "headlining" features we wanted to try to get into the release to help encourage app developers to port as soon as possible. We mostly agreed that the performance improvements were a large reason to port, and didn't come up with any single "big new feature" that should be added at this point. LibDazzle and Purism's LibHandy also demonstrate that you can still do a lot more with GTK3 than most apps do, so even getting much of those widgets upstreamed into GTK4 would not be compelling features in themselves.

We also talked about what is going to hold a lot of apps back from GTK4 to start: WebKitGtk. There is not currently a GTK4 port, meaning any app needing a web view will need to stay on GTK3 until that work is started and finished. That's a huge void that will take a lot of time and effort to accomplish, and as far as we know, nobody has taken it on yet.

Matthias has a great [dedicated blog post](https://blog.gtk.org/2019/08/29/gtk-bof-at-guadec/) on this BoF as well.

### Vendor Styles

I attended this BoF on the second day. Organized and moderated by Neil McGovern, Executive Director of the GNOME Foundation. It was all about moving forward with the sometimes at-conflict goals of GNOME apps looking as good as they can and downstream vendors (like Ubuntu or Pop!_OS) wanting to express their unique branding and styling. Rather than just sit in two separate camps, the idea was to talk it out and decide where we actually aligned, and how we could move forward to improve GNOME.

Over all, it went exceedingly well in my eyes. We came to a conclusion that GNOME _could_ support some amount of styling if it were well-defined and well documented—right now, the only real "documentation" is Adwaita's behavior itself. This definition and documentation work would also directly benefit apps as well, as they could use the documented styles to do more interesting custom styles that would be supported in Adwaita as well as any "compatible" stylesheets. This is actually pretty similar to elementary OS, where we have publicly-exported variables, the color palette, and Granite style classes for apps to do custom styling.

We agreed that there are really three areas when it comes to custom styling: the "supported" styles (currently nothing, but hopefully soon a handful of public variables, color palette, colored headerbars, etc.), "upstreamable" styles (i.e. something that a vendor or app wants to be supported but currently is not), and "here be dragons" which is everything else that's explicitly unsupported. But at least agreeing on the three areas, it means GNOME can work to increase the supported styling and downstreams can work on upstreaming, ultimately reducing the "dragons" area.

Interestingly, Yaru (the Ubuntu GTK stylesheet) is already based on Adwaita (the GNOME GTK stylesheet), using a build-time variable system that the Yaru developers put together. They even demoed a Pop!\_OS inspired set of variables that does express much of the same branding as the official Pop!\_OS stylesheet without much work. Some of this work may get upstreamed into Adwaita itself, and I've been sharing our experiences with publicly-exported variables in elementary OS to enable our unique features like per-app accent colors and branded headerbars.

I'm currently [helping lead this effort within GNOME](https://discourse.gnome.org/t/gtk-adwaita-and-vendor-styles/1641), and as this work continues, we'll try to share and upstream as much of our work from elementary OS as possible.

### Flatpak Donations/Store

Unfortunately I was unable to attend this BoF since the Vendor Styles BoF ended up taking the whole day. However, I chatted with Robert McQueen beforehand about how AppCenter works, and he debriefed me afterwards and shared some ongoing work within Flatpak to enable payments. It sounds like they are headed in the right direction, and I expect the work here to simplify some of our Flatpak work around payments.

## Social

As always, the social events were almost as important as the talks and BoFs; they provide a time and space to get to know folks, have fun, and chat about things—GNOME-related and otherwise—that don't have an official time and place in the schedule.

## Thank You

I'd like to give a **huge** thank you to the [GNOME Foundation](https://www.gnome.org/foundation/) for sponsoring my travel and lodging! I had an amazing time connecting and working with folks throughout the GNOME community—especially Allan Day, Clarissa Borges, Niel McGovern, Robert McQueen, Tobias Bernard, Adrien Plazas, Julian Sparber, Matthias Clasen, Britt Yazel, Alex Angelou, Cosimo Cecchi, Ian Santopietro, Benjamin Berg, and probably dozens of others I've missed.

<figure markdown="1">
![Sponsored by GNOME Foundation]({{ site.baseurl }}/images/elementary-at-guadec-2019/sponsored.png)
</figure>

As a member of the GNOME Foundation, I see my attending GNOME events as multi-purpose: First, I help represent elementary and ensure future GNOME-stack developments are generally compatible with our vision. Equally, I strive to bring my experiences, knowledge, and data collected from working on elementary OS to GNOME to help make GNOME itself better. Lastly, I learn more about the technologies we're using in elementary OS so we can go and build cool things with them. The fact that the GNOME Foundation sees so much value in this is validating, and I encourage anyone who works on GNOME or GNOME-related downstreams to [apply for Foundation membership](https://www.gnome.org/foundation/membership/)!

We would also like to thank everyone who’s bought an app on [AppCenter], our supporters on [Bountysource] and [Patreon], and those who’ve purchased a copy of [elementary OS] or merch from [our store]. Each contribution helps make what we do possible. If you’d like to help improve elementary OS, don’t hesitate to [get involved].

[AppCenter]: https://appcenter.elementary.io
[Bountysource]: https://salt.bountysource.com/teams/elementary
[Patreon]: https://www.patreon.com/elementary
[elementary OS]: https://elementary.io/
[our store]: https://elementary.io/store/
[get involved]: https://elementary.io/get-involved

