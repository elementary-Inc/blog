---
title:  "Juno Updates for July, 2019"
---

## Look and Feel

Lastly, we improved the look and feel of elementary OS via the [system stylesheet](https://github.com/elementary/stylesheet/releases/tag/5.2.5) and [icons](https://github.com/elementary/icons/releases/tag/5.0.4).

We added a subtle fade-out effect to the start and end of lists in popovers, like the list of Wi-Fi networks in the Networking indicator. Keycaps in menus now have a flatter style, which will come into play as we add keycaps in menus in future updates. Progress and loading states on entries (like the address bar of browsers when a page is loading) has been made more subtle. Lastly, the system stylesheet now supports the floating-bar widget used in newer versions of Epiphany.

The most immediate icon change is the newly redesigned wired networking icons, visible if your device has Ethernet or another wired network. In the panel, the new icon is simpler and clearer—instead of the complex and hard-to-align [ISO IEC-60417-5988 "Computer network" symbol](https://www.iso.org/obp/ui#iec:grs:60417:5988), we use a simpler metaphor that has been adopted by other platforms like Android and macOS. While the ISO symbol technically represents _any_ wired network, it has become overwhelmingly associated with Ethernet connections; since we also use this symbol for USB network connections, we feel the new symbol works better. It's also easier to add states to it like "connecting" or "disconnected." We also took the opportunity to align the full-color and symbolic versions of the icons: instead of an Ethernet jack for the full-color version, we use the new symbol on an orange tile.


- Redesigned wired networking icons
- Simplified image-missing
- Re-shaped system-software-update
- Scaled process-completed to 64px
- Scaled find-location to 64px
- Added new icons:
  - preferences-system-privacy-housekeeping
  - media-memory-symbolic
  - mail-forwarded-symbolic
  - application-x-firmware-symbolic
  - computer-laptop-symbolic
  - location-active-symbolic
  - location-inactive-symbolic
  - location-disabled-symbolic
  - 64px night-light
  - 48px image-crop
  - 48px mail-send

