---
title: 
description: 
author: danrabbit
image: /images/updates-for-july-2024/settings-system.png

tags:
  - earlyaccess
  - horus
  - updates
---


## Community

Just a little follow up on our Discord community: we're now just over 550 members! It's quickly becoming a great place to ask questions and get help, share ideas, and generally hang out and chat with other people who use elementary OS or run Pantheon on other Linux distributions.

<div style="text-align: center" markdown="1">
[Join us on Discord](https://discord.com/invite/kwRyqGCzm5){: .button.suggested }
</div>

# OS 7 Updates

While most of the releases going out at the moment are exclusive to OS 8, there were still a number of significant updates that we were able to release for OS 7!

## Videos

A new more modern and minimal design
Now follows the dark style preference
Support repeat one and repeat all
Performance improvements
Drop support for optical media

## Code
The Terminal pane now has a settable default directory

Redesigned preferences dialog with improved screen reader compatibility

New Tab Bar with improved animations and Drag-n-Drop

A dozen reported issues fixed

## Terminal

Allow switching event alerts on and off in the app menu
Save tabs and zooms to the saved state settings when they change

Document missing options in the man page
Suppress unwanted default tab when opening a new window

## Files

Restoring tabs from last time is now optional
Drag and select can no longer be done with secondary pointer button

Supports `.hidden` file

## And More

Three new Portals are now supported in OS 7: Color Picker, Screenshot, and Screencast. These portals are essential for maintaining compatibility with modern apps which are written to work in a Wayland world and don't have direct access to the pixels on your display—preserving your privacy and requiring your explicit consent. If you've previously experienced trouble using modern color picker or screen recording apps on elementary OS 7, this update should fix that for you!

Music can now open individual audio files from within the app instead of requiring you to open them from within Files. And it gains the now-familiar sticky toolbar style when scrolling in the queue. Camera has been updated to use GTK4 which for now simply means improved performance. And a new Tasks release fixes an issue where it would crash when the system style was changed from light to dark.

---

# OS 8 Updates

We've landed a rename of the session options on the Lock Screen to hopefully improve clarity for folks that aren't sure if they should be using a Wayland or X11 session. The X11 session is now called the "Compatibility Session" since it offers improved compatibility with legacy apps and some accessibility tools. The Wayland session is now called the "Secure Session" since it requires apps to use modern APIs that improve your security and respect your privacy. There was a lot of back-and-forth discussion about the best way to concisely describe these sessions in a non-technical way—we're aware these descriptions are not perfect—and we think that for now this the best way to sum up the trade offs when selecting a session. In the future this may change as new features may rely on Wayland and the performance benefits of Wayland become more distinct. But for now we want to make sure that folks who rely on the X11 session for certain workflows aren't being discouraged by a word choice that doesn't reflect their reality.

And speaking of the compatibility session—pending approval of a new window manager protocol—we will be able to ship the new Dock in both the Secure and Compatibility sessions in OS 8. This is particularly great news since the new Dock offers a much better multitasking workflow based on the feedback we gathered in our survey and for those times you may need to switch back to the Compatibility session for certain apps you won't need to manage disparate dock settings.

On the heels of some of our recent accessibility work, I'm proud to say that navigation in Onboarding has been rewritten for much improved keyboard navigation and screen reader compatibility. This was a show stopper when [Florian](https://www.twitch.tv/ic_null) took [a look at OS 8 in June](https://www.youtube.com/watch?v=7jOB4lZH3AE). Onboarding is such an important part of introducing a new operating system and making sure people new to elementary OS have a great time, so I'm particularly glad to improve this first impression for folks with vision-related disabilities.

The Bluetooth Daemon was previously shipped in the same package as the Bluetooth Indicator and it now lives in its own separate package and has its own project. This should both make it clearer which components are responsible for which parts of Bluetooth features on elementary OS and make things a bit easier to maintain. For now features remain completely unchanged and this is purely organizational.

We're also now shipping Font Viewer as a Flatpak app. Previously we had packaged it and released it to AppCenter, but it is now pulled into OS 8 daily by default. This means we can continually ship the latest GNOME Font Viewer in elementary OS built against our Flatpak runtime so that it fits in stylistically.


## Release Planning

Nearly everything is now released in the OS 8 stable repository, which means we're very close to building stable release candidate quality builds for OS 8 in Early Access. At the moment we're mainly waiting on the new Window Manager protocol for the Dock in the compatibility session which will unblock releases for the Dock and Panel.

As always you can follow along with our progress towards the release of OS 8 in [this GitHub project](https://github.com/orgs/elementary/projects/128/views/1). Hang tight, we're almost there!

---

## Sponsors

At the moment we're just above 21% of our monthly funding goal and we're at 365 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

We're also now automatically building monthly release candidate quality stable builds! These builds are created on the 1st of every month and include all stable updates for the current stable OS series. They have not been reviewed by a human, but should usually be of high quality. Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier!

Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
