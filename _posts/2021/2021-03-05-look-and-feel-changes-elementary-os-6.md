---
title: Look & Feel Changes Coming to elementary OS 6
description: Visual design updates that are more than skin deep
author: danrabbit
image:
tags:
  - devices
  - ux
---

Oftentimes when a new major version of some piece of software is released, there is an immediate focus put on visual changes. If there aren't a ton of new and shinies, social media will inevitably be filled with words like "stale", "old", and "outdated". This had become especially true for elementary OS, whose visual design hasn't really changed all that much over the years. At elementary, we tend to avoid making changes for the sake of change. We're very skeptical about design trends, and do our best to create things that feel a bit more "evergreen". After all, "Good design is long lasting" and this allows us to focus more on refining than constantly reinventing. We also have a 3rd party developer community to think about, and making sweeping visual changes means that the nearly 200 apps in AppCenter will have to be updated and tested to make sure they still look as intended. So, when we decided to work on the look and feel for elementary OS 6, we wanted to approach things with a lot of intentionality, avoiding trends and focusing on setting the stage for the next several years.

## Toolkit & Libraries

App developers rely on pre-made widgets to do a lot of the heavy lifting and provide good default styles when making their apps. In addition to the widgets provided by Gtk, we also ship our Gtk companion library Granite that makes replicating common elementary design patterns a breeze. In elementary OS 6, we're also making heavy use of Handy, the library originally developed by Purism for mobile interfaces. Thanks to Handy, we have two major, obvious visual design improvements that developers can adopt.

We've long had plans to modernize the Granite Avatar widget. A continual problem we've faced is that many people just don't set avatars. As a consequence, we need a more meaningful fallback design that allows avatars to be distinct and useful in apps like Mail or in System Settings. As it turns out, the folks behind Handy had the same thoughts and the work was largely already done. Alex was very helpful and gracious in implementing changes in Handy to acheive the exact style we wanted, and I'm happy to say that we now have much more colorful interfaces in elementary OS 6 thanks to Hdy.Avatar, even if people don't set avatar images.

The other obvious change is more rounded bottom window corners. This seems like something that would be simple, but is actually not possible in vanilla Gtk3. In elementary OS 5, we used clever workarounds for specific cases to give dialogs and other flat windows rounded corners all the way around. But in elementary OS 6, we can now have rounded bottom corners even in complex cases like Camera, thanks to Hdy.Window. It's a small thing, but it definitely makes the whole UI feel just a bit more polished.

## Typography

We've also changed up the default typeface in elementary OS. Instead of Open Sans, we're using Inter: a new, modern typeface specifically designed for use in user interfaces on computer screens. The designer, Rasmus Andersson, actively updates Inter and has been very responsive on GitHub. He's even weighed in on our use of Inter in elementary OS, and his feedback has led to changes in the weights we use for various headers. You'll find that in general, text is bolder and higher contrast in elementary OS 6.

https://rsms.me/inter/

## Iconography

The visual style for our icons has remained largely unchanged, with more focus put on internal consistency. You'll notice subtle improvements such as the more gender nuetral user accounts icon in System Settings.

A long outstanding issue has been wrangling all the different styles of arrows that we've used over the years. There are hundreds of arrow icons in the elementary icon set, used across many different contexts. We provide both full color and flat, symbolic icons and in a range of different sizes. There are even different kinds of arrows tails depending on context, or no tail at all. In elementary OS 6, we have one new shape to rule them all and we've given arrows more rounded corners.

In arrows with curved tails, such as in Mail tool icons, the area under the curve is larger, making the shape more recognizeable at small sizes or for folks with less acute vision. We've also reduced busy overlap and improved separation in symbolic icons, which now match their full color counterparts much more closely.

We're rounding out corners and using bolder shapes in other places as well. The new media controls icons for example feel much more weighty, and the lightning bolt symbol used on power icons is more distinct.

## Stylesheet

Brand new from scratch using Sass instead of CSS.

A recurring bit of feedback we received is that the style sheet is too low contrast. Important not just for visually impaired users, but also users with lower quality displays. Widgets can be mixed and matched. How to ensure contrast? Potentially very complicated and requires lots of testing. Make it simple by always using levels for background color. Sass superpowers to apply depth. End result is overall a bit flatter, but more shadows. Shadows also have levels.

UIs are interactive. Must design for states. Active. Selected. Disabled. Focused. Started some work on these states with checkboxes in OS 5. In OS 6, all disabled widgets are darker than the default UI level. Very obvious. Disabled elements intentially lower contrast as per WCAG. Focus styles still a work in progress, but bold use of color. More obvious. Selection styles and suggested action styles, no longer white on color. Dark color on light color is higher contrast, better for custom brand colors. Less in your face. Works other places where we want to use color like Calendar events.

Dark style follows all the same principles: contrast, levels, etc.

Accent colors. Make elementary OS feel more personal. Combined with dark style, can get a much more unique look without breaking app styles. Still exploring more ways to expose accent colors in the UI.

Scalability. No fractional scaling, instead a much more native way to scale the UI. Make elementary OS more legible with more resolutions. Try to eliminate awkwardness with spacing when using larger or smaller text. People who need larger text, more first class experience.
