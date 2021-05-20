---
title: AppCenter Dashboard Sprint Spring 2021
description: Big steps for the Flatpak-based AppCenter
author: danrabbit
image:
tags:
  - appcenter
  - odin
  - devs
---

In case you're unfamiliar, we ran a crowdfunding campaign last year for an ambitious project that we called "AppCenter for Everyone". The goal of this project was to move our pay-what-you-want app store from being Debian-package-based and largely locked in to elementary OS to being based on Flatpak and available for use on any modern Linux-based desktop. Though we succesfully raised almost 200% of our goal, we had to postone our in-person sprint due to the COVID-19 pandemic. Over a year later—and with the availability of the vaccine—we decided to split this work up into multiple sprints, starting with one focused on the publishing workflow. Last week, I flew out to Denver, Colorado for a week to work with Blake Kostner and Cassidy James and I'm excited to share with you what we achieved.

<div style="margin: 3em auto;">
{% assign post = site.posts | where:"slug", "appcenter-for-everyone" | first %}
{% include featured.html post=post %}
</div>

We kicked off the week by talking about places where the current publishing experience could be improved. Transparency was a big theme, including issues with communicating review times, recording reviewer discussions and actions, and making it easier to contribute as an Open Source project. We also wanted to make sure there was a way to actively notify reviewers of pending reviews and improve the performance of the dashboard for people who have access to a large number of GitHub repositories. After some time brainstorming, we decided that the dashboard should be split up into two projects: the [AppCenter Dashboard](https://github.com/elementary/appcenter-dashboard) where developers submit their apps, connected to Stripe, etc. and [a new repository for reviewers](https://github.com/elementary/appcenter-reviews) where app submissions are processed as GitHub pull requests and ultimately published using GitHub Actions.

The design and workflow of the AppCenter Dashboard will remain largely the same for developers with a couple of small differences. Firstly, instead of trying to read and list all of the GitHub repositories you have access to, the new dashboard will only list apps for which you have explicitly submitted the repository URL. This should make the dashboard much faster, less cluttered, and reduces the scope of permissions needed for our GitHub integration. Secondly, there will be some minor changes to the way Stripe Connect API keys are generated and linked to your app. We're still working out the exact design details, but it should make monetizing your app a little more explicit.

On the review and publishing side, things are very different. Instead of an internal reviewer dashboard, reviews will now be processed as GitHub Pull Requests. This means that the review queue will be publically visible, as will discussion by reviewers, and who approved or requested changes on your app. This also means reviewers will be proactively notified on GitHub and on our company Slack when apps are submitted, which should cut down on review times. Publishing is now built on GitHub actions, using the [Flatpak Builder action](https://github.com/bilelmoussaoui/flatpak-github-actions) maintained by Bilal Elmoussaoui. We're especially happy to be working upstream there on a common codebase and have already submitted our first pull request. Automated tests run as part of the review process will now also be built using GitHub actions, which should make them much easier to write and re-usable in your own CI. And speaking of CI, we're now also building a publicly available container that includes the elementary platform to reduce build times.

There's still some work to do before we're ready for developers to submit their Flatpak apps through the new dashboard, but the submission process is already a working MVP. We'll be reaching out shortly to developers on a case-by-case basis to start testing, and submissions should be open to everyone shortly after that. If you haven't yet Flatpak'd your app, now is a great time! The documentation for packaging your app has already been updated on our website [here](https://docs.elementary.io/develop/writing-apps/our-first-app/packaging).

During the week, we spent some time working on Flatpak-ing more of our own first party apps and we'll now be shipping Camera, Mail, and Tasks as Flatpak apps in elementary OS 6. Eventually, our plan is to ship all of our first-party apps as Flatpaks and publish them through the AppCenter Dashboard. In this way, we'll be dogfooding the AppCenter submission process and developer platform, and strongly incentivized to make it a great experience. We're also able to see firsthand how apps must interact with sandboxing and portals and make sure platform APIs are available for developers.

As an aside, Cassidy and I also spent some time working on the new stylesheet and closed many of its remaining issues. Especially of interest is the work put into backdrop, disabled, and focus states.

I want to give a special shout out and thank you to developers working on Flathub and the wider Flatpak ecosystem. They've been an immense help offering their time and knowledge.

If you're looking for news about elementary OS 6 Beta 2, hang tight! We'll have more information soon about the improvements we've made on the road to the final stable release.
