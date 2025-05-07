---
title: A Little Bit Now, A Lotta Bit Later
description: Updates for OS 8 and Early Access
author: danrabbit
image: /images/updates-for-may-2025/monitor.png

tags:
  - circe
  - updates
---

In mid-March we released a big bug fix update—elementary OS 8.0.1—and since then we've been hard at work on even more bug fixes and some new exciting features that I'm excited to share with you today! Read ahead to find out what we've released recently and what you can help us test in Early Access.

## Quick Settings

<figure markdown="1" class="card">
![Quick Settings](/images/{{ page.slug }}/quick-settings.png)
<figcaption markdown="1">
Quick Settings has a new "Prevent Sleep" toggle
</figcaption>
</figure>

[Leo](https://github.com/lenemter) added a new "Prevent Sleep" toggle. This is useful when you're giving a presentation or have a long-running background task where you want to temporarily avoid letting the computer go to sleep on its normal schedule. We also fixed a bug where the "Dark Mode" toggle would cancel the dark mode schedule when used. We now have proper schedule snoozing, so when you manually toggle Dark Mode on or off while using a timed or sunset-to-sunrise schedule, your schedule will resume on the next schedule change instead of being canceled completely. [Vishal](https://github.com/vjr) also fixed an issue that caused some apps to report being improperly closed on system shutdown or restart and on the lock screen we now show the "Suspend" button rather than the "Lock" button.

## System Settings

Locale settings has a fresh layout thanks to [Alain](https://github.com/alainm23) with its options aligned more cleanly and improved links to additional settings.

<figure markdown="1">
![Locale](/images/{{ page.slug }}/settings-locale.png)
<figcaption markdown="1">
Locale Settings has a more responsive design
</figcaption>
</figure>

We've also added the phrase "about this device" as a search term for the System page and improved interface copy when a restart is required to finish installing updates based on your feedback. Plus, [Stanisław](https://github.com/stsdc) improved stylus detection in Wacom settings preventing a crash when no stylus is found.

## AppCenter

We now show a small label next to the download button for apps which contain in-app purchases. This is especially useful for easily identifying free-to-play games or alt stores like Steam or Heroic Games Launcher.

<figure markdown="1">
![AppCenter](/images/{{ page.slug }}/appcenter.png)
<figcaption markdown="1">
AppCenter now shows when apps have in-app purchases
</figcaption>
</figure>

Plus, we now reload app icons on-the-fly as their data is processed, thanks to [Italo](https://github.com/edwood-grant). That means you'll no longer get occasionally stuck with an AppCenter which shows missing images for app's who have taken a bit longer than usual to load.

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

Our development focus recently has been on some of the bigger features that will likely land for either elementary OS 8.1 or 9. We've got a new app, big changes to the design of our desktop itself, a whole lot of under-the-hood cleanup, and the return of some key system services thanks to a new open source project.

## Monitor

<figure markdown="1">
![Monitor](/images/{{ page.slug }}/monitor.png)
<figcaption markdown="1">
We're now shipping a System Monitor app by default
</figcaption>
</figure>

By popular demand—and thanks to the hard work of [Stanisław](https://github.com/stsdc)—we have a new system monitor app called "Monitor" shipping in Early Access. Monitor provides usage information for your processor, GPU, memory, storage, network, and currently running processes.

<figure markdown="1" class="card">
![Panel](/images/{{ page.slug }}/monitor-panel.png)
<figcaption markdown="1">
You can optionally see system information in the panel with Monitor
</figcaption>
</figure>

You can also optionally get a ton of glanceable information shown in the panel. There's currently a lot of work happening to port Monitor to GTK4 and improve its functionality under the Secure Session, so make sure to report any issues you find!

## Multitasking

<figure markdown="1" class="card">
![Dock](/images/{{ page.slug }}/dock.png)
<figcaption markdown="1">
The Dock is getting a workspace switcher
</figcaption>
</figure>

Probably the biggest change to the Pantheon shell since its early inception, the Dock is getting a new workspace switcher! The workspace switcher works in a familiar way to the one you may have seen in the Multitasking View: Your currently open workspaces are represented as tiles with the icons of apps running on them; You can select a workspace to switch to it; You can drag-and-drop workspaces to rearrange them; And you can use the "+" button to create a new blank workspace. One new trick however is that selecting the workspace you're already on will launch Multitasking View. The new workspace switcher makes it so much more accessible to multitask with just the mouse and get an overview of your workflows without having to first enter the Multitasking View. We're really excited to hear what people think about it!

<figure class="card">
  <video width="1920" height="1080" autoplay="true" loop="true" playsinline="true" muted="true">
    <source src="/images/updates-for-may-2025/multitasking-swipe.mp4" type="video/mp4">
  </video>
  <figcaption>You can close apps from Multitasking View by swiping up</figcaption>
</figure>

Another very satisfying feature for folks using touch input, you can now swipe up windows in the Multitasking View to close them. This is a really familiar gesture for those of us with Android and iOS devices and feels really natural for managing a big stack of windows without having to aim for a small "x" button.

## GTK4 Porting

We've recently landed the port of Tasks to GTK4. So far that comes with a few fixes to tighten up its design, with much more possible in the future. Please make sure to help us test it thoroughly for any regressions!

<figure markdown="1">
![Tasks](/images/{{ page.slug }}/tasks.png)
<figcaption markdown="1">
Tasks has a slightly tightened up design
</figcaption>
</figure>

We're also making great progress on porting the panel to GTK4. So far we have branches in review for Nightlight, Bluetooth, Datetime, and Network indicators. Power, Keyboard, and Quick Settings indicators all have in-progress branches. That leaves just Applications, Sound, and Notifications. So far these ports don't come with major feature changes, but they do involve lots of cleaning up and modernizing of these code bases and in some cases fixing bugs! When the port is finished, we should see immediate performance gains and we'll have a much better foundation for future releases. You can follow along with our progress porting everything to GTK4 [in this GitHub Project](https://github.com/orgs/elementary/projects/95/views/1).

## And More

When you take a screenshot using keyboard shortcuts or by secondary-clicking an app's window handle, we now send a notification letting you know that it was succesful and where to find the resulting image. Plus there's a handy button that opens Files with your screenshot pre-selected.

We're also testing [beaconDB](https://beacondb.net/) as a replacement for Mozilla Location Services (MLS). If you're not aware, we relied on MLS in previous versions of elementary OS to provide location information for devices that don't have a GPS radio. Unfortunately Mozilla [discontinued the service](https://www.omgubuntu.co.uk/2024/03/mozilla-location-services-axed) last June and we've been left without a replacement until now. Without these services, not only did maps and weather apps cease to function, but system features like automatic timezone detection and features that rely on sunset and sunrise times no longer work properly. beaconDB offers a drop-in replacement for MLS that uses Wireless networks, bluetooth devices, and cell towers to provide location data when requested. All of its data is crowd-sourced and opt-in and several distributions are now defaulting to using it as their location services data provider. I've set up a small sponsorship from elementary [on Liberapay](https://liberapay.com/joelkoen/) to support the project. If you can help support beaconDB either by sponsoring or providing stumbler data, I'd highly encourage you to do so!

---

## Sponsors

At the moment we're at 23% of our monthly funding goal and 336 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
