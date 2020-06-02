---
title: "Hera Updates for May, 2020"
description: Improvements across AppCenter, Files, System Settings for OS 5.1.5
author: cassidyjames
image:
tags:
 - hera
 - updates

facebook:
mastodon:
reddit:
twitter:
---

In May, we focused on quality-of-life improvements primarily across AppCenter, Files, and System Settings panes. These updates have been released to users of elementary OS 5.1 throughout the month, and are available in the new OS 5.1.5 ISO from [the homepage](https://elementary.io).

## AppCenter

We continued our steady iterative improvements to AppCenter with new features and fixes. The big quality-of-life one: **users can now install updates without administrator permission.** Since an administrator had to approve the original installation and we provide clear expectations around curated versus non-curated apps, it didn't make sense to make users authenticate just for updates. This is part of our [ongoing work](https://github.com/orgs/elementary/projects/74) on reducing authentication fatigue and only elevating permissions when necessary.

Since by default on elementary OS Flatpak apps are already installed as user apps, installing and updating them does not require authentication, either.

On the more minor side, we made improvements to ensure apps on the homepage are more reliably displayed by caching previous results and falling back to them if needed. We also improved the  reliability of the Dock badge number, meaning it should better reflect the number of available updates.

## Files

In Files, copying an image and pasting into another app will paste the image itself instead of file paths, if possible; for example, you can now paste images right into an image editor or web apps in certain browsers. Similarly, you can now paste one or more cut or copied files into a folder by pressing <kbd>Ctrl</kbd><kbd>V</kbd> with the folder selected.

We now show the file info overlay in the List View as well, i.e. making it quicker to see the size of images at a glance no matter which view you prefer. You can now use the <kbd>Tab</kbd> key to cycle through search results instead of just the arrow keys. And when trying to open trashed files, we now show an informative dialog to let users know they must restore or move the file first.

We also fixed a handful of smaller issues. We fixed a small uneditable area in pathbar which is showing home folder placeholder, fixed an issue that prevented file modification times from showing, fixed the size of restored tiled windows, and fixed color tags disappearing when thumbnails are hidden.

## System Settings

Fix potential freeze when changing settings from multiple panes for Power, Date & Time, and Desktop settings.

Better support for various network encryption types and More accurately report encryption type in Network settings

## …and More

We greatly improved performance when switching months in date/time indicator when you have events, plus we fixed missing event dots in certain situations. We updated icons to use new consistent Bubblegum and Mint palette colors, plus added `software-update-urgent` and `sync-synchronizing`, and new sizes for `window-close-symbolic` and preference icons.

## Get It

As always, you can get these updates on elementary OS 5.1 Hera alongside updated translations, bug fixes, and performance improvements by opening AppCenter and hitting **Update All**.

If you're new to elementary OS or would just like a fresh ISO, these updates are also included in a new elementary OS 5.1.5 Hera download on [our homepage](https://elementary.io).
