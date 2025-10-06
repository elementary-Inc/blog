---
title: 
description: Updates for OS 8 and Early Access
author: danrabbit
image: /images/updates-for-october-2025/.png

tags:
  - circe
  - updates
  - earlyaccess
---

Hot off the release of OS 8.0.2, we've got a great new batch of feature updates for you as we get closer to the release of elementary OS 8.1!

# Maps

The first stable release of elementary Maps is now available for download on any Linux OS. For now we've focused on some of the basics like showing your current location, searching for locations, and handling `geo://` uri links.

<figure markdown="1">
![Maps](/images/{{ page.slug }}/maps.png)
</figure>

You may recall that Maps evolved from the Atlas code base originally written by [Steffen Schuhmann](https://launchpad.net/~sschuhmann) for elementary OS. [Ryo](https://github.com/ryonakano) has worked hard to maintain the code and update it for the latest platform libraries like GTK4. Since the rename, we've updated the app to match the latest elementary styles and design conventions. We've also added an illustrated view switcher between Explore and Transit maps and when you search you'll see color coded place type icons next to search results. Keyboard navigation,screen reader accessibility, and performance should also be slightly improved. Plus we have a modernized app icon, shoutouts to [Micah](https://github.com/micahilbery) for providing art direction.

<div style="text-align: center" markdown="1">
[Get Maps on AppCenter](https://appcenter.elementary.io/io.elementary.maps/){: .button.suggested }
</div>

# AppCenter

On the Home page, the "Updates &amp; installed apps" button is now properly labeled for screen readers. We've fixed a minor visual bug with banner shadows. And the "Education" category now has an icon.

In app info views, we now show a simple percentage-based app rating when ratings are available from [ODRS](https://odrs.gnome.org/)—the same ratings server used by apps like GNOME Software. Expect future versions of AppCenter to expand our support for ratings and reviews, but for now we have some groundwork laid out. App info views also now show content warnings with a more compact layout. [Italo](https://github.com/edwood-grant) updated our "End of Life" warnings to contain more accurate language, and licensing information now shows more detail and a simplified summary. Plus, we now show when a game supports playing with controllers. [Leonhard](https://github.com/leolost2605) added support for app addons, and we've simplified the "What's New" section to show just the latest release, with the option to view more releases in a separate version history window.

[Leonhard](https://github.com/leolost2605) did a ton of work in this release to make app updates faster and more reliable. The code has been massively streamlined and we've resolved reported crashes that some folks were experiencing while checking for updates. Plus we're now using GTK 4's FilterListModels for improved performance. The "Last checked" time is now updated every minute while the updates view is open and the gear menu can now be opened with the keyboard shortcut <kbd>F10</kbd>.

We've made a few changes to the way installed apps are shown to make it easier to keep up with what's new when you have automatic app updates turned on. Installed apps are now sorted by release date instead of alphabetically. The Releases dialog got a slight redesign and you can now see recent releases for all installed apps. And we've adjusted where the version number and store origin labels appear to clean up their layout.

Occasionally, app icons can take a little longer to load; When this happens they'll now fall back to a nicer placeholder and cross fade into their proper icons once available, thanks to [Italo](https://github.com/edwood-grant). We've changed the label of the action button for free apps from "Free" to "Install", according to your feedback. "Recent" apps in Category views should feature a more up-to-date selection and be a bit faster to load. And Search Results will now show in two columns when enough space is available so that you can see more results at once.

# Dock

When we ran our [desktop survey](https://blog.elementary.io/2021-ui-study-results-dock-multitasking/) 75% of you told us that you expected to see background apps in the Dock, so we now have Background Portal support in the Dock thanks to [Leonhard](https://github.com/leolost2605)! Here you can see a list of apps running the background without a window, their supplied reason for running the background, and you have the ability to force them to quit. You can always further manage app permissions in System Settings → Applications and choose which apps are allowed to run in the background.

New contributor [Sebastian](https://github.com/sebastianlay) fixed issues with the placement of app name tooltips, added a shake animation when you try to open a new window on a single-window app with middle-click, and fixed an issue where re-arranging app icons in the dock could cause them to shake indefinitely. [Leonhard](https://github.com/leolost2605) fixed an issue where maximized windows would be behind a portion of the dock when hiding is turned off. And [William](https://github.com/wpkelso) improved the color of the indicator dot for apps which are active on another workspace.

# Panel
Quick Settings:

PopoverWidget: notify when onboard activated in Wayland by @danirabbit in #120
DarkModeToggle: animate by @danirabbit in #121
RotationToggle: animate by @danirabbit in #122

Network:

Airplane mode disables networking radios, not bluetooth or wired networks
Jump to settings by middle-clicking on toggles

PopoverWidget: add stateful icons to Airplane Mode by @danirabbit in #338

Fix crash in greeter by @vjr in #342

rfkill: Use sizeof instead of literal size by @ryonakano in #349

# System Settings
Network:
RKFill: add airplane mode property by @danirabbit in #438

Applications:
Sidebar: use Action, search on type by @danirabbit in #251
DefaultPlug: add settings for geo uri handler by @danirabbit in #255

# Login &amp; Lock Screen

Add dark style support by @lenemter in #786
Use gsettings to store last user by @lenemter in #793
Move session action into application by @lenemter in #795
Fix popover keyboard nav by @lenemter in #797
Set power settings of active user by @lenemter in #801
Connect to lightdm daemon early by @lenemter in #802
Follow automatic accent color preference by @lenemter in #813
Save and restore last selected session type by @lenemter in #809
Center caps lock label by @lenemter in #798
Sync Wingpanel transparency by @lenemter in #788
Select classic session when using a11y features by @danirabbit in #821
Conf: set wayland as default session by @danirabbit in #747
Do not try to fallback to x11 session when it is unavailable by @bobby285271 in #824
Change manual card workflow by @lenemter in #794

---

# Files

The Properties Window now shows the exact date and time the file was last modified
PropertiesWindow: Use "iso" format for datetimes by @jeremypw in #2609

FileOperations: Re-escape uris from Clipboard or DNDHandler before use in fileoperations by @jeremypw in #2616

Do not unquote dropped and pasted uris from uri_list by @jeremypw in #2638

# Code

The terminal pane is now synchronized with the Terminal app foreground, background and palette settings
The terminal pane is now synchronized with GNOME font and cursor blink settings

Restart shell in terminal pane if it exits by @jeremypw in #1618
Rework terminal settings by @jeremypw in #1585

# Terminal

Only embedded newlines should trigger safe paste warning by @jeremypw in #906
MainWindow: set strict centering in header by @danirabbit in #909
Simplify make restorable by @jeremypw in #910
