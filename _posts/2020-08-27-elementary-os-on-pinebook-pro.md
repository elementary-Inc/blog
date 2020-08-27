---
title: elementary OS on Pinebook Pro
description: An experimental case of hardware enablement
author: davidmhewitt
image: /images/elementary-os-on-pinebook-pro/card.jpg
---

<figure class="constrained" markdown="1">
![Pinebook Pro]({{ page.image }}){: width="2048" height="1364"}
</figure>

In June, PINE64 reached out to see if elementary would be interested in experimenting with elementary OS on Pinebook Pro. We'd been loosely following PINE64 and the progress of Pinebook Pro, but hadn't gotten our hands on one—so we expressed our interest. PINE64 was gracious enough to send a few devices out to members of our team, and our work began.

First, a bit of a disclaimer: Pinebook Pro support is still considered an experiment for elementary OS, and it's not something we have committed to officially support indefinitely. That said, the experience so far has been a lot of fun, and we're happy with the current state. Second, this post isn't going to get into a lot of details about the hardware itself; for that, see [Cassidy's recent personal blog post](https://cassidyjames.com/blog/pinebook-pro/). Lastly, our work on bringing elementary OS to Pinebook Pro has been made possible by PINE64 generously providing the hardware as well as by funding from our [Early Access][builds] sponsors. If you'd like to see more projects like this, consider backing us on [GitHub Sponsors][sponsors].

## Bringing elementary OS to Pinebook Pro

The process of producing both functional and high-quality builds of elementary OS for Pinebook Pro has been long, but was made substantially easier thanks to help from PINE64 and the work of other projects.

### Kernel & Bootloader

Thanks to the great work that the Manjaro ARM team have done in this field, getting a working kernel for the Pinebook Pro was relatively painless. We've simply taken a mainline kernel straight from [kernel.org](https://kernel.org), applied a few patches copied from the Manjaro repository and used a config set similar to the Manjaro one. It needed tweaking slightly to be compatible with the way Ubuntu/elementary works.

For example, we've had to disable kernel module compression in the kernel config as this isn't compatible with the Ubuntu `update-initramfs` scripts yet.

Unfortunately, Ubuntu hasn't released any kernels that are new enough or contain the necessary tweaks, options and patches to run on the Pinebook Pro yet. So this is one major area where the Pinebook Pro builds differ from the regular Intel/AMD builds. You'll notice that we're using kernel 5.7.11 currently, though this is likely to be upgraded to 5.8 soon (as it allows dropping some more patches that have been mainlined).

elementary normally relies heavily on the fantastic work done by Canonical in testing and maintaining kernel releases. So maintaining our own kernel configuration and patchset is a bit of a departure from that. Ubuntu already releases [specific kernels for the Raspberry Pi](https://packages.ubuntu.com/focal/linux-raspi), perhaps we'll see a ready made Pinebook Pro one in the future. In the short term however, we may consider packaging the Pinebook Pro kernel into a .deb and hosting it on a PPA, so we can push updates in future if necessary. Currently the kernel is just built into the image at build time.

The bootloader is a similar story. We needed a version that was new enough to support the Pinebook Pro and a few patches, so this has come directly from mainline u-boot and not yet packaged as an upgradable .deb.

### Performance

Despite elementary OS being a relatively light distribution, performance still isn't as good as you would hope given the capability of the hardware. This is down to GTK3 largely not using GPU acceleration, especially when running on Xorg. There are a number of tweaks we've applied to improve the experience somewhat, though there won't be any big leaps in performance until we can move the stack to Wayland and to a greater extent GTK4.

One interesting point is that you can clearly notice the difference between the GPU accelerated animations (done by the Compositor) and those done largely on the CPU by GTK. For example, the `Alt+Tab` animation feels pretty smooth compared to the animation used when opening the applications menu. So the potential of the hardware is there, it's just unfortunate that the software isn't quite ready to take advantage yet.

The first tweak we applied was disabling the `ondemand` CPU governor which is forced on by default as a systemd unit on Ubuntu. This allows the kernel to use the `schedutil` governor which has been enabled and set as the default in our kernel config. The `schedutil` governor is a much newer governor with an awareness of the different performance/power utilisation levels of the big.LITTLE cores in the ARM CPU. Switching to this gave an immediate noticeable gain in performance.

Both `ondemand` and `schedutil` scale the frequency of the processor cores in response to load. However, if they aren't doing this efficiently or if the CPU has delays or slowdowns while it's switching frequency, you notice a bit of latency while the frequency picks up, then things feel a bit more speedy for a few seconds and then they slow down again.

We've opted to increase the minimum frequencies of both the CPU and GPU to reduce some of this sluggishness. This has the downside of reducing the battery life slightly. But given the already excellent battery life, we felt it was a reasonable trade-off.

If you wish to disable these frequency tweaks and have longer battery life but worse performance instead, you can comment out the lines in `/etc/tmpfiles.d/cpufreq.conf` and reboot.

### Keyboard and Trackpad Tweaks

We've applied 3 independent config tweaks to get the keyboard and trackpad functioning better under elementary OS.

The first is some UDev config originated from Manjaro to correctly map the sleep and brightness keys on the keyboard (`Fn+ESC`, `Fn+F1`, `Fn+F2`). Some similar config tweaks could be used to essential invert the Fn key (i.e. pressing the F1 key would turn the brightness down and Fn+F1 would function as F1). As this is not the intended layout of the keyboard, we likely won't apply this config by default, but we'll update this page with details of how to do so when ready.

The second tweak is some libinput config at `/etc/libinput/local-overrides.quirks`. This file tells libinput that the Pinebook keyboard is "internal", as it automatically assumes USB keyboards (the Pinebook Pro keyboard is on the USB bus) are external unless it is told otherwise. This has the effect of allowing libinput to "pair" the keyboard with the trackpad, meaning that when the "disable while typing" setting is enabled for the trackpad, it functions correctly. External keyboards do not disable the trackpad.

The final tweak at the bottom of `/etc/udev/hwdb.d/10-usb-kbd.hwdb` disables a device that the keyboard firmware reports as a "keyboard mouse". We assume that the keyboard firmware has some provision for a Trackpoint style mouse that doesn't physically exist on the keyboard, but the firmware still reports it. Having this device enabled resulted in the trackpad being disabled if you enabled the "disable when external mouse connected" option. The phantom "keyboard mouse" device was again assumed to be external, meaning `libinput` assumed you had an additional external mouse connected and that you didn't want the trackpad anymore.

It's possible that some/all of these tweaks are not necessary/useful on distributions that use the synaptics driver instead of `libinput` for the trackpad, but elementary OS uses `libinput` by default.

### Power Management

The biggest and most time consuming issue we came across while porting elementary OS to the Pinebook Pro was a sporadic issue with shutdown not powering off the device. Sometimes the power light would go off, but the device was still secretly on, draining battery and you had to hard reset by holding the power button and then powering on again. Other times the power light would flash red (indicating a kernel panic), and on occasion, it would shut down properly/normally.

Using a UART cable for debugging resulted in some kernel warnings about the i2c code for handling the shutdown call to the PMIC (Power Management Integrated Circuit) not being "atomic". This turned out to be an important hint, but it is a relatively normal message that you'll also see on other distributions using a similar kernel.

After much digging, it turned out that something in our stack pulls in a package called `irqbalance` by default. This distributes the hardware interrupts among the CPU cores to try and get better performance. The fact that the i2c code in the rockchip driver is not atomic means that it relies on interrupts to function.

During shutdown, the kernel disables interrupts on all but the first CPU core. The fact that `irqbalance` has potentially told a different core to handle the interrupts for the PMIC is the problem here. It also explains the random/sporadic behaviour. Removing the package was enough to fix the issue as the kernel has its own interrupt distribution code and is smart enough to ensure the interrupts are handled on the first core during shutdown.

A lot of ARM platforms handle power management functions like shutdown and suspend in a low level firmware interface called PSCI (Power State Coordination Interface). Instead of communicating directly with the PMIC chip like the current kernel in the Pinebook Pro image does, the kernel can communicate with the standardised PSCI API.

Unfortunately, these shutdown and suspend interfaces are not yet implemented in the open-source ARM TF-A (Trusted Firmware-A) meaning these functions have been implemented in the kernel in a non-standard way. This is understandable given the amount of work required to implement these functions in the low level firmware. Hopefully, when these features are implemented in the firmware, it should be possible to drop these non-standard patches and hopefully have improved suspend power draw levels.

A lot of manufacturers of ARM platforms offer a BSP (Board Support Package), which can include closed source firmware and a custom kernel (which is now a relatively out of date version). Rockchip offers a BSP firmware image and kernel where the suspend performance is improved, but we've opted for up to date and more easily auditable versions of these components.

## Run elementary OS on Pinebook Pro

In its current state, we would not consider elementary OS on Pinebook Pro as polished of an experience as running on well-supported Intel-based hardware.

That said, the audience for Pinebook Pro is substantially more technical and Linux-savvy than your average computer user; as such, we've decided to publish our experimental builds under our [Early Access builds][builds] program. This means dedicated [sponsors] of elementary OS who wish to run elementary OS on Pinebook Pro can download it from the same place as Early Access builds of elementary OS As a note, all of this work has been focused on bringing the **pre-release of elementary OS 6** to Pinebook Pro, so all the usual disclaimers about pre-release builds apply here as well.

<div style="text-align: center;" markdown="1">
[Pinebook Pro on the elementary OS Wiki][wiki]{: .button}
</div>

Once you have access to Early Access builds, head over to the [elementary OS wiki][wiki] to get it installed on your own hardware. If you find and file any issues, please remember to specify the build of the OS you downloaded as well as that you are running on Pinebook Pro—it will help us validate and triage issues much more quickly.

[builds]: https://builds.elementary.io
[sponsors]: https://github.com/sponsors/elementary
[wiki]: https://github.com/elementary/os/wiki/Pinebook-Pro
