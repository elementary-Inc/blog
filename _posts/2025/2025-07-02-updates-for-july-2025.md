---
title: Supporting Disability Is Our Social Responsibility
description: Updates for OS 8 and Early Access
author: danrabbit
image: /images/updates-for-july-2025/card.png

tags:
  - circe
  - updates
  - accessibility
  - earlyaccess
---

July is Disability Pride Month, an opportunity for us to consider how we're serving our disabled community and work on breaking down barriers to access. Last year we had the pleasure of being introduced to [Florian](https://www.twitch.tv/ic_null)—a fully blind cybersecurity enthusiast—and thanks to his feedback we completely rewrote navigation in Onboarding to be more keyboard and screen reader friendly, as well as took another look at Installation and Initial Setup to vastly improve our entire first run experience for blind folks. Plus, we implemented the screen reader interface in the <kbd>Alt</kbd> + <kbd>Tab</kbd> window switcher. Thanks to this feedback, elementary OS 8 can be installed and set up completely blind, an important win for maintaining your independence as a person with vision disabilities.

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "updates-for-july-2024" | first %}
{% include featured.html post=post %}
</div>

Since the release of OS 8 we've been working on things like improving contrast, support for Dark Mode screenshots and brand colors in AppCenter, turning on or snoozing Dark Mode without canceling your schedule, expanding the scope of the "Reduce Motion" setting, and adding more options to reduce distracting notification bubbles. Plus, thanks to feedback from [Aaron](https://github.com/aaron-gh) who you may know from [his blog series on Linux accessibility](https://fireborn.mataroa.blog/blog/i-want-to-love-linux-it-doesnt-love-me-back-post-1-built-for-control-but-not-for-people/), Notifications and the Shortcut Overlay both got releases that add screen reader support.

<figure markdown="1" class="card">
![Disability pride logo](/images/{{ page.slug }}/card.png)
</figure>

As a community that includes folks with a range of disabilities ourselves, we're deeply invested in improving access to Open Source software. We succeed at our mission when we build open computing experiences that are available regardless of ability and fail when accessibility is considered an afterthought or a nice-to-have. This month and always, Inclusive Design is at the core of what we do and we will continue to strive towards that ideal.

If you want to follow along or help us address accessibility issues in elementary OS, we'd love your help! We're tracking issues in [this GitHub project](https://github.com/orgs/elementary/projects/111). If you discover a new issue—accessibility related or otherwise—we'd love to get your feedback and we have a handy contributor guide to help you [file a report here](https://docs.elementary.io/contributor-guide/feedback/reporting-issues).

---

## Code

A big new release of Code is here, thanks primarily to [Jeremy](https://github.com/jeremypw). This release closes 19 reported issues including a couple of crashers. The "Open in…" menu is now sorted and includes an option for the Terminal pane. Plus the Terminal pane now follows Natural Copy/Paste settings from the Terminal app. The Vala symbols pane now shows a lot more information about symbols in their tooltips. Numbered lists are now handled correctly by the Markdown plugin. The Highlight Word Selection plugin now works with selections of more than one word. Several enhancements were made to managing git branches including sorting branch names alphabetically, the ability to switch to remote branches, and you'll now be asked how to handle uncommitted changes when switching branches. You can now create edit marks by clicking in the source view gutter. They can be jumped between via the context menu or with the keyboard shortcuts <kbd>Alt</kbd> + <kbd> ←</kbd> / <kbd>→</kbd>. If you're using the Flatpak version of Code on another OS, the "Open in…" menu is no longer empty and operations that require a network should now work. Plus performance was improved in several cases.

## Window Manager &amp; Dock

This month [Leonhard](https://github.com/leolost2605) and [Leo](https://github.com/lenemter) closed another 19 issue reports in our window manager, including several issues related to multi-monitor, the Multitasking View, and Dock behavior. A crash that could occur when closing LibreOffice windows was fixed. Picture-in-picture will now select the correctly window when its area selection is drawn over an app's shadow. Non-flatpak apps that don't correctly match their launchers can now sometimes be matched by the Dock anyways. If you have "activate hotcorners in fullscreen" turned on, you can also now access the Applications Menu with <kbd>Super</kbd> while playing a fullscreen game, for example. Plus we made some performance improvements to drawing shadows.

## System Settings

In Keyboard → Shortcuts → Custom you can now choose from a list of installed apps and their actions—in addition to being able to execute custom commands—thanks to [Leo](https://github.com/lenemter). This makes it super straightforward to add a keyboard shortcut for your most common workflows like composing a new email or adding a new Calendar event.

<figure markdown="1">
![Keyboard Settings](/images/{{ page.slug }}/settings-keyboard.png)
<figcaption markdown="1">
You can now create custom keyboard shortcuts for apps and their actions
</figcaption>
</figure>

System Settings will also now warn you if your desired keyboard shortcut conflicts with a common system shortcut like "Copy", "Paste", or "New Tab". Plus we fixed an issue that would prevent certain Housekeeping configurations from running, and the "Automatic" accent color option now works more reliably.

## And More

The Screencast Portal now features an improved design for selecting which display or window should be captured, as well as respecting options for capturing the pointer. Plus we fixed issues that prevented screenshots from including window shadows in some cases, and screenshot notifications now open the Image Viewer when clicked.

<figure markdown="1">
![Screencast Portal](/images/{{ page.slug }}/portal-screencast.png)
<figcaption markdown="1">
Screencasts portal has a new design
</figcaption>
</figure>

[Jeremy](https://github.com/jeremypw) fixed a number of issues in the latest release of Files including issues related to file renaming, drag-and-drop, ejecting removable drives, and an issue activating context menus from certain parts of the sidebar. And he also fixed an issue preventing bluetooth file sharing from working.

Plus, [Leo](https://github.com/lenemter) made sure that panel transparency and orientation lock settings get synced to the Login &amp; Lock screen.

## Get These Updates

As always, pop open System Settings → System on elementary OS 8 and hit "Update All" to get these updates plus your regular security, bug fix, and translation updates. Or set up automatic updates and get a notification when updates are ready to install!

---

# Early Access

Bluetooth Settings got a redesign and a reworking of its list sorting logic that should improve performance, reliability, and its screen reader experience. Especially of note, we now sort out more bluetooth devices so the list of nearby devices should be more concise and useful. Plus we fixed a few issues related to devices that require a passcode to pair, like some keyboards. This includes some fairly large changes so we could really use help testing for regressions before releasing this update for everyone.

<figure markdown="1">
![Bluetooth Settings](/images/{{ page.slug }}/settings-bluetooth.png){: width="849" height="603"}
<figcaption markdown="1">
Bluetooth settings has a new design
</figcaption>
</figure>

We're also now building daily ARM64 Native images thanks to new contributer [NN708](https://github.com/NN708). This is a universal ARM UEFI image, which means it should be a single image that runs on platforms like Raspberry Pi, Pinebook Pro, and Apple M-series Macs. This makes it a lot simpler for us to support ARM processors in future releasses of elementary OS. Please test these images on your ARM devices and report back! We now include additional processor architecture options in our issue report template to track any problems you experience.

<div style="text-align: center" markdown="1">
[Download ARM64 Builds](https://builds.elementary.io/downloads){: .button.suggested }
</div>

---

## Sponsors

At the moment we're at 23% of our monthly funding goal and 322 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
