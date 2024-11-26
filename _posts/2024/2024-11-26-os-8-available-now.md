---
title: elementary OS 8 Available Now
description: Carefree because you're cared for
author: danrabbit
image: /images/os-8-available-now/card.png

tags:
  - circe
  - release

sponsor:
  name: Laptop with Linux
  link: https://laptopwithlinux.com/linux-laptops/
  image: /images/os-8-available-now/laptop-with-linux.png
  hook: "Laptop with Linux offers laptops and desktops that are perfectly tuned and optimized for use with various Linux-based operating systems and ships worldwide! They aim to make switching to Linux accessible for every computer user by increasing freedom of choice. Buy a laptop pre-installed with elementary OS 8.0 now!"
---

Today, we're proud to announce that elementary OS 8 is available to download now and shipping on several high-quality computers!

<figure markdown="1">
![elementary OS 8](/images/{{ page.slug }}/card.png){: width="1200" height="628"}
</figure>

With OS 8, we've focused in on:

- Creating a new **Secure Session** that ensures applications respect your **privacy** and require your **consent**
- **A brand new Dock** with productive **multitasking and window management** features
- Empowering our diverse community through **Inclusive Design**

To get elementary OS 8 now, head to [elementary.io] for the download—or read on for an overview of what's new.

---

# Privacy, Security &amp; Consent

Over the past several years we've been building features to improve the trust relationship with your computer by requiring your explicit informed consent and disallowing untrustworthy behavior on a technical level. We've done that by embracing Flatpak as the way to install apps on elementary OS and Portals for confining them to a safer sandbox. Now we're extending that story with both new settings to put you in control of the system features apps can access and a new Secure Session powered by Wayland.

<figure class="half" markdown="1">
![Screenshot Portal](/images/{{ page.slug }}/Portals/screenshot.png){: width="538" height="211"}
![Wallpaper Portal](/images/{{ page.slug }}/Portals/wallpaper.png){: width="538" height="226"}
<figcaption markdown="1">
In the Secure Session apps need your explicit permission for more things
</figcaption>
</figure>

On the lock screen, you'll now see a gear menu next to the password field that gives you the option of Classic or Secure sessions. If you select the Secure Session, elementary OS will use Wayland, a modern and secure method for apps to draw themselves and accept your input. In the Secure Session, apps will be more restricted and will require your consent for access to system features. When an app wants to listen in the background for your keystrokes, take a screenshot, record the screen, or even pick up the color from a single pixel, you will be asked first to make sure that it's okay. The Secure Session also comes with other modern features like support for Mixed DPI modes—A hotly requested feature for folks using a HiDPI notebook or tablet with a LoDPI external display—and improved support for multi-touch gestures on touch screens and tablets. You might also experience improved performance and smoothness, especially on low-powered hardware.

<aside markdown="1">
>OS 8 will use the Classic Session by default and apps will work and behave as they always have
</aside>

Portals are the standardized system interfaces that apps use to access features in a way that respects your privacy and requires your explicit consent. Four new Portals are now supported in OS 8: Color Picker, Screenshot, Screencast, and Wallpaper. These Portals are essential for enabling modern apps to work in the Secure Session when they don't have direct access to the pixels on your display. Since some apps haven't yet made use of the Portals required to operate under the Secure Session, OS 8 will continue to use the Classic Session by default. Apps will work and behave as they always have there, with the same level of system access you're used to from OS 7 and before. If you rely on certain accessibility features, you may find that those are not yet available under the new Secure Session as well. However, we highly encourage you to give the Secure Session a try and you might be surprised to find that the apps and features you use are already compatible.

<figure markdown="1">
![Application Settings](/images/{{ page.slug }}/Settings/permissions.png){: width="884" height="576"}
<figcaption markdown="1">
System Settings → Applications has expanded options
</figcaption>
</figure>

Application settings has an all-new design that expands your control over permissions. We now support adjusting the run-time permissions in Flatpak's Permissions Store—these are set when an app explicitly asks for your permission to access a feature while it's running. So if you've previously denied an app access to run in the background or granted an app permission to set the wallpaper, you can change your mind at any time and adjust permissions here. We've also adjusted the language of install-time permissions—aka sandbox holes—to be more clear that these represent advanced system access and the implications of adjusting them. Plus the descriptions of several individual items were changed based on your feedback to use less technical language. And app permission pages now show the app's icon and description.

# Getting Apps You Need &amp; Staying Up to Date

In 2017 [we shipped AppCenter](https://blog.elementary.io/building-the-future-of-elementary-os/), the Open Source pay-what-you-can app store and in 2021 we [revamped that store to use Flatpak](https://blog.elementary.io/elementary-appcenter-flatpak/), an app distribution technology that is decentralized by design and makes cross-platform app distribution on Linux-based operating systems a breeze. Since the move to Flatpak, you’ve always had the option to easily sideload apps directly from developers or use entire alternative app stores. In OS 8 we’re expanding your access to apps even further by including the most popular app store for Linux out of the box: Flathub.

<aside markdown="1">
>We’re expanding your access to apps even further by including Flathub out of the box
</aside>

This means you’ll be able to access apps made specifically for elementary OS, apps made for Linux, and popular cross-platform apps like Discord and Spotify all directly from AppCenter without having to manually sideload or configure an alt store.

<figure markdown="1">
![AppCenter](/images/{{ page.slug }}/AppCenter/home.png){: width="1078" height="716"}
</figure>

To support this change, we’ve made a few changes to App info pages in AppCenter. We’ve removed the “non-curated” badge based on your feedback and instead show a “Made for elementary OS” badge when appropriate. The links section has also been redesigned, featuring colorful iconography. We now show a Sponsor link for app developers that fund the development of their app using third-party platforms like GitHub or Patreon and we show a link directly to the app's source code for apps that provide it.

<figure class="half" markdown="1">
![AppCenter](/images/{{ page.slug }}/AppCenter/info-header.png){: width="1078" height="716"}
![Appcenter](/images/{{ page.slug }}/AppCenter/info-links.png){: width="1078" height="716"}
<figcaption>
App info pages show “Made for elementary OS” badges and more links
</figcaption>
</figure>

With the introduction of the Secure Session and new Portals to support it, expanded permissions settings, and sandbox warnings in AppCenter we feel much more confident in providing this expanded app access out of the box while upholding the expectation that the apps you get from AppCenter are reasonably safe, will ask for your consent, and respect your privacy.

In elementary OS there are two different kinds of updates. Updates to the operating system itself are installed offline, when your computer restarts, to make sure services are restarted correctly and to prevent issues. Updates to apps, on the other hand, are quickly installed while your computer is running. In OS 7, both of these types of updates appear side-by-side in AppCenter, but in OS 8 operating system updates will now appear in System Settings.

<figure markdown="1">
![System Settings](/images/{{ page.slug }}/Settings/system.png){: width="884" height="576"}
<figcaption markdown="1">
Operating system updates now appear in System Settings
</figcaption>
</figure>

Splitting apart these two update systems makes it faster to check for updates, more reliable to install them, and clearer which updates will require a restart: updates in AppCenter will never require a restart, while updates in System Settings will always require a restart.

<aside markdown="1">
>Updates in AppCenter will never require a restart, while updates in System Settings will always require a restart.
</aside>

The new system updates mechanism is super fast and includes the option to download updates automatically—which you can now opt-in to during Onboarding. It will also let you know if the updates package contains security updates and has improved error handling if things go wrong. Plus there are new options in the system shutdown dialog so you can install updates before shutting down or choose to skip a pending update, even when automatic updates are enabled.

# Multitasking &amp; Window Management

When planning for the Secure Session we realized that our Dock would need to be completely rewritten. So we took the opportunity a few years ago to run a survey and get better insights into the way you multitask on elementary OS and other operating systems. We then combined those new insights with the feedback we've received in GitHub over the years and carefully reconsidered the role of the Dock in our desktop alongside other desktop features which have appeared over the years. This has resulted in a Dock that retains the features you love from OS 7 and before and introduces whole new features to improve your multitasking workflow.

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "2021-ui-study-results-dock-multitasking" | first %}
{% include featured.html post=post %}
</div>

In particular, we've revisited the way we handle multi-window apps and made the behavior of clicking app icons more predictable. When an app isn't open yet, a single-click of its icon will still launch it. When an app has a single window open, a single-click will always focus that window, even switching workspaces if necessary. And, when an app has multiple windows open, a single-click will show a window spread so you can quickly select the right window, even outside of the Multitasking View. In this way, a single-click always takes you to an app window instead of sometimes opening a new window or even hiding windows.

<figure class="card">
  <video width="1920" height="1080" autoplay="true" loop="true" playsinline="true" muted="true">
    <source src="/images/os-8-available-now/Desktop/dock.webm" type="video/webm">
    <source src="/images/os-8-available-now/Desktop/dock.mp4" type="video/mp4">
  </video>
  <figcaption>When an app has multiple windows, clicking shows a window spread</figcaption>
</figure>

For apps that support multiple windows, we've implemented a new system that is aware of the FreeDesktop.org standard for hinting this feature, so we can now reliably open new windows when middle-clicking an app's icon. Plus you can still scroll over an app icon to cycle through open windows. And, you can now launch pinned apps with <kbd>⌘</kbd> + <kbd>1­</kbd>—<kbd>9</kbd>, a hotly requested feature.

We’ve also added several new optional multitasking features including the ability to switch between windows with a horizontal swipe gesture, the ability to disable hotcorners when on a workspace that contains a fullscreen app, and the ability to switch between workspaces by scrolling over the panel

# Designing for Inclusivity

We sat down this summer with self-described fully-blind cybersecurity enthusiast [Florian Beijers](https://blog.elementary.io/updates-for-july-2024/) to evaluate our experience for blind folks and identify areas of improvement. A particular showstopper we noticed was keyboard navigation and screen reader support during Onboarding, which has now been completely rewritten. We also took a second look at keyboard navigation and screen reader support during Installation and Initial Setup and the entire first run experience has been much improved for blind folks in OS 8. We also now have screen reader support in the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher and we’ve made sure that there's audio—or visual depending on your settings—feedback when we're unable to complete window management tasks like cycling workspaces in response to the keyboard shortcut.

<figure markdown="1">
![Onboarding](/images/{{ page.slug }}/Onboarding/home.png){: width="525" height="495"}
<figcaption markdown="1">
Navigation has been rewritten in Onboarding
</figcaption>
</figure>

System Settings has been refreshed with a modern space-saving dual-pane design that is more responsive for small and large displays. We’ve also vastly improved support for text scaling, screen readers, keyboard navigation, right-to-left language layouts, and improved contrast in illustrations. Plus search now returns more relevant results and the titles of those results now reflect both the exact setting name they’re matching and the path to that setting.

<figure class="third" markdown="1">
![System Settings](/images/{{ page.slug }}/Settings/search.png){: width="884" height="576"}
![System Settings](/images/{{ page.slug }}/Settings/appearance.png){: width="884" height="576"}
![System Settings](/images/{{ page.slug }}/Settings/touchpad.png){: width="884" height="576"}
![System Settings](/images/{{ page.slug }}/Settings/limits.png){: width="884" height="597"}
![System Settings](/images/{{ page.slug }}/Settings/network.png){: width="884" height="597"}
![System Settings](/images/{{ page.slug }}/Settings/notifications.png){: width="884" height="597"}
<figcaption>
Many System Settings pages feature modern redesigns
</figcaption>
</figure>

Instead of removing features during this redesign, we’ve added new ones. For example, if you're not a fan of overlaid scrollbars or have a motor disability that makes them difficult to use, there's a new setting to always show scrollbars in Desktop → Appearance. Language &amp; Region settings has a new option to automatically select the temperature unit based on locale. And there are new keyboard shortcut options for switching between keyboard layouts or using features like emoji or unicode typing.

<aside markdown="1">
>Instead of removing features during this redesign, we’ve added new ones
</aside>

Settings that use dropdowns are now frequently searchable. We've also improved setting descriptions, added new ones based on your feedback, and made sure help text is less frequently hidden behind a mouse hover. Plus, System got a redesign of external links similar to the one in AppCenter, with clearer help and documentation links as well as a better call for contributions.

<figure class="card" markdown="1">
![Quick Settings](/images/{{ page.slug }}/Desktop/quick-settings.png){: width="297" height="347"}
<figcaption markdown="1">
Quick Settings improves access to features while reducing clutter
</figcaption>
</figure>

OS 8 also brings a new Quick Settings menu that improves access to features while reducing clutter in the panel. We’ve started by combining the accessibility and session menus which contain useful controls, but don’t indicate a change in status. We’ve also added hotly requested controls like Dark Mode and Rotation Lock. Features like the Screen Reader and Onscreen Keyboard are now available from the Quick Settings menu by default, but you can still choose to hide them in System Settings → Desktop → Dock &amp; Panel.

By popular demand, we’re making a major change to our default keyboard shortcuts: pressing <kbd>⌘</kbd> will now open the Applications menu instead of the Shortcuts overlay and <kbd>⌘</kbd> + <kbd>Space</kbd> will now switch keyboard layouts by default. This brings us more in line with the defaults from other desktops and operating systems and will hopefully be more comfortable for folks who rely on these shortcuts to get around. Of course you can always change the <kbd>⌘</kbd> key behavior and keyboard shortcuts in general in System Settings → Keyboard.

Visual design plays a huge role in the appeal of our operating system and elementary has always had a strong identity in using colorful and playful design to convey a sense of friendliness and fun. In OS 8 we’ve maintained our careful balance of learning and evolving while avoiding chasing design trends to retain our unique personality.

<figure markdown="1">
![Pointers](/images/{{ page.slug }}/Desktop/pointers.png)
<figcaption markdown="1">
Pointers are more consistent and make better use of color
</figcaption>
</figure>

A perfect example of this is our new pointers. Pointers were completely redrawn to be more consistent, make better use of color, and be more precise. The new design is more fun and playful with softer edges and rounder corners while maintaining high contrast and legibility. The new design feels extremely familiar but also more modern.

<figure class="card half" markdown="1">
![A Large Body of Water Surrounded By Mountains](/images/{{ page.slug }}/Desktop/mountains.jpg)
![A Trail of Footprints In The Sand](/images/{{ page.slug }}/Desktop/sand.jpg)
</figure>

We have two new wallpapers to share, ["A Large Body of Water Surrounded By Mountains"](https://unsplash.com/photos/a-large-body-of-water-surrounded-by-mountains-Dxod5pdRtsk) by [Peter Thomas](https://unsplash.com/@lifeof_peter_) and ["A Trail of Footprints In The Sand"](https://unsplash.com/photos/a-trail-of-footprints-in-the-sand-of-a-beach-A9mr3TPoj0k) by [David Emrich](https://unsplash.com/@davidemrich). Both of these images have been slightly edited for use as wallpapers in elementary OS and are distributed under the permissive Unsplash license.

<figure class="card half" markdown="1">
![Multitasking View in light mode](/images/{{ page.slug }}/Multitasking/light.png)
![Multitasking View in dark mode](/images/{{ page.slug }}/Multitasking/dark.png)
<figcaption>
Multitasking View now features a blurred version of your wallpaper
</figcaption>
</figure>

Instead of a plain dark gray background, Multitasking View now features a blurred version of your wallpaper that is adjusted for light and dark modes. Workspace cards now have rounded corners and the switcher at the bottom of the screen has been updated for light and dark modes as well.

<figure class="card" markdown="1">
![Lock Screen](/images/{{ page.slug }}/Desktop/lock-screen.png)
<figcaption markdown="1">
The Login &amp; Lock Screen also features a blurred background similar to the Multitasking View as well as a larger and bolder clock
</figcaption>
</figure>

Several applications have a noticeably more modern design as well. Notably, Videos has a completely redesigned player page and now follows the system light and dark style preference. The new Fonts looks fantastic and has much better performance. And Web 46 brings its own set of performance improvements along with a more minimal appearance.

<figure class="third" markdown="1">
![Fonts](/images/{{ page.slug }}/Applications/fonts.png){: width="854" height="656"}
![Web](/images/{{ page.slug }}/Applications/web.png){: width="1078" height="824"}
![Videos](/images/{{ page.slug }}/Applications/videos.png){: width="1045" height="605"}
<figcaption>
Several apps have a noticeably more modern design
</figcaption>
</figure>

---

# Hardware Support

OS 8 includes the latest long-term support Hardware Enablement stack from Ubuntu, including Linux 6.8. We’re also shipping with Pipewire which improves latency and bluetooth audio quality while being architected for the world of sandboxed Flatpak apps running in the Secure Session. This is an especially big deal for folks doing audio production tasks on elementary OS.

<figure markdown="1">
![Driver Settings](/images/{{ page.slug }}/Settings/drivers.png)
<figcaption markdown="1">
Drivers moved to System Settings → System
</figcaption>
</figure>

Driver management has moved from AppCenter to System Settings → System. The new design for drivers is more in line with how drivers are managed on other operating systems and is easier to work with, especially for hardware that has multiple driver options like NVIDIA® graphics.

<figure markdown="1">
![Power Settings](/images/{{ page.slug }}/Settings/power.png){: width="884" height="597"}
<figcaption markdown="1">
Power Settings now shows battery charging levels
</figcaption>
</figure>

Power settings now shows the charging level and status for both internal batteries and connected battery devices like mice and keyboards. You can also choose to automatically set different power profiles based on whether your device is plugged in or on battery power, and power modes can be quickly changed from the power menu in the panel. Plus the battery icon in the panel will now show much more accurate battery levels for mobile computers.

<figure class="card" markdown="1">
![Power menu](/images/{{ page.slug }}/Desktop/power-menu.png){: width="334" height="460"}
<figcaption markdown="1">
Power modes can be changed from the power menu
</figcaption>
</figure>

---

# Get elementary OS 8

elementary OS 8 is available as a pay-what-you-can purchase at [elementary.io] today. Localized direct downloads and a torrent magnet link are provided.

<figure class="on-screen" markdown="1">
![A clean desktop](/images/{{ page.slug }}/Desktop/clean.png)
</figure>

<div style="text-align: center" markdown="1">
[OS 8 FAQ](https://github.com/orgs/elementary/discussions/categories/q-a){: .button.flat }
[Download elementary OS 8][elementary.io]{: .button.suggested }
</div>

OS 8 will receive additional feature and bug fix updates on a monthly schedule that will be reported on here on our blog, so stay tuned for even more updates in the future!

## Get A New Computer

Our hardware retailers [Laptop with Linux], [Star Labs], and [Slimbook] are offering elementary OS 8 out of the box starting today! Visit retailers' individual sites for more information.

<div style="text-align: center" markdown="1">
[Shop Devices][store]{: .button }
</div>

---

## Special Thanks

I want to give special thanks to all of our volunteer contributors for working hard over the last 13 months to make this an incredible release. We set some really ambitious goals and have made major architectural changes to accomplish them that required a lot of planning and coordination. Some of the features landed in this cycle have been years in the making. Our monthly blog posts highlight more of our individual contributors and it’s worth reading through them to admire their passion and dedication.

I’m also eternally grateful to our individual Early Access sponsors for providing consistent funding to keep producing our operating system and distributing it under our pay-what-you-can model. We’re funded almost entirely by the good will of individuals without any VC funding or major corporate backing. The only partnerships we have is with our indie hardware vendors. Choosing to support an operating system made by a community like ours is an act of protest in the world we currently find ourselves in and your solidarity means everything.

[elementary.io]: https://elementary.io
[updates]: {{ site.baseurl }}/tags/#updates
[Laptop with Linux]: https://laptopwithlinux.com/?ref=36&utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[Star Labs]: https://starlabs.systems/?rfsn=4227837.e8f025
[Slimbook]: https://slimbook.es/?utm_source=referral&utm_medium=elementary&utm_campaign=elementary
[store]: https://store.elementary.io/
