---
title: Happy Pride! Have Some Updates!
description: OS 7 Updates and OS 8 progress during May
author: danrabbit
image: /images/updates-for-june-2024/lock.png

tags:
  - earlyaccess
  - horus
  - updates
---

This month we have some surprise updates for OS 7, including new releases of GNOME apps and a big update for Mail. Plus Wayland is here, there's a new way to manage Drivers, and we're shipping Flathub by default! And don't forget Platform 8 is now ready for developers. Read ahead for all of the details of the work we accomplished during the month of May.

## Updated Flatpak apps for OS 7

Thanks to Flatpak, OS 7 continues to receive updates for several apps, including the GNOME apps that we ship with elementary OS. Web 46 brings a new flatter design and tons of bug fixes. Document Viewer gets the latest bug fixes while Archive Manager now uses GTK 4.

<figure markdown="1">
![The Fonts app](/images/{{ page.slug }}/fonts.png)
<figcaption markdown="1">
The updated Fonts app is available from AppCenter
</figcaption>
</figure>

Plus, Fonts is now available to install as a Flatpak from AppCenter. The new Fonts looks fantastic and has much better performance, and it will continue to receive updates just like our other apps shipped as Flatpak, so we highly recommend switching to it.

## Mail

Email aliases have arrived in Mail! You can now secondary click on an account in the sidebar and select "Edit Aliases…" to configure them. Plus Mail now also handles replying and forwarding to the correct address for senders who use aliases. And bugs related to certain emails blanking or certain attachments not downloading have been fixed. Shoutouts to [Leonhard](https://github.com/leolost2605) for his work here.

## Monthly Stable Builds

We're now automatically building monthly release candidate quality stable builds on our [Builds website](https://builds.elementary.io). These builds are created on the 1st of every month and include all stable updates for the current stable OS series. They have not been reviewed by a human, but should usually be of high quality. These monthly release candidates and daily unstable builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier!

---

## Wayland &amp; Dock

You can now choose between a Wayland or X11 session on the lock screen of the latest OS 8 Early Access builds via the gear menu on your login card. Thanks to the work of [Corentin](https://github.com/tintou) and [Leonhard](https://github.com/leolost2605), our window manager now contains fresh APIs for positioning panels and docks, including handling hide modes. Currently the new Dock is only positioned correctly in the Wayland session. Speaking of the Dock, you can now launch pinned apps with <kbd>Super</kbd> + <kbd>1­</kbd>—<kbd>9</kbd>, a hotly requested feature.

## System Settings

Continuing our big redesign of System Settings, a new paned design has landed for Desktop settings. This also includes wallpaper previews on the "Appearance" page. You'll notice that the "Dim Wallpaper With Dark Style" option has also moved to the Appearance page where you can see a preview of its effect.

<figure markdown="1">
![System Settings → Desktop → Appearance](/images/{{ page.slug }}/appearance.png)
<figcaption markdown="1">
Desktop settings have been redesigned
</figcaption>
</figure>

Another new feature from [Leonhard](https://github.com/leolost2605), Driver management has moved to System Settings → System. The new design for drivers should be more in line with how drivers are managed on other operating systems and be easier to work with. We're definitely looking forward to your feedback here to make sure we're providing a better experience for folks who rely on additional drivers.

<figure markdown="1">
![System Settings → System → Drivers](/images/{{ page.slug }}/drivers.png)
<figcaption markdown="1">
Drivers are now managed from System Settings
</figcaption>
</figure>

## AppCenter

Now that System Updates and Drivers have moved to System Settings, AppCenter has become Flatpak only! This greatly reduces code complexity and improves stability and performance. Plus it will make it easier for us to introduce new features in the future. And as a bonus, we're now shipping Flathub as an available Flatpak remote. This means you will be able to access both apps made for elementary OS and cross-platform apps for Linux out of the box.

## And More

The Lock Screen now features a larger and bolder clock and it looks really great with our new default wallpaper for OS 8!

<figure class="card" markdown="1">
![The new Lock Screen](/images/{{ page.slug }}/lock.png)
<figcaption markdown="1">
A larger and bolder clock on the Lock Screen
</figcaption>
</figure>

We have two new wallpapers to share, ["A Large Body of Water Surrounded By Mountains"](https://unsplash.com/photos/a-large-body-of-water-surrounded-by-mountains-Dxod5pdRtsk) by [Peter Thomas](https://unsplash.com/@lifeof_peter_) and ["A Trail of Footprints In The Sand"](https://unsplash.com/photos/a-trail-of-footprints-in-the-sand-of-a-beach-A9mr3TPoj0k) by [David Emrich](https://unsplash.com/@davidemrich). Both of these images have been slightly edited for use as wallpapers in elementary OS and are distributed under the permissive Unsplash license.

## Developer Platform

The elementary Flatpak Platform 8 has been released and is available now in the AppCenter Flatpak remote. If you're an app developer, that means you can update your app to the latest Platform today! We recommend doing so as soon as possible so that your app doesn't have an "Outdated" badge next to it in AppCenter on release day.

Platform 8 is based on the GNOME 46 platform and includes all of the same library updates as well as the latest Granite, elementary Stylesheet, and elementary Icons. Plus we're now including LibPortal, a library that makes it easy to use platform APIs for things like background &amp; autostart, taking screenshots, and setting wallpapers. Platform 8 includes the latest LibAdwaita with `Adw.ToolbarView` and the elementary stylesheet now supports it as well. Plus `Granite.Toast` now includes a new `dismissed ()` signal with  dismissal reasons, a new `STYLE_CLASS_SUCCESS` constant, and you can now use markup in `Granite.HeaderLabel`. We now also load widget fallback styles when using `Granite.init ()` that should improve your apps' cross-platform compatibility.

---

## Sponsors

At the moment we're just above 23% of our monthly funding goal and we're almost at 350 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

If you're not already in Early Access, you can be among the first to try the next release of elementary OS and give us your feedback by sponsoring elementary [for as little as $1/mo](https://builds.elementary.io/). Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
