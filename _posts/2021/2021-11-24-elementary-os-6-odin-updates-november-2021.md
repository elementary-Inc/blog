---
title: elementary OS 6 Updates for November, 2021
description: Getting ready for the holidays
author: cassidyjames
image: /images/elementary-os-6-odin-updates-november-2021/card.jpg
tags:
  - odin
  - updates
---

<figure class="on-screen" markdown="1">
![Screenshot]({{ page.image }})
</figure>

This past week was Thanksgiving in the US, which for my family means decorating for the holidays is in full swing. In a similar vein, we've spent some extra time over the past month focusing on both visual and functional polish to make sure elementary OS 6 looks as good and works as well as it can—read on for the details!

## The Desktop

We spent a lot of time working on improvements and new features across the desktop—from quick window switching and animations to new search functionality and improved indicator designs.

### Quick Window Switching

Let's start with possibly the most obvious update to elementary OS this month: the redesigned <kbd>Alt</kbd><kbd>Tab</kbd> quick window switcher.

Previously, quick window switching re-used the dock to show which app windows you'd switch between, and used the desktop to highlight just the newly-focused window. However, over time and based on a lot of real world feedback, we found that looking down at the dock—or even across physical space to the primary display in the case of multi-display users—was less intuitive and overloaded the dock's purpose. Visually focusing windows also meant a lot of flashing if you switched quickly, which was inelegant at best, and could be a real issue for people with certain types of photo-sensitivity. Thanks to [Aral Balkan](https://ar.al/2021/11/08/my-three-month-long-elementary-os-6-upgrade-adventure-in-three-parts-part-1-catts/), we kicked off a project to rework quick window switching—and the initial work has been released this month!

<figure class="half" markdown="1">
![Old](/images/{{ page.slug }}/gala-old.gif)
![New](/images/{{ page.slug }}/gala-new.gif)
<figcaption markdown="1">
**Left:** Old window switcher | **Right:** New window switcher
</figcaption>
</figure>

The new window switcher always shows centered on current display, making it much more likely to be near your gaze. It also features bigger icons, helping you more quickly identify apps. It includes window titles, helping to differentiate between multiple windows from the same app. We also ensured the new design helps you keep your context—and no longer flashes the screen. As a bonus, it follows both the dark style preference and your selected accent color, making your elementary OS installation feel even more personal.

### Dialogs

Not content to stop with the <kbd>Alt</kbd><kbd>Tab</kbd> quick window switcher, we also refreshed the interaction design of dialogs in elementary OS. First, you'll notice dialogs animate in from above on top of their parent window instead of shooting out from within their parent window. This helps reinforce that dialogs are a more transient interaction. We also dim the parent windows behind blocking modal dialogs to make it more clear which window it belongs to, and that the dialog has to be dealt with before proceeding.

<figure  markdown="1">
![Dialogs](/images/{{ page.slug }}/dialogs.gif)
<figcaption>New dialog animation</figcaption>
</figure>

These two changes make for a subtle but ever-present interaction change that is more clear and feels more modern.

We also fixed a handful of small visual issues across the desktop: legacy/server-side decorated windows should no longer have a clipped shadow, we isolated the workspace "nudge" animation (when trying to navigate past the last workspace) to only show on the primary display. and we improved that nudge animation to work with the mouse wheel in addition to touchpads and touchscreens.

### Applications Menu

Search Bookmarks
Prevent potential crash when starting

### Indicators

Sound: get device icons, allow horizontal scroll, clean up invalid "analog" output devices
Network: prevent blank VPN entries

### Housekeeping

Redesign Housekeeping and add Downloads option, Security & Privacy settings: Add Downloads option to Housekeeping

## Apps

### AppCenter

- Amusements appear in the Games category
- Categories show as a grid instead of a list
- Allow window to shrink to much narrower sizes

### Code

- Projects with the same name now include their parent folder name as well
- When scrolling to search results, overshoot slightly for better visibility
- Use the FileChooser portal instead of the one from GTK
- Center the global search dialog over the main Code window
- made the "Visible whitespace" simpler and more clear with a switch instead of a drop-down

- Fix visibility of Terminal button on Welcome page
- Fix some keyboard shortcuts affecting unfocused Document instead of focused Terminal
- Close Terminal if shell exited and create new Terminal if re-opened with no shell

### Files

### Camera

- Resolve issues with cameras being unavailable when multiple cameras are connected
- Default to a working camera if multiple cameras are connected and one is unavailable

## System Settings

Desktop: Move Text settings to their own page, More granular settings for text scale

Keyboard: Redesigned custom shortcuts view, On-screen keyboard switch in Layouts tab

Sound: Show device icons, Switch to enable the screen reader

User accounts: Update permissions when enabling and disabling accounts

## Other Fixes & Updates

Fixed a couple of issues discovered in the system stylesheet; namely, the accent color in IBus candidate window and the font style for labels in header bars (visible in Japanese).

And as always, there are translation updates, code cleanups, and other under-the-hood improvements included with these updates across the OS and apps.

For developers, min_length property for Granite.ValidatedEntry, Granite.HyperTextView for navigatable URLs in text views. New preferences-desktop-font* icons, additional sizes for playlist-queue, redesigned PDF file type, additional sizes for emblem-downloads, and removed arrows from Copy and Paste actions. 6.0.4 platform release with the latest Granite, icons, and stylesheet updates.

<aside markdown="1">
>We prioritize our work based directly off of the feedback we receive
</aside>

If you're experiencing an issue that wasn't fixed in this month's updates—or if you have an idea for a new feature—we'd love to hear from you. We prioritize our work based directly off of the feedback we receive. Be sure to check out our [issue reporting guide](https://docs.elementary.io/contributor-guide/feedback/reporting-issues) for tips and more info.

## Get These Updates

As always, if you're already running elementary OS 6 you can get updates directly from AppCenter by opening up the "Installed" tab and selecting "Update All." Previous OS 6 purchase links from email receipts will be upgraded to the newest OS 6 release as usual.

If you're not yet running elementary OS 6, we'll be publishing a new 6.0.4 download for a pay-what-you-can price that includes all of these updates [on our homepage](https://elementary.io) soon.
