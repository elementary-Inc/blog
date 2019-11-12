---
title: Accessibility Features Are Just Features
description: An OS-wide curb-cutting effort
date: '2019-02-16T19:54:18.288Z'
author: cassidyjames
image: https://cdn-images-1.medium.com/max/1600/0*3Q6Snc6Qga_HsPK7
tags:
  - accessibility
  - ux
---

<figure markdown="1">
![Photo of an accessible curb cut](https://cdn-images-1.medium.com/max/1600/0*3Q6Snc6Qga_HsPK7)
<figcaption markdown="1">
Photo of an accessible curb cut by [Dane Deaner](https://unsplash.com/@danedeaner) on [Unsplash](https://unsplash.com)
</figcaption>
</figure>

For some time now, Daniel and I have been talking about how accessibility features really ought to just be standard features of the desktop. Much like [curb cuts](https://99percentinvisible.org/episode/curb-cuts/)—the slopes on sidewalks designed to make traversal with a wheelchair possible—many “accessibility” features can be used to improve the experiences of everyone, regardless of any specific ability or impairment. In addition, the ubiquitous nature of these features can greatly destigmatize their use.

For full disclosure, I am not personally an accessibility expert; in elementary OS and the broader open source world we lean heavily both on conventions and expert research that has been published by others.

## Examples from Other Platforms

Mobile OSes have been incredibly successful in integrating accessibility features into the daily lives of millions and potentially billions of users. Features that have been subpar without extremely specialized tools on the desktop have become common place.

### On-Screen Keyboard

The most obvious one for touchscreen devices is the on-screen keyboard. On the desktop, this can be considered an accessibility feature that is used by people who may have some sort of pointer input to control a mouse cursor, but not the motor capabilities to type on a traditional keyboard. To these users, this is an accessibility feature that accounts for their physical differences.

However, on-screen keyboards have also become important for hardware accessibility—that is, the software being more accessible to users with different hardware form factors. Install GNOME or elementary OS on a tablet, and you're going to need to type something eventually. An on-screen keyboard lets the software be more compatible with this hardware.

#### Speech

Another example is speech input and output in mobile OSes and smart home devices. Traditionally, speech input had been designed for people who were unable to or unwilling to type into their computer. On the desktop, dictation software promised to allow you to write a document without touching the keyboard. Some software was even designed to let you use the entire computer without using the keyboard or mouse. On the flip side, text-to-speech or screen reading has been around for a long time, but has been generally lacking on desktop platforms without expensive, specialized software.

But mobile OSes really took both of these features to another level. On Android today, anywhere you can type with a keyboard, you can speak. Voice input is built into the keyboard itself, meaning if you don't have the fine motor control to tap away at tiny virtual keycaps, you can still send messages to people, perform Internet searches, etc. This is an incredible accessibility feature!

But it's not just helpful for folks who have a permanent physical difference that means they can't use a keyboard. For a new dad who is trying to wrangle his daughter while still staying in contact with the outside world, the ability to use my voice to control and input text into my device instead of using my very full hands is a godsend. “Hey Google… (Hey Siri… Alexa… Mycroft…) what's the weather?” might be way more convenient in the morning before I've put my contacts in and fully woken up than finding a gadget, unlocking it, opening up a weather app, etc. My mother-in-law who is perfectly _capable_ of typing into a phone keyboard greatly prefers speech input for longer messages because to her, it's just more natural and faster to speak.

Both speech input and output are major features individually, and are both extremely difficult problems. But they're perfect examples of compelling features that have huge accessibility benefits as well as being genuinely useful to a wide variety of people—regardless of them thinking of themselves as “disabled” or in need of an “accessibility" feature.

## Captioning

Closed captioning as you see on a television has been around since the 1970s, and has become required by law in some countries as part of anti-discrimination legislation. What's interesting is that captions have been adopted widely by people who are not hard of hearing; for example, captions have become standard features both for second-language learners and for public spaces that don't want extra noise polution.

More recently, Android has implemented system-wide live captions that do all sorts of magic on-device machine learning to caption videos, audio, and even live speech in realtime. This is incredible for so many situations like, yes, those who are hard of hearing, but also those watching a video with speech in a quiet environment.

## It's a Mindset

While the examples I've provided so far are major features—and individually would take a ton of effort to implement, this idea of "accessibility features are just features" is really a mindset that should be applied throughout the design of experiences of both platforms and apps. We've recently been talking about how a dark style preference is useful from both a traditional accessibility perspective as well as improving the experiences of almost everyone in certain situations.

In elementary OS, we used to have a concept in the HIG called "Minimal Configuration," the idea being that apps and the OS should be as minimally configurable as possible to reduce complexity—both of development and use. However, taken to an extreme, minimalism is excluding certain classes of users. Instead, we've shifted to a concept of "Accessible Configuration," focusing on offering configuration or customization when it can serve an accessibility or hardware need. And by catering to these accessible needs, it makes the product more useful to everyone.

<!-- TODO: more theoreticals/examples? -->

For example, while it's perfectly sane to prefer a certain font in your app as part of its branding, understand how that affects people who might have dyslexia. Perhaps offer a few font options, or offer an option to use the system font—especially if the user can already configure the system font to be more accomadating to their needs.

For a podcast app, it might seem crazy to you that someone would want to slow down speech and take longer to listen to a podcast, but consider how it could benefit someone with a learning disability, or someone listening to a podcast in a non-native language. Or just how it could help anyone when listening to a podcast of a particularly fast speaker.

If you're going to offer these more accessible options, make sure you test against them. And if they're well-supported and well-tested options, why bury them in some accessibility menu? Bring them more in line with where users would expect, and you might be surprised by how many everyday users find them useful.

## In elementary OS

We are approaching this concept in elementary OS through [a new organization-wide effort](https://github.com/orgs/elementary/projects/35) to better support these features. A major part of this effort is reorganizing several Universal Access (or accessibility) settings into standard System Settings panes—if they’re exposed in Universal Access settings, it means we must support them in order for the desktop to be usable to those users, so why not make them more discoverable for all?

Something we’ve also heard is that users don’t go looking in Universal Access for these types of settings, because they don’t feel that they have a disability (even though Universal Access is explicitly _not_ titled “features for disabilities”). By reorganizing these settings into the standard, natural System Settings locations, we hope that everyone can benefit with more features and options to help them better use their computer. Consequently, settings and preferences that can be useful to a wide range of users will be both easier to find and better supported. We’ve already begun in a few small areas.

### Appearance Settings

We’ve added a new Appearance tab in the Desktop settings to expose window animations, panel translucency, and text size.

![Desktop Appearance settings](https://cdn-images-1.medium.com/max/1600/1*EyErGVV6till1aap3FMPYA@2x.png)

These were all supported Universal Access features before, but now they’re much more obvious. Plus, we’ve improved text size by offering a wider range than the Universal Access options. Whether you have a vision impairment, a display resolution that’s a bit high or low for its physical size, or just like your text smaller or larger, you now have more control.

### Sound Settings

We also expanded on the “Event sounds” toggle in Sound settings.

![Sound output settings](https://cdn-images-1.medium.com/max/1600/1*3gQ7yzFaH5xGNjz8QpvgLQ.png)

We’ve added a new “Flash screen” checkbox alongside, plus we added descriptive text to make it more clear what these settings do. Now if you are hard of hearing, don’t have speakers, or are using your computer in an environment where sounds are not appropriate, you have more accessible control over what happens with event alerts.

### Mouse & Touchpad Settings

In order to move several supported accessibility settings here, we’ve actually completely redesigned the Mouse & Touchpad settings. Instead of one long scrolling list, it’s now separated into tabs for General settings as well as hardware-specific settings for Mouse and Touchpad individually.

![Mouse settings](https://cdn-images-1.medium.com/max/1600/1*cr4atYu07uDm3JjakBtBhQ@2x.png)

We’ve pulled the long-press and keypad control settings into the General settings. We also revised the left/right click setting to be more visual and to make more sense in right-to-left languages. And with the redesign, we’ve pulled the help text out of less-discoverable tooltips and put them right into the natural flow, requiring less finicky mousing around to learn about the different features.

### Universal Access Settings

For now, we will keep the existing settings available all in one spot in Universal Access as well as their new homes in the relevant panes. We’ll listen to feedback and if over time users are visiting Universal Access less for those types of settings, we will consider revisiting the design of Universal Access to focus on assistive technologies that don’t have a more natural home.

### Visual Style

Another way this has manifested is the massively-improved contrast in the system stylesheet; we always strive to be WCAG AA or AAA contrast compliant in the UI, reducing the need for special high contrast modes. If the entire desktop is high contrast _and_ looks great, it’s a win for everyone. Not only is it more accessible to those with difficulty seeing things that have low contrast, but it also greatly helps when using elementary OS on a projector, older display, or in sunlight.

### Color Schemes

Lastly, a new feature we brought to both Terminal and Code in elementary OS Juno was designed as an accessibility-for-all feature from the start. Both apps sport a color scheme option where you can choose between a light, dark, or high-contrast style. Rather than just changing the color scheme of the terminal emulator or code view itself, we also adapt the visual style of the whole app to match.

We've heard that these apps are more useful for people in dark environments and help alleviate migraines with the dark style. We've heard that it's less straining for other folks when using the light style. And we've heard that it's super helpful when coding in a super bright environment—like at a park or on a train with big windows—when using the high contrast style.

While we don't offer every possible color combination under the sun, we did shift from an idea of having one good color scheme to having multiple schemes that can serve the varrying needs of users. And we're exploring how we can expand this idea without it becoming overwhelming or unmaintainable.

## Just the Beginning

While many of these features are in elementary OS Juno today, they're just the beginning of our efforts in this area. We will continue to reorganize and refine settings and preferences, consider accessibility in our standard experience, and do our best to design a computing experience that is usable by all.

---

### Changes

The following edits were made for clarity or to reflect new information.

#### Nov 8, 2019:

- Reorganized existing content
- Added examples from mobile OSes
- Added Mindset section
- Added Color Schemes example
