---
title: Surprise! Big Updates for OS 7 Are Here!
description: And a progress update on OS 8
author: danrabbit
image: /images/updates-for-august-2024/videos.png

tags:
  - earlyaccess
  - horus
  - updates
---

This month we have a bunch of surprise updates for OS 7 and as always a progress update on OS 8. We're getting very close to releasing the latest version of our operating system and that means releasing new versions of all of the projects we maintain! That means big new versions of apps and new platform features, some of which we're also able to release as an update for OS 7.

## Community

Just a little follow up on our Discord community: we're now just over 550 members! It's quickly becoming a great place to ask questions and get help, share ideas, and generally hang out and chat with other people who use elementary OS or run Pantheon on other Linux distributions. It's been really fun to watch this server grow and I'm really excited to participate more in a much less formal way with our community.

<div style="text-align: center" markdown="1">
[Join us on Discord](https://discord.com/invite/kwRyqGCzm5){: .button.suggested }
</div>

# OS 7 Updates

While most of the releases going out at the moment are exclusive to OS 8, there were still a number of significant updates that we were able to release for OS 7! This is in large part due to shipping many of our apps as Flatpak packages, but it also includes a sneaky platform update that you might not even know you needed.

## Videos

<figure class="half" markdown="1">
![Videos player view](/images/{{ page.slug }}/videos.png){: width="1045" height="605"}
![Videos library view](/images/{{ page.slug }}/videos-library.png){: width="1045" height="605"}
<figcaption>Videos has a new modern and minimalist design</figcaption>
</figure>

Videos now sports a more modern and minimal design which is especially apparent on the player page. On the library page it uses larger landscape format thumbnails and the app now follows the system light and dark style preference. The upgrade to GTK4 also brings performance improvements. Major shoutouts to [Leonhard](https://github.com/leolost2605) for his work modernizing this code base.

Videos—like all of our Flatpak apps—is of course also available to download as a Flatpak for folks running Linux distros other than elementary OS:

<div style="text-align: center" markdown="1">
[Download Videos as Flatpak](https://appcenter.elementary.io/io.elementary.videos/){: .button.suggested }
</div>

## Developer Tools

Code now uses the LibHandy tab bar widget which brings improved animations and drag-n-drop behavior. The Terminal pane can now open to your preference of project subdirectory by default. The preferences dialog was slightly redesigned to fit more modern platform conventions and improve screen reader compatibility. And we fixed a dozen reported issues!

There's a new setting in Terminal for event alerts on invalid input and we now do a better job saving tab state. Plus man page documentation has been improved.

Restoring tabs from last time is now optional in Files and it now supports hiding files and folders via a `.hidden` file, a feature you may be familiar with from other file manager apps.

Special thanks go to [Colin](https://github.com/colinkiama), [Gustavo](https://github.com/marukesu), and [Jeremy](https://github.com/jeremypw) for working on our developer tools.

## Portals

Portals are special API that apps can use to access system features in a way that respects your privacy and requires your explicit consent. Three new Portals are now supported in OS 7: Color Picker, Screenshot, and Screencast. These portals are essential for maintaining compatibility with modern apps which are written to work in a Wayland world and don't have direct access to the pixels on your display. If you've previously experienced trouble using modern color picker or screen recording apps from alt stores like Flathub on elementary OS 7, this update should fix that for you! Thanks to [David](https://github.com/davidmhewitt)and [Leonhard](https://github.com/leolost2605) for their work here!

## And More

Music can now open individual audio files from within the app instead of requiring you to open them from within Files and it gains the now-familiar sticky toolbar style when scrolling in the queue. Camera has been updated to use GTK4 which for now simply means improved performance. And a new Tasks release fixes an issue where it would crash when the system style was changed from light to dark.

---

# OS 8 Updates

We've landed a rename of the session options on the Lock Screen to hopefully improve clarity for folks that aren't sure if they should be using a Wayland or X11 session. The X11 session is now called the "Compatibility Session" since it offers improved compatibility with legacy apps and some accessibility tools. The Wayland session is now called the "Secure Session" since it requires apps to use modern APIs that improve your security and respect your privacy. There was a lot of back-and-forth discussion about the best way to concisely describe these sessions in a non-technical way—we're aware these descriptions are not perfect—and we think that for now this the best way to sum up the trade offs when selecting a session. In the future this may change as new features may rely on Wayland and the performance benefits of Wayland become more distinct. But for now we want to make sure that folks who rely on the X11 session for certain workflows aren't being discouraged by a word choice that doesn't reflect their reality.

And speaking of the compatibility session—pending approval of a new window manager protocol—we will be able to ship the new Dock in both the Secure and Compatibility sessions in OS 8. This is particularly great news since the new Dock offers a much better multitasking workflow based on the feedback we gathered in our survey; For those times you may need to switch back to the Compatibility session for certain apps you won't need to manage disparate dock settings.

<figure markdown="1">
![Onboarding](/images/{{ page.slug }}/onboarding.png){: width="497" height="438"}
<figcaption markdown="1">
Navigation in Onboarding has been rewritten for improved accessibility and with a neat progress bar
</figcaption>
</figure>

On the heels of some of our recent accessibility work, I'm proud to say that navigation in Onboarding has been rewritten for much improved keyboard navigation and screen reader compatibility. This was a show stopper when [Florian](https://www.twitch.tv/ic_null) took [a look at OS 8 in June](https://www.youtube.com/watch?v=7jOB4lZH3AE). Onboarding is such an important part of introducing a new operating system and making sure people new to elementary OS have a great time, so I'm particularly glad to improve this first impression for folks with vision-related disabilities.

The Bluetooth Daemon was previously shipped in the same package as the Bluetooth Indicator and it now lives in its own separate package and has its own project. This should both make it clearer which components are responsible for which parts of Bluetooth features on elementary OS and make things a bit easier to maintain. For now features remain completely unchanged and this is purely organizational.

We're also now shipping Font Viewer as a Flatpak app. Previously we had packaged it and released it to AppCenter, but it is now pulled into OS 8 daily by default. This means we can continually ship the latest GNOME Font Viewer in elementary OS built against our Flatpak runtime so that it fits in stylistically.


## Release Planning

Nearly everything is now released in the OS 8 stable repository, which means we're very close to building stable release candidate quality builds for OS 8 in Early Access. At the moment we're mainly waiting on the new Window Manager protocol for the Dock in the compatibility session which will unblock releases for the Dock and Panel.

As always you can follow along with our progress towards the release of OS 8 in [this GitHub project](https://github.com/orgs/elementary/projects/128/views/1). At this rate we may be looking at a September release of OS 8 if everything goes smoothly; keep your fingers crossed!

---

## Sponsors

At the moment we're just above 21% of our monthly funding goal and we're at 382 Sponsors on GitHub! Shoutouts to everyone helping us reach our goals here. Your monthly sponsorship funds development and makes sure we have the resources we need to give you the best version of elementary OS we can!

Monthly release candidate builds and daily Early Access builds are available to [GitHub Sponsors](https://github.com/sponsors/elementary) from any tier! Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](https://Github.com/elementary).
