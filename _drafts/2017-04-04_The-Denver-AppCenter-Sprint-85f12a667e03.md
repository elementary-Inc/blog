---
title: The Denver AppCenter Sprint
description: >-
  A couple weeks ago, we took a trip to Denver, Colorado for our AppCenter
  sprint. The team got in on a Wednesday night and hacked on…
date: '2017-04-04T00:21:18.854Z'
categories: []
keywords: []
slug: /@DanielFore/the-denver-appcenter-sprint-85f12a667e03
---

A couple weeks ago, we took a trip to Denver, Colorado for our AppCenter sprint. The team got in on a Wednesday night and hacked on AppCenter from Thursday (the 16th) through Monday (the 20th). We accomplished a _lot_ over the five days and are happy to share our experience and progress with you!

### Day 0 (Wednesday)

![](https://cdn-images-1.medium.com/max/800/0*xhPLDPUrDX4181pi.)

Wednesday was our traveling day. Everyone arrived at various times throughout the day, starting with Nathan. He and Cassidy started the day by doing a grocery run, and loading it all in the AirBnB. Cody and Blake arrived a few hours later (after Cody mustered enough courage to get on the train), but soon enough they met up with the rest of the gang. Felipe and Dan arrived later at night, and we all did the best we could do after a long day of traveling:

### Day 1 (Thursday)

Thursday kicked off with a battle against breakfast. Between scavenging for pans and cooking utensils, Dan and Felipe managed to make eggs, hash browns, and sausage for the team to chow down on before getting started.

![](https://cdn-images-1.medium.com/max/800/0*69V4Mpc_2CAdpemS.)

The team quickly decided that migrating AppCenter to GitHub would allow us to work much more quickly, but in order to do that we needed to do some cleanup on Launchpad. The first order of business was reviewing and merging outstanding branches into AppCenter. We knew that during the sprint we’d introduce changes that would need further polishing, so we also made a new stable release of AppCenter that included those fixes and translation updates. More details about that in our [March updates post](https://medium.com/elementaryos/loki-updates-for-march-ead798af2b63).

After we’d adjusted for jet lag, we mosied over to System76 and continued our work. We converted AppCenter’s bzr branch into a git branch, set up a new [project on GitHub](https://github.com/elementary/appcenter), and pushed. Outstanding bug reports were imported into [GitHub issues](https://github.com/elementary/appcenter/issues), and translations moved to [Weblate](https://l10n.elementary.io/projects/desktop/appcenter/). For actually building the AppCenter package, we have an auto importer running on Launchpad. From the perspective of delivering unstable AppCenter updates to our Daily PPA, nothing has changed.

![](https://cdn-images-1.medium.com/max/800/0*DBwmslRowt_SjCQ-.)

From there, we split up. Blake, Cassidy, and Dan took over the whiteboard room and the rest of the team set up shop in a nearby corner of the office to get coding. Before the sprint, Dan had [prototyped](https://github.com/danrabbit/HumbleButton) our pay-what-you-want widget and the Stripe payment dialog. This allowed Felipe and Nathan to really hit the ground running and dive into accessing Stripe API with LibSoup. Meanwhile, in the whiteboard room, we discussed the goals of the home page and some of the common pitfalls we’ve experienced with other app store home page designs. We talked a lot about increasing discoverability and maintaining a high rate of churn. We talked about designs that would be visually interesting and engaging, but ensuring that the barrier for developers to use them would be low. One thing we quickly discovered was that Dan is incapable of sketching anything smaller than half of the whiteboard, which led to a lot of erasing and redrawing by Cassidy. By the end of the day, design team had kicked out some tidy wireframes and listed the attributes and behaviors of the various homepage widgets, desktop team had successfully generated test charges, and we ran into and addressed a few concerns that came up during development like email receipts and the feedback process when a charge fails.

![](https://cdn-images-1.medium.com/max/600/1*oIyIjserjtrAAIvHQFi-8Q.jpeg)
![Dan’s wireframes (left) and Cassidy’s (right)](https://cdn-images-1.medium.com/max/600/1*yoRLajY1qLI43taSUHVKbg.jpeg)
Dan’s wireframes (left) and Cassidy’s (right)

With all of that under our belts, we had worked up quite an appetite! System76 joined us at Soko Sushi on the first floor of their building where we got to know them a little better and shared several bottles of sake. Carl, the CEO of System76, remarked how great it was to be able to have the experience of working alongside friends and how it made getting up in the morning an exciting prospect. During the first day of our sprint, we tasted a bit of what they regularly enjoy and we were hooked. We connected over the ideas of doing great things and unleashing our potential.

![System76 & elementary bonding over Sushi](https://cdn-images-1.medium.com/max/800/0*Y7zaV8pQ-x1thTK4.)
System76 & elementary bonding over Sushi

### Day 2 (Friday)

![](https://cdn-images-1.medium.com/max/800/0*6jQJ9fUcTvp_bD2c.)

Friday, Nathan and Dane went to work on prototyping the home page designs that we had discussed the previous day, but ran into a snag. For reasons unknown at the time, we struggled to make use of AppStream’s ability to add custom keys. This is crucial for tying a payment ID to an app as well as providing any additional metadata to AppCenter. With the help of Matthias Klumpp, we resolved the problem and were able to continue working.

Meanwhile, Cassidy and Dan went back to basics on ratings and reviews to focus on how best to communicate qualitative information as concisely as possible. An “aha” moment happened when they started to think about reactions like those you see on Facebook or Slack. Maybe we could give quick and insightful reviews with reactions and let ratings be implicit through them. Dan started to sketch out various icons for attributes that could apply to an app like “Fast”, “Useful”, or “Buggy”. This seemed like a great beginning to a larger conversation and they decided to let the idea stew before moving too quickly on the implementation. They switched gears to working through the rest of the App information view, keeping this reactions idea in mind.

Felipe focused on the payment flow experience on the desktop, both implementing the feedback mechanisms we wireframed the previous day and new client-side credit card validation. Stripe’s documentation here was invaluable and made the process smooth and simple.

### Day 3 (Saturday)

![Cassidy looking real focused](https://cdn-images-1.medium.com/max/800/0*ql0XFZRsP_ioawbB.)
Cassidy looking real focused

On Saturday, several of us woke up with stomach problems. We had made breakfast plans downtown, but quickly cancelled and decided to stay in. Between sleep schedule changes, dietary changes, and copious amounts of performance enhancing substances, we had passed our peaks. However, it was still a great day for code. With AppStream custom key fields available, Nathan landed bold, branded banners into the App information views. Dan landed several branches that added links for standard AppStream URL keys like “Translations” and “Report a Problem”. We implemented simple continuous integration testing with Travis and cleaned up several files. Felipe plugged away on payments, making sure to get everything just right.

### Day 4 (Sunday)

On Sunday, everything started to fall into place. Building off the previous day’s work, Nathan landed banners on the homepage that display the newest apps to AppCenter with an API that Blake just put into production. Felipe’s payments code was successfully merged. Adam, who was participating remotely, snuck in a branch for better error reporting. In the afternoon, we headed back to the System76 office where Cassidy and Dan finished up a few sketches. Katie and Dan wrapped up some branding work, finalizing the purple used in the AppCenter icon and the fonts used for the AppCenter logo.

![](https://cdn-images-1.medium.com/max/800/0*jGebuPt0pOYpZeCq.)

We closed out the night with our final team dinner, where we reminisced about the time we’ve spent getting to know each other and looked forward to seeing everyone together again.

### Day 5 (Monday)

Monday morning, we said our final goodbyes and cleaned up our AirBnB. While most of the team headed out to the airport early in the morning, Cody and Dan went back to the Blaede’s to play with the cat and get some last minute hacking in. Dan merged a couple of minor stylesheet changes, while Cody resolved a small packaging mishap.

![Dan (left) and Cody (right)](https://cdn-images-1.medium.com/max/800/0*GL6nM2MIQmDYNbKx.)
Dan (left) and Cody (right)

We want to give one last shoutout to our backers on IndieGoGo for funding this sprint. It was tremendously helpful to be able to get together in person and we couldn’t have done all the work we did in this timeframe without being in person. Look forward to more AppCenter news as we move into private beta with our developer community! Plenty more AppCenter features have already landed since the sprint and there will be more to come before the new AppCenter Dashboard goes live.

Now that AppCenter itself is on GitHub, it’s easier to follow along and contribute! See the [latest commits](https://github.com/elementary/appcenter/commits/master), [open issues](https://github.com/elementary/appcenter/issues), and review any outstanding [pull requests](https://github.com/elementary/appcenter/pulls).

_We’d like to say thanks again to our supporters on_ [_Bountysource_](https://salt.bountysource.com/teams/elementary) _and_ [_Patreon_](https://www.patreon.com/elementary)_, those who’ve purchased a copy of_ [_elementary OS_](https://elementary.io/) _or merch from_ [_our store_](https://elementary.io/store/)_. Every contribution helps make all of this possible, and we wouldn’t be here without you! If you’d like to help improve elementary OS, don’t hesitate to_ [_Get Involved_](https://elementary.io/get-involved)_!_