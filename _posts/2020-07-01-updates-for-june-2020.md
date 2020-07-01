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

To smooth out the transition to elementary OS 6, we've released Granite 5.5.0 with a couple of a new things and a whole slew of deprecations! The new style constants `Granite.STYLE_CLASS_COLOR_BUTTON` and `Granite.STYLE_CLASS_ROUNDED` will become more useful in 6.0's fancy new stylesheet—there aren't color button styles in 5.x's stylesheet, but they're now available if you'd like to make use of them. Additionally, `Granite.Widgets.SourceList` now includes `Gtk.STYLE_CLASS_SIDEBAR` by default and we'll likely deprecate `Granite.STYLE_CLASS_SOURCE_LIST` in a future release.

The more important change is the number of deprecations in this release. There are several utilties and widgets in Granite that are now much better handled by Gtk and GLib, and will likely be removed in Granite 6.0. Expect to see some new deprecation warnings in Terminal if you're using any of the following:

- `Granite.Services.SimpleCommand` is deprecated and `GLib.AppInfo.create_from_commandline` should be used instead.
- Several theming utilites including `Granite.Utils.set_theming` and `Granite.Utils.get_css_provider` are now deprecated and `Gtk.CssProvider` and `Gtk.StyleContext` should be used directly instead.
- `Granite.Services.Paths` is deprecated and `GLib.Environment` provides methods that should be used instead.
- Old, unused utilities like `Granite.Utils.get_button_layout_schema` and `Granite.Utils.get_default_close_button_position` are now deprecated with no recommended replacement. There should no longer be a need for these at all. This also applies to the widgets `Granite.Widgets.CollapsiblePaned` and `Granite.Widgets.CompositedWindow` which are no longer necessary with modern Gtk3.

## And More

Several system components received minor updates to ensure that sessions end quickly and safely when logging out and shutting down.

## Get It

As always, you can get these updates on elementary OS 5.1 Hera alongside updated translations, bug fixes, and performance improvements by opening AppCenter and hitting **Update All**.

If you're new to elementary OS or would just like a fresh install, these updates will be included in a new elementary OS 5.1.6 Hera download on [our homepage](https://elementary.io) soon.

## A Quick Note

As we head into the second half of the year, more and more development focus is being put into elementary OS 6. While we intend to continue releasing updates to Hera for the forseeable future, we expect those updates to become more mundane and less noticeable. Several apps and components will likely no longer receive updates on elementary OS 5, including Terminal, Onboarding, parts of System Settings and more. This is because they're already making use of new features only available in elementary OS 6. We're excited to be working on a refreshed visual design, including dark mode and custom accent colors and taking advantage of the latest development libraries like Libhandy by Purism. But don't worry! elementary OS 5 will continue to receive security and stability updates to its underlying libraries until April of 2028, courtesy of Canonical. Also, we're almost ready to share a feature preview of elementary OS 6 for developers and enthusiasts, so stay tuned to our blog to hear more about what's coming and how you can get involved.
