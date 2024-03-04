---
title: GTK 4 Porting And A Bit Of Whimsy
description: OS 8 progress during February
author: danrabbit
image: /images/updates-for-march-2024/greeter.png

tags:
  - earlyaccess
  - updates
---

I want to start off this post by saying, "Thank you!" to our now over 250 sponsors on GitHub for helping us reach 20% of our monthly funding goal! I've been seeing a ton of demand for Early Access which is super exciting. If you're not already in Early Access, you can be among the first to try the next release of elementary OS and give us your feedback by sponsoring elementary [for as little as $1/mo](https://builds.elementary.io/). Beware that Early Access builds are not considered stable and you will encounter fresh issues when you run them. We'd really appreciate reporting any problems you encounter with the Feedback app or directly [on GitHub](Github.com/elementary). With that, let's talk about what we accomplished in the last month!

## System Settings

The GTK 4 port of System Settings is now almost complete! We merged ports for Display, Network, and Printer settings during the last month. Display settings received a big update to the way we do arranging and snapping which should be much smoother and more reliable with 3 displays thanks to [Jeremy](https://github.com/jeremypw). [Leonhard](https://github.com/leolost2605) made sure that the colored display labels you see in the corner while arranging displays are now created in a Wayland-compitable way. Plus we've improved CSS styling here for higher contrast.

<figure markdown="1">
![Power Settings](/images/{{ page.slug }}/settings-power.png) {: width="678" height="901"}
<figcaption markdown="1">
System Settings → Power has new options and shows battery charge status
</figcaption>
</figure>

Power settings now shows charging level and status for internal batteries and theoretically supports multiple internal batteries—though I'm not sure that's been tested so please send feedback if you have a device with multiple internal batteries. You can also now choose to automatically set different power profiles based on whether your device is plugged in or on battery power thanks to [Leo](https://github.com/lenemter). We've cleaned up some old code here quite a bit along the way and solved some issues with system hangs while getting permission for lid close settings. I'm excited to continue iterating here and hopefully have more new features to announce to you next month!

I want to give a special thanks to [Micah](https://github.com/micahilbery) for donating a Wacom tablet so that I can do the port of Wacom settings. I received it near the end of the month so I've only made a preliminary port so far, but I'm feeling confident about being able to finish it quickly! We're also closing in on a much larger redesign of System Settings in general, so hang tight for news on that. The new GTK 4 System Settings is almost ready to go!

## The Desktop

The Login &amp; Lock Screen now features a blurred background similar to the Multitasking View, thanks to [Leo](https://github.com/lenemter). A number of improvements have landed for our Window Manager when running under Wayland as well as keeping up with the latest changes in the upstream Mutter library that it uses. And we've landed basic support for the Wallpaper Portal which means you can grant access to apps to change your wallpaper in a platform agnostic way as opposed to the platform-specific way we had implemented before.

<figure class="card" markdown="1">
![Login &amp; Lock Screen](/images/{{ page.slug }}/greeter.png)
<figcaption>The Login &amp; Lock Screen now shows a blurred version of your wallpaper in the background</figcaption>
</figure>

We also landed launcher animations in the new Dock. It's worth mentioning again that this is a fully GTK 4 application and not custom drawing! Animations are done with GTK transforms and timed with Adwaita.Animation

<figure class="card">
    <video width="842" height="194" autoplay="true" loop="true" playsinline="true" muted="true">
        <source src="/images/updates-for-march-2024/dock.webm" type="video/webm">
        <source src="/images/updates-for-march-2024/dock.mp4" type="video/mp4">
    </video>
    <figcaption>Launcher animations in the new Dock</figcaption>
</figure>

### And More

The GTK 4 port of AppCenter has landed which brings with it a number of small fixes and performance improvements. Since OS Updates are now handled in System Settings, we've also removed that functionality from AppCenter which greatly improves performance and has enabled us to really simplify some of the backend code here. Plus, you can now opt-in to automatic OS updates during Onboarding and automatic App updates are now opt-out.

---

# Updates for OS 7

Some minor bug fix updates for GNOME Web and Document viewer were released upstream and those are available to you now.

We're also [tracking an issue](https://github.com/elementary/browser/issues/125) where some folks are not seeing any content appearing in Web. We're working on a proper solution for this, but if you're experiencing this issue it can be solved by manually installing the latest version of the Freedesktop GL Platform. We normally would not recommend copying and pasting Terminal commands you read on the internet, but the only way to do this manually is via Terminal with the following commands:

```bash
flatpak install --system freedesktop org.freedesktop.Platform.GL.default//23.08{,-extra}
flatpak pin --remove runtime/org.freedesktop.Platform.GL.default/x86_64/23.08
flatpak pin --remove runtime/org.freedesktop.Platform.GL.default/x86_64/23.08-extra
```

The first command installs the missing Freedesktop GL Platform in the required version. The next two commands make sure that when this platform is no longer being used, it will be automatically uninstalled. If you're not experiencing this issue, you don't need to do anything and the above commands will have no effect. Apologies for the inconvenience!


## Get These Updates

As always, pop open AppCenter on elementary OS 7 and hit "Update All" to get your regular security, bug fix, and translation updates.
