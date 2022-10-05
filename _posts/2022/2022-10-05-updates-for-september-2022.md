---
title: Updates for September, 2022
description: A new developer tool and steady OS 7 progress
author: danrabbit
image: /images/updates-for-september-2022/iconbrowser.png

tags:
  - horus
---

Sorry 6.1 fans, this month was all about OS 7 with the exception of a new Icon Browser app being released in AppCenter.

<figure markdown="1">
![elementary Icon Browser](/images/updates-for-september-2022/iconbrowser.png){: width="1034" height="710"}
<figcaption markdown="1">
The new elementary Icon Browser available in AppCenter
</figcaption>
</figure>

If you're familiar with my LookBook app which was previously offered for $10, you may be excited to know that the new elementary Icon Browser is available for free. This developer tool shows you all of the system icons available to use in your apps and you can even search them by description. The new app has been updated to use Gtk 4 and has much better system dark style support as well as doing a better job showing relevant icon sizes and more. If you're writing apps for elementary OS, be sure to check it out!

---

<figure class="constrained card" markdown="1">
![elementary OS 7 Horus](/images/updates-for-april-2022/card.jpg)
</figure>

## Multitasking & Window Management

If you're following the release closely, you may be aware the the primary release blockers for the last several months have been some serious regressions in Gala, our window manager. I'm happy to report that several of these regressions have now been solved and there is only one known release blocking issue for Gala left. Major shoutouts to Corentin and David for their work here. This brings us much much closer to the stable release of OS 7. As always, you can follow along with remaining release targeted issues on the [OS 7 Project Board](https://github.com/orgs/elementary/projects/94/views/1).

## AppCenter

AppCenter continues to get new features and plenty of fixes in preparation for quite a large new release!

You can now see the release notes of up to 5 past releases on app info pages to get a clearer idea of how often an app is updated. Plus, we now support the `<issues>` tag so that developers can provide links back to solved issues that you've reported. We're hoping this encourages folks to get involved as part of the open source community for their favorite apps.

<figure markdown="1">
![Improved AppCenter Release Notes](/images/updates-for-september-2022/release-notes.png)
<figcaption markdown="1">
Improved release notes in AppCenter with linked issue reports
</figcaption>
</figure>

There's now an overlay status bar showing a description of currently in progress tasks. This replaces the mysterious spinner that previously appeared in the header bar. And in the updates view, the "Update All" header is now sticky to the view, making its action always easily accessible.

<figure markdown="1">
![AppCenter Updates View](/images/updates-for-september-2022/updates.png)
<figcaption markdown="1">
AppCenter with a overlay status bar and a sticky updates header
</figcaption>
</figure>

Also, shoutouts to [Michael Murphy](https://github.com/mmstick) from System76 for upstreaming a fix for a crash that would occur when showing error messages. In addition to several other under the hood improvements, the next release of AppCenter will certainly be much more stable. One final thing, though it hasn't been approved yet, the Gtk 4 port of AppCenter is ready for review! So we can hopefully look forward to a big performance boost once that lands as well.

## GitHub & CI

Still important, but probably less interesting for you, Corentin also spent some time resolving some issues we were having with GitHub Actions and our continuous integration testing process. We're now building some new Docker containers specifically for OS 7 and have a resolved an issue that caused build failures for any projects making use of GResource—which is quite a few. Our Gettext action has also been updated so that translation templates are always kept up to date and translators are able to quickly and automatically do their work via Weblate. These handy automations help us to do our work quickly while ensuring large breaking changes don't get into our code.

## Early Access Preview

If you're in early access, you now have the ability to install and test the very early Gtk 4 port of System Settings. To get the new System Settings, pop open Terminal and enter `sudo apt install io.elementary.settings*`. This will install the new System Settings app itself as well as the 7 panes currently available to test. Note that you may not experience too much different here just yet and there will be plenty of issues to sort through.

If you're not already in early access, you can be among the first to try it and give your feedback by joining [Early Access for a $10/mo sponsorship](https://builds.elementary.io/). Can't wait to see you in the next one!
