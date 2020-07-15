---
title: "Leaving Google Analytics is Finally Plausible"
description: "Another big step towards privacy and transparency"
author: danrabbit
image:
tags:
  - web
  - privacy
---

We've always believed that our user experience doesn't just begin when people use elementary OS; it begins from the first moment that someone interacts with our organization in any way. And for a lot of people, that experience starts with our website. You may already know about our stance on privacy, advertising, and tracking from our previous blogposts, and that a core part of our business model is that you are our customer, not a product.

<aside>
{% assign post = site.posts | where:"slug", "you-are-not-the-product" | first %}
{% include featured.html post=post %}
</aside>

You might also know that our website has a comprehensive [privacy page](https://elementary.io/privacy) that details not only exactly how we use things like cookies on our website, but how to disable them. And with such a strong stance on privacy, you might be asking yourself why elementary uses analytics at all, let alone Google Analytics. To that I am happy to respond that we are leaving Google Analytics behind in favor of the Open Source and privacy-respecting [Plausible](https://plausible.io/).

# What Are Analytics?

If you're not familiar with the concept, you may be surprised to know that the majority of the websites you regularly visit are collecting statiscal data about your usage of the website. Website developers then use this data to optimize infrastructure, pinpoint problems, or even drive design decisions—something we don't advise.

<aside>
{% assign post = site.posts | where:"slug", "privacy-and-elementary-os" | first %}
{% include featured.html post=post %}
</aside>

At elementary, we use anonymous data about things like physical region and download method to make sure we have properly localized HTTPS and Torrent downloads so that you can get a fast and stable connection. We also keep track of which pages are most—and least—visited on our website so we know where to focus improvements. And we pay attention to which operating system downloaders are coming from to make sure that we're on track with our mission of bringing an Open Source operating system to more people.

But Google Analytics tracks a whole lot more than that, and frankly we don't want this data. Google will happily tell us if you have changed jobs or moved recently and whether you like to spend time outdoors. It's invasive and unnecessary and even though we may choose to ignore these profiles, by using Google Analytics on our website, we've contributed to creating them. This really does not align with our values and for quite some time now, we've been looking at how we can move away.

# The Challenge

Google Analytics is by far the most popular analytics solution available and there are few privacy-respecting alternatives. We considered a few self-hosted products like [Matomo](https://matomo.org/), but we couldn't find a good fit in terms of maintanence, pricing, and features. That is, until we stumbled upon Plausible.

Plausible is a UK-based startup that provides a hosted, privacy-conscious analytics solution with simple and fair pricing and support for custom events. The product itself fits what we're looking for in an analytics solution, and it's encouraging to see that they are actively growing and developing new features, but what really got our attention is their messaging around their business model. Read [their blog post on monetizing](https://plausible.io/blog/open-source-funding) and see if it sounds familiar.

<div class="twitter-card" markdown="0">
  <a href="https://twitter.com/plausiblehq/status/1282678251148763137">
    <div class="header">
        <img class="avatar" src="/images/leaving-google-analytics-is-finally-plausible/twitter-avatar.png" />
        <strong>Plausible Analytics</strong>
        <p>@PlausibleHQ</p>
        <img class="logo" src="/images/twitter.svg" />
    </div>
    <p>
        A day in the life of a startup...<br />
        "Wanted to quickly reach out and see if you'd be interested in raising funds or taking investment"<br />
        No.<br />
        "Any interest in talking about an exit?"<br />
        No.
    </p>
    <p class="timestamp">7:08 AM · Jul 13, 2020</p>
  </a>
</div>

Unlike Google, Plausible isn't in the advertising game and doesn't have an obvious incentive to collect and sell user data. And they've made it clear that they're not interested in being scooped up by VCs or new ownership that might seek to change those values. They make money the same way elementary does: by directly charging customers for their product. We know firsthand how important it is to make sure that your business is built around your ethics, and we get the same feeling from the folks at Plausible. We're excited to be supporting a company that shares our values and respects the people visiting our website.

# Improving Transparency

One of the most interesting and unique features of Plausible is their open invitation and celebration of data transparency. Every user of Plausible is encouraged to make their analytics dashboard public so that people can see the data for themselves and know that nothing fishy is going on. We've embraced this new feature at elementary and opened up the dashboards for our various subdomains as well as our main website. Check them out yourself!

  * [Main Website](https://plausible.io/elementary.io)
  * [Blog](https://plausible.io/blog.elementary.io)
  * [Developer Portal](https://plausible.io/developer.elementary.io)
  * [AppCenter on The Web](https://plausible.io/appcenter.elementary.io)
  * [Release Tracking](https://plausible.io/releases.elementary.io)

We hope that this move will provide a tangible improvement to your digital life and give you more peace of mind when using elementary products. We're always working towards the ideal and we're confident that we've made a big step by switching to Plausible. Let us know on social media what you think of the new public analytics dashboard and feel free to ask questions about how we're using this data!
