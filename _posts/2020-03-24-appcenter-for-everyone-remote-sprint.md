---
title: AppCenter for Everyone Remote Sprint
description: What we accomplished despite postponing the in-person sprint
author: cassidyjames
image: /images/appcenter-for-everyone/confetti.jpg
tags:
 - appcenter
 - event
---

<figure class="full-bleed" markdown="1">
![Confetti](/images/appcenter-for-everyone/confetti_2560.jpg)
</figure>

While we ended up postponing the in-person [AppCenter for Everyone](/appcenter-for-everyone) due to concerns around COVID-19, we did still get together remotely to get started on some of the work. We're a completely remote company and open source project to begin with, so we're used to working remotely; however, we had planned to get together in person to knock out more rapid whiteboarding, prototyping, and discussion that we've found is only at its most effective when people are in the same timezone and physical location for a few days.

## What We Worked On

We did get some things done, though, and have a clearer picture of the path forward.

### Design Track

Design-wise we whiteboarded, worked through, and ultimately prototyped a few components of the future AppCenter experience. One prototype branch addressed adding an account menu to the native AppCenter client along with app download history and links to the other places to manage your payment methods and online accounts. Another couple of branches explored embedding first a web-based OAuth flow and then a native OAuth flow for an elementary sync account (name still pending), which would power syncing your payment methods and purchase history between devices.

We also worked on a few branches for Online Accounts and the Wallet plug in System Settings to clean up the code and pave the way to these features.

Unfortunately, it felt like a lot of individual pieces of work were thrown out due to evolving requirements and discoveries during the remote sprint. While that's typical _to an extent_ with any sprint, it felt like the remote aspect made it especially true this time around. We did learn and think through things, but we look forward to getting together in person and more productively working through some of the design tasks.

### Web Track

A large part of our web team's goals to start was to investigate, understand, and communicate how all of the different web components fit together for a full Flatpak store; there's a Flatpak remore, flat-manager, linux-store-backend, linux-store-frontend, an account/authenticator web service, and then the dashboard (that we're building).

Our web team worked on spinning up an OAuth server that could create a passwordless account (leaning on email link based sign in for now), with fancy websockets for a seamless login. We also threw together a small prototyping project so we could iterate on some web concepts quickly without spinning up a whole dynamic server.

We built a rough prototype web service mockup to start hooking into the Flatpak Authenticator—even if much or all of this code is thrown away in the end, it was useful to begin hooking all the pieces together and understanding what each part needed to do.

### Desktop Track

On the desktop side of things, we started work on a shared library for components that will exist in both the Flatpak Authenticator and the Wallet plug (plus anywhere else we might need it). We also started work on a branch of the Authenticator that puts the pieces together—handling logging into an OAuth account, adding and managing payment cards via Stripe, processing payments (including the developer/platform split), storing/fetching purchases, and authenticating the Flatpak downloads.

### Other Work

While prototyping, an issue with Valadoc cropped up that prevented some docs from loading properly. So as part of the sprint we found the root cause (a too-large build environment) and worked to resolve it and get Valadoc.org working smoothly again.

We also worked toward some elementary OS 6 goals, working with Mutter and Vala upstream to get some fixes and new bindings in. We continued our work porting more Files code from C to Vala, and investigated some Flatpak implications for both Mail and Online Accounts management.

## What's Next

As soon as it is considered safe and appropriate, we do still plan to host an in-person sprint to accomplish the original AppCenter for Everyone goals. We'll share when we know more. While we'll still be working on some of those things in the meantime, we plan to pivot the main focus of our remote work to foundational pieces that will also help us ship elementary OS 6:

- Getting a first-party Flatpak remote up and running (which can eventually be the AppCenter remote as well)
- Continuing work on our elementary Flatpak SDK and Platform
- Starting to Flatpak our apps, starting with easier ones like Calculator
- Automating Flatpak builds as part of our CI and release pipeline
- Beginning Flatpak-focused developer documentation
