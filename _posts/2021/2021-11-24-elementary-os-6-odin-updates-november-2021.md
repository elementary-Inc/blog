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

Previously, quick window switching re-used the dock to show which app windows you'd switch between, and dimmed out the rest of the desktop to highlight just the newly-focused window. However, over time and based on a lot of real world feedback, we found that looking down at the dock—or even across physical space to the primary display in the case of multi-display users—was less intuitive and overloaded the dock's purpose. Dimming the desktop and visually focusing windows also meant a lot of flashing if you switched quickly, which was inelegant at best, and could be an accessibility issue for people with certain types of photo-sensitivity. Thanks to [Aral Balkan](https://ar.al/2021/11/08/my-three-month-long-elementary-os-6-upgrade-adventure-in-three-parts-part-1-catts/), we kicked off a project to rework quick window switching—and the initial work has been released this month!

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

<figure class="card" markdown="1">
![Dialogs](/images/{{ page.slug }}/dialogs.gif)
<figcaption>New dialog animation</figcaption>
</figure>

These two changes make for a subtle but ever-present interaction change that is more clear and feels more modern.

We also fixed a handful of small visual issues across the desktop: legacy/server-side decorated windows should no longer have clipped shadows, we isolated the workspace "nudge" animation (when trying to navigate past the last workspace) to only show on the primary display, and we improved that nudge animation to work with the mouse wheel in addition to touchpads, touchscreens, and the keyboard.

### Applications Menu

We landed a major new feature to the Applications Menu to speed up your workflow: file bookmark search! Now you can search right from the Applications Menu for bookmarked folders and locations like Downloads, Pictures, or even network shares.

<figure class="card" markdown="1">
![Bookmark search in Applications Menu](/images/{{ page.slug }}/bookmark-search.png){: width="888" height="689"}
<figcaption>Bookmark search in the Applications Menu</figcaption>
</figure>

And following cross-desktop standards, this feature will work with whatever your default file manager is—whether or not it's the default elementary Files app.

### Housekeeping

elementary OS has a Housekeeping feature where old temporary and trashed files can be automatically cleaned up to save space and help protect your privacy.

<figure class="half" markdown="1">
![Onboarding](/images/{{ page.slug }}/housekeeping-onboarding.png)
![Settings](/images/{{ page.slug }}/housekeeping-settings.png)
<figcaption markdown="1">
**Left:** Housekeeping in the Welcome app | **Right:** Housekeeping in System Settings
</figcaption>
</figure>

This month we improved Housekeeping with the addition of Downloads to the options, and a more clear and consistent design between both the Welcome app and System Settings.

### Sound

Lastly, we focused on improving the sound indicator and settings. In the indicator, you'll notice new device icons to make it easier to find the right output. We also improved the scroll interaction on the volume slider to work with horizontal scrolling, and cleaned up invalid "analog" output devices that could appear in certain situations.

<figure class="half" markdown="1">
![Sound indicator](https://user-images.githubusercontent.com/7277719/140836056-d5cd00ad-8be4-4f43-a7e4-32a27d0f01bc.png){: .card width="750" height="473"}
![Sound settings](https://raw.githubusercontent.com/elementary/switchboard-plug-sound/5bc331aa0c099c40d5940d1211403e1397e39395/data/screenshot.png){: width="929" height="689"}
<figcaption markdown="1">
**Left:** Sound indicator with device icons | **Right:** Sound settings with similar icons
</figcaption>
</figure>

In System Settings, you'll see similar but larger, full-color device icons to distinguish devices, as well as an easier-to-scan multi-line layout.

## Apps

We also released a handful of updates to the default apps this month.

### AppCenter

We've continued our work on the design of AppCenter with a few small but impactful changes. First, Category views (like Audio or System) are now shown with a more space-efficient grid view. We also separate paid, free, and non-curated apps (if you've added a third-party remote like Flathub) into their own sections within categories.

<figure class="constrained" markdown="1">
![Category view](https://user-images.githubusercontent.com/7277719/141206268-5505f96e-39e4-436e-970c-e72b6369d6cc.png)
<figcaption>Newly redesigned category view in AppCenter</figcaption>
</figure>

Apps categorized as "Amusements" will now appear in the Games category to better surface these types of apps. And lastly, we've improved the responsiveness of the UI throughout to allow the window to be resized to much narrower sizes.

### Code

In Code, we new distinguish between projects with the same name in the sidebar by including their parent folder. The project/folder search dialog now shows centered over then window, and when scrolling to search results, we overshoot the result slightly for better visibility. We also made the "visible whitespace" setting simpler and more clear with a switch instead of a drop-down. We're also now using the FileChooser portal provided by Files instead of the one from GTK; as a result, opening files and folders from within Code will now be more consistent with Flatpak apps.

If you use the Terminal extension, we fixed the visibility of Terminal button on Welcome page, fixed some keyboard shortcuts affecting unfocused document instead of focused Terminal, ensure the Terminal is closed if shell exited, and create a new Terminal if it's re-opened with no shell.

### Files

<!-- TODO: Double-check this was released. -->

We released a significant update to Files this month with a handful of fixes and improvements. Importantly, we rewrote the FileChooser portal

- Fix pasting of selected pathbar text into another window using middle-click
- Allow blank passwords for remote connections, e.g. for SSH via a private key
- Use "Send Mail" portal instead of contract
- Allow dropping bookmark directly below the Recent bookmark
- Do not show unusable drop target below the Trash bookmark

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
