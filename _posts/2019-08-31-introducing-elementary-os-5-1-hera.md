---
title: Introducing elementary OS 5.1 Hera
description: A major update on a solid foundation
author: cassidyjames
image: https://cdn-images-1.medium.com/max/1600/1*LjHTYMbr_p3fOsUNa38QqA.jpeg

tags:
  - hera
  - juno
  - release
  - updates
---

![Hera wallpaper](https://cdn-images-1.medium.com/max/1600/1*LjHTYMbr_p3fOsUNa38QqA.jpeg)

In October, we [announced elementary OS 5 Juno][juno] with wide-ranging updates to provide a more refined user experience, improve productivity for new and seasoned users alike, and take our developer platform to the next level. Today we're pleased to announce elementary OS 5.1 Hera, the latest major update.

Hera builds on the solid foundation of Juno while bringing: 

1. A brand new installer, greeter, and onboarding experience
2. Major updates around accessibility and System Settings
3. Iterative improvements across nearly all apps
4. The latest hardware enablement and support

## What's in a Name and Number?

We detailed our shift in the numbering scheme from the 0.x of old to Juno being elementary OS 5 when we announced it back in October. In the same vein, Hera builds on the new numbering scheme.

elementary OS 5.1 Hera takes the same foundation as Juno-utilizing the same underlying repositories and libraries-but builds on it with a refined experience. It is the culmination of our work over the past nine months packaged up into one cohesive update. As such, the 5.1 number represents that it's a major update, but not an entirely new version (which usually come around every two years). It's still significant enough, however, to deserve its own name and identity.

We always name our releases after mythological beings and deities, and Hera is no different. The Greek equivalent of Juno, Hera is considered the queen of the Greek gods and represents women, marriage, family, and childbirth.

## Updates from the Juno Release

Since Hera builds on Juno, it includes [all of the monthly OS updates][updates] we've detailed since Juno's release. You can check those monthly stories for the nitty-gritty-and if you've diligently followed along, everything after Installer, Greeter, and Onboarding will be a review-but here's a higher-level overview of what Hera brings:

### Installer, Greeter, and Onboarding

This is the trifecta of major new features for Hera. 

<figure class="third" markdown="1">
![Disk Encryption](https://cdn-images-1.medium.com/max/800/1*yduIK-8ivl7dJj1sDHEqzQ@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*yduIK-8ivl7dJj1sDHEqzQ@2x.png 2x"}
![Keyboard Layout](https://cdn-images-1.medium.com/max/800/1*1q2aXstHd_08_KYMTtgj8g@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*1q2aXstHd_08_KYMTtgj8g@2x.png 2x"}
![Select a Language](https://cdn-images-1.medium.com/max/800/1*eKhZa1Ir8HB9m9Wfc5ka3w@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*eKhZa1Ir8HB9m9Wfc5ka3w@2x.png 2x"}
<figcaption>A few screens of the new Installer</figcaption>
</figure>

We've been working on the new Installer for over a year now, and it's finally ready to ship to users. It's designed to be simple and straightforward, and really fast. It handles getting the OS installed onto bare metal, and little more. In line with our Secure By Default efforts, it heavily encourages full-disk encryption out of the box to keep user data more secure.

<figure markdown="1">
![Customize Partitions](https://cdn-images-1.medium.com/max/800/1*9aBxCBQ2lIlMh_iroBp6bg@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*9aBxCBQ2lIlMh_iroBp6bg@2x.png 2x"}
<figcaption>Customize Partitions view for more control</figcaption>
</figure>

It does also include a Customize Partitions feature to let users with more unique setups (including specific filesystem preferences and multi-booting installs) install elementary OS just how they'd like.

<!-- TODO: Greeter screenshot -->

Along with the installer comes a new redesigned login and lockscreen greeter that looks sharper, works better, and handles creating a new user when none exist. It also fixes many reported issues with the previous greeter including focus issues, HiDPI issues, and better localization. It pairs with the installer to streamline the first boot experience, only handling creating a new user once the OS is installed. This follows our [every-install-is-an-OEM-install design][oem-design], meaning less variance between installing your own OS and getting it included from an OEM.

<figure class="third" markdown="1">
![Welcome screenshot](https://miro.medium.com/max/1120/1*OsUdeEafTuWof7e_jdEeNg@2x.png)
![Location Services screenshot](https://miro.medium.com/max/1120/1*CHRbLVIpEKti-vzcN6c8IA@2x.png)
![Night Light screenshot](https://miro.medium.com/max/1120/1*dZ6zFyWk48YBA-tjoB3V-g@2x.png)
![Housekeeping screenshot](https://miro.medium.com/max/1120/1*5tVjv1f9GqHfHmYjFYfJlQ@2x.png)
![AppCenter screenshot](https://miro.medium.com/max/1120/1*2lEgiaFuFnV-fM9WcsU4sQ@2x.png)
![Finished screenshot](https://miro.medium.com/max/1124/1*XMhBb2LH7zaW1VFQeORMow@2x.png)
</figure>


Lastly, [the new Onboarding app] introduces key features to users and handles common first-run tasks like managing privacy settings. Since it's a modular component-and not all baked into one piece of software along with an installer and new user creation-the Onboarding experience works great for newly-created users on existing installs, as well. When a major new feature lands in elementary OS, Onboarding can also be used to introduce it to existing users. You can read more about Onboarding and its design and development process in our story from earlier this month.

<!-- TODO: Include onboarding post -->

Together, these three components greatly improve the first impressions of elementary OS from installing the OS or getting a new computer all the way through using your account for the first time. With a fresh codebase across all three, we'll also be able to more quickly iterate on features and fixes.

### Accessibility and System Settings

In February, we [shared our philosophy on accessibility features][accessibility] and how they should be exposed as fully-supported features to all users. In elementary OS 5.1 Hera, we're now shipping several improvements in System Settings that expose more accessible settings for all users. Performance and keyboard shortcut discoverability has also been improved. We've also improved several other areas in System Settings based on reported issues.

<figure markdown="1">
![Displays](https://cdn-images-1.medium.com/max/800/1*MktQpi08_85vY78wMKLWDg.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*MktQpi08_85vY78wMKLWDg.png 2x"}
<figcaption>Improved Displays settings</figcaption>
</figure>

The Displays settings have been improved, bringing a more reliable scaling factor setting, new refresh rate options, and an improved design using palette colors.

<figure markdown="1">
![Sound](https://cdn-images-1.medium.com/max/800/1*NPiwb5nTWZoM_Y5moHPAYw@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*NPiwb5nTWZoM_Y5moHPAYw@2x.png 2x"}
<figcaption>Improved Sound settings</figcaption>
</figure>

Sound settings have also been improved with a new approach to handling external devices. The result is a simpler way of picking your output device and the more reliable display of available devices. We've also added the "Flash screen" option for event alerts here to better manage whether alerts are audible, visual, both, or neither. This is particularly handy for the hearing impaired or to use in environments where an audible alert would be inappropriate, like live production.

<figure class="third" markdown="1">
![General Mouse & Touchpad settings](https://cdn-images-1.medium.com/max/800/1*7sjK_MxYqydyoW-YqlApPw@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*7sjK_MxYqydyoW-YqlApPw@2x.png 2x"}
![Mouse settings](https://cdn-images-1.medium.com/max/800/1*C2FeSPnxKkb-4bOHA5VJxw@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*C2FeSPnxKkb-4bOHA5VJxw@2x.png 2x"}
![Touchpad settings](https://cdn-images-1.medium.com/max/800/1*NxDWr5_QRXNRQ3lQFvDJMw@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*NxDWr5_QRXNRQ3lQFvDJMw@2x.png 2x"}
<figcaption>Improved Mouse & Touchpad settings</figcaption>
</figure>

Mouse & Touchpad settings have been redesigned and improved for Hera. They're now organized into tabs for different hardware-specific settings, plus several accessibility settings like long-press secondary click, reveal pointer, and control pointer using keypad have been exposed. We've also added the highly-requested "Ignore when mouse is connected" toggle to the touchpad settings.

<figure markdown="1">
![Bluetooth settings](https://cdn-images-1.medium.com/max/800/1*RPQW7xDn904fMIufTe7sRg@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*RPQW7xDn904fMIufTe7sRg@2x.png 2x"}
<figcaption>Improved Bluetooth settings</figcaption>
</figure>

Bluetooth settings have been improved with more reliable pairing and trusting of devices, plus improved device support including certain keyboards and devices that require pairing with a pin or code.

<figure markdown="1">
![Desktop Appearance settings](https://cdn-images-1.medium.com/max/800/1*m-kaKQqh_o9XsqFa967kaA@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*m-kaKQqh_o9XsqFa967kaA@2x.png 2x"}
<figcaption>New Desktop Appearance settings</figcaption>
</figure>

We've added a new Appearance tab to the Desktop settings, exposing some existing accessibility settings and making them more discoverable. This includes a new wider range of supported text sizes, from small (0.75x) to larger (1.5x). This should help those who need larger or smaller text, including alleviating some issues with certain hardware combinations where 1x or 2x display scaling is not the best fit.

<figure markdown="1">
![Applications Menu search](https://cdn-images-1.medium.com/max/697/1*TTr3mUvKtb--h57ZVCxORA@2x.png){: srcset="https://cdn-images-1.medium.com/max/1395/1*TTr3mUvKtb--h57ZVCxORA@2x.png 2x"}
<figcaption>Improved Applications Menu search</figcaption>
</figure>

Lastly, we've made both System Settings and system actions like restarting much more discoverable in Hera with greatly improved deep searching from the Applications Menu. You can now search for something like "display" and get a list of all the individual features in each pane where the word "display" is used. We've also updated those keywords across all actions and settings panes, making them even easier to find-including common alternatives like "reboot" for Restart.

### App Updates

As with any major elementary OS update, we've been hard at work on several built-in apps for Hera.

<figure markdown="1">
![AppCenter categories](https://cdn-images-1.medium.com/max/800/1*r2DZyxdSOc6wSYzkFdSJjw@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*r2DZyxdSOc6wSYzkFdSJjw@2x.png 2x"}
<figcaption>New & Improved AppCenter categories</figcaption>
</figure>

To make more apps more discoverable in AppCenter, we've improved and added several new categories in Hera. We've also greatly improved performance and stability in several areas, plus fixed reported issues including ones related to email validation, visibility of available apps, and button styles. And since Hera is built from the same foundation as Juno, **all AppCenter apps released so far for Juno will automatically be available in Hera**.

{% comment %}
<!-- TODO: Uncomment if it's released, otherwise remove -->
AppCenter in Hera also includes our first steps towards a Flatpak future, with support for the newer packaging format built-in. While nothing has changed with the way curated apps are distributed to elementary OS just yet, any manually-added Flatpak remotes are now usable within AppCenter.
{% endcomment %}

<figure markdown="1">
![Calendar](https://cdn-images-1.medium.com/max/800/1*GqkCuLStGsy2cfvXU8jqTA@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*GqkCuLStGsy2cfvXU8jqTA@2x.png 2x"}
<figcaption>Refreshed Calendar design</figcaption>
</figure>

We've put a lot of work into Calendar for Hera with a refreshed design that is brighter, cleaner, and more usable. Keyboard navigation, color palette usage, and the event dialog have also all been improved. See the February updates story for more information.

<figure markdown="1">
![Code](https://cdn-images-1.medium.com/max/800/1*mO9RqSUJy2WYKZWhAf3QAA@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*mO9RqSUJy2WYKZWhAf3QAA@2x.png 2x"}
<figcaption>Improved keyboard shortcut discoverability in Code</figcaption>
</figure>

Code has been updated for Hera with more discoverable keyboard shortcuts, the restoration of the line wrap setting, new "Change Branch" functionality for git projects, and the display of hidden and non-text files in the sidebar to make git management more accurately reflect the state of the repository. We've also implemented several fixes and performance improvements, especially around saving and restoring files.

<figure markdown="1">
![Files](https://cdn-images-1.medium.com/max/800/1*XG7msxmcJ-dPFZPn-fxmmQ@2x.png){: srcset="https://cdn-images-1.medium.com/max/1600/1*XG7msxmcJ-dPFZPn-fxmmQ@2x.png 2x"}
<figcaption>Improved keyboard shortcut discoverability in Files</figcaption>
</figure>

For Files, we've made search more discoverable in Hera by showing the search icon and placeholder text in the Home folder, similar to a web browser's empty state. The search results dropdown is also larger and shows more results, and there's a new feature to hide thumbnails. "Cherry picking" files has been greatly improved, and we've refined the design of the color tags to be easier targets-plus we show all color tags used in a selection in the context menu. We've also improved keyboard shortcut discoverability throughout, improved the Open In and Open With menus with app icons, and made Files respect the Event Alerts setting from _System Settings_ → _Sound_ for the trash sound. Lastly, we've implemented several performance and stability improvements including fixing reported issues around file sorting, color tags, file renaming, and more.

<figure markdown="1">
![Music preferences](https://cdn-images-1.medium.com/max/337/1*mZGIW4KbddMKDyzKoaKAww@2x.png){: srcset="https://cdn-images-1.medium.com/max/674/1*mZGIW4KbddMKDyzKoaKAww@2x.png 2x"}
<figcaption>Improved keyboard shortcut discoverability in Files</figcaption>
</figure>

We've spent a lot of time improving Music for Hera, with large improvements to sorting in the album, list, and column views. We also updated it with more discoverable keyboard shortcuts, plus a new bold orange accent color throughout, carrying its identity from the icon into the app itself. We fixed several reported issues with queuing and playlists. Music can now also play s3m files and double clicking an album cover in the grid view will start playing that album. Lastly, album art in the grid view is now displayed more crisply on HiDPI displays.

### Desktop

We've been steadily improving the core desktop experience in elementary OS Hera.

Picture-in-Picture now displays at the bottom-right of the display by default, better matching where users expected it. We've made several usability and performance improvements to taking screenshots.  We also addressed a couple of visual glitches that sometimes occurred when tiling windows and on HiDPI displays after switching the scaling factor.

<figure markdown="1">
![Session indicator](https://cdn-images-1.medium.com/max/288/1*SUshGaq26qOgbMP3gkxi0g@2x.png){: srcset="https://cdn-images-1.medium.com/max/577/1*SUshGaq26qOgbMP3gkxi0g@2x.png 2x"}
<figcaption>Session Indicator with keyboard shortcuts</figcaption>
</figure>

We've also brought several improvements to the top Panel and Indicators to Hera. The Applications Menu now shows all configured keyboard shortcuts in its tooltip and is a bit faster. We've improved the design of the Bluetooth indicator to be more consistent with other indicators and added connection status badge to each device. The Date & Time indicator makes the selected day more clear and more reliably shows events for the current day. The Session indicator now shows keyboard shortcuts for lock and log out. We improved several aspects of the Sound indicator including smooth scrolling, touchpad scrolling, and scroll directions, plus new features for microphone users like scrolling or middle-clicking the mic icon on the panel to adjust or mute input.

### Visual Style

We've subtly improved the system stylesheet in several ways for Hera.

<figure class="card" markdown="1">
![Sidebar badges](https://cdn-images-1.medium.com/max/166/1*59rV-UJoPkUM_e2cK7KLFQ@2x.png){: srcset="https://cdn-images-1.medium.com/max/332/1*59rV-UJoPkUM_e2cK7KLFQ@2x.png 2x"}
<figcaption>More subtle badges in sidebars</figcaption>
</figure>

More subtle badges in sidebarsContrast is further improved-especially for apps that utilize a dark style-and we've refreshed the appearance of numbered badges in Sidebars to be a bit more subtle. We've also improved accent color shading in switches, fixed some right-to-left issues, fixed some insensitive buttons states, fixed other small issues (see the [June updates story][june] for more), and added support for raised buttons in app header bars.

The system icons have also been refreshed throughout Hera with added icons for playlists, chat, caps lock, num lock, mail actions, SSDs, and headsets. We've refined and added several new sizes for icons for pixel-perfect hinting in more contexts-including the Onboarding experience. We also added symbolic versions of several icons including location services, laptops, and firmware. We've animated the microphone mute icon in the Panel, the mobile phone icons have been updated to better match modern phones, path and group icons (for drawing/design apps) have been redesigned, we've added a few mirrored icons for right-to-left languages, and we've made several icon families a bit more consistent.

Lastly, the default wallpaper has been updated. This photo of a sunset over a pier was included in Juno, but we've set it as the new default to give Hera its own unique identity. At the same time the color scheme is similar to Juno with its purples, oranges and blues-evoking the more iterative relationship between the two releases.

### Hardware Support

Along with all of the functional updates, translations, and issue fixes comes the latest hardware enablement provided by Linux 4.18 and the LTS HWE stack from Canonical. This includes improved support for more recent processors, GPUs, input devices, and more.

## Get It

Due to the rolling nature of elementary OS updates, **users of elementary OS 5 Juno get the update to 5.1 Hera alongside regular system updates** from AppCenter. You can also always check _System Settings_ → _About_ to ensure you're on the latest version. If you haven't been upgraded to 5.1 Hera yet, hit the "Check for Updates" button to open AppCenter, and install any updates listed. 

The one exception is the HWE stack; if you'd like the improved hardware support, you can install the latest HWE stack from Terminal with the following command:

`sudo apt install --install-recommends linux-generic-hwe-18.04 xserver-xorg-hwe-18.04`

New users or those who prefer a fresh start can also download elementary OS 5.1 Hera from [elementary.io]. Even if you already have an older Juno ISO, we recommend downloading the latest Hera ISO if you're planning to perform a new install-you'll automatically get the latest hardware support, the new installer and onboarding, and to reduce the number of updates necessary once it's installed.

[updates]: {{ site.baseurl }}/tags/#updates
[accessibility]: {{ site.baseurl }}{% post_url 2019-02-16-accessibility-features-are-just-features %}
[oem-design]: https://github.com/elementary/installer/wiki#every-install-is-an-oem-install
[onboarding]: {{ site.baseurl }}{% post_url 2019-07-23-get-settled-into-elementary-os-with-onboarding %}
[june]: {{ site.baseurl }}{% post_url 2019-07-01-juno-updates-for-june-2019 %}
[juno]: https://medium.com/elementaryos/elementary-os-5-juno-is-here-471dfdedc7b3
[elementary.io]: https://elementary.io

