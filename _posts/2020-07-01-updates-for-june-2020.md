---
title: "Hera Updates for June, 2020"
description: "OS 5.1.6"
author: danrabbit
image:
tags:
  - updates
  - hera
---

June was a busy month for elementary; we [started shipping elementary OS](/now-shipping-elementary-os/) on retailer devices, said [goodbye to Bountysource](/goodbye-bountysource-hello-github-sponsors/), started using [Plausible](https://plausible.io/blog.elementary.io) on the web (More about that later!), and of course, pushed out several updates to elementary OS. <!-- As usual, these updates are available in a new OS 5.1.6 ISO at [elementary.io](https://elementary.io) -->

## AppCenter

AppCenter should now correctly show all Flatpak runtimes in the updates view, solving an issue where AppCenter reported updates were available but showed nothing to update.

Also solved an issue with High CPU usage when a certain number of screenshots are downloaded

## Files

Add warning and error colored disk usage bars when disk becomes too full
Prevent window resizing when filename column width exceeds available space
Fixes:

Fix handling of filenames containing the # character
Fix regressions regarding pathbar context menus and clicking

## Videos

Start up faster with large libraries

Fix cases where subtitles refused to load
Handle if library folder is deleted or moved


## Code

Fix empty sidebar layout, ensuring folders can always be added

You can now scroll past the end of a file, making it easy to get a line a code exactly where you feel comfortable with it on screen.

And we've optimized the way Code saves and loads its window size and position to reduce how often it accesses your disk.

## Calendar
Calendar and the accompanying Date & Time panel indicator received a fix for events which where scheduled from a different timezone.

## Updates for Developers

granite 5.5.0 Released

New Style Constants:

STYLE_CLASS_COLOR_BUTTON
STYLE_CLASS_ROUNDED
Deprecations:

Several theming utilities. Use Gtk.CssProvider and Gtk.StyleContext instead
Granite.Services.SimpleCommand. Use GLib.AppInfo.create_from_commandline instead
Old unused utilities like get_button_layout_schema, get_default_close_button_position, and Granite.Services.Paths
Old unused widgets like CollapsiblePaned and CompositedWindow
Other Changes:

Granite.SourceList now gets Gtk.STYLE_CLASS_SIDEBAR by default
Updated translations

## And More

Several system components received minor updates to ensure that sessions end quickly and safely when logging out and shutting down.

## Get It

As always, you can get these updates on elementary OS 5.1 Hera alongside updated translations, bug fixes, and performance improvements by opening AppCenter and hitting **Update All**.

If you're new to elementary OS or would just like a fresh install, these updates will be included in a new elementary OS 5.1.6 Hera download on [our homepage](https://elementary.io) soon.

## A Quick Note

As we head into the second half of the year, more and more development focus is being put into elementary OS 6. While we intend to continue releasing updates to Hera for the forseeable future, we expect those updates to become more mundane and less noticeable. Several apps and components will likely no longer receive updates on elementary OS 5, including Terminal, Onboarding, parts of System Settings and more. This is because they're already making use of new features only available in elementary OS 6. We're excited to be working on a refreshed visual design, including dark mode and custom accent colors and taking advantage of the latest development libraries like Libhandy by Purism. But don't worry! elementary OS 5 will continue to receive security and stability updates to its underlying libraries until April of 2028, courtesy of Canonical. Also, we're almost ready to share a feature preview of elementary OS 6 for developers and enthusiasts, so stay tuned to our blog to hear more about what's coming and how you can get involved.
