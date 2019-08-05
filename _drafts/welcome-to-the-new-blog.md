---
title: Welcome to the New Blog
subtitle: Why it exists, how we built it, and what's next
author: cassidyjames
---

In 2016, elementary moved to a Medium publication to host our official blog. At the time, Medium was touted as a simple, clean, and reader-focused host for writers. They supported custom domains, a robust API, RSS, rich formatting, and great image embedding. We have been largely happy with the experience, but in 2018 something changed. 

## The Decline of Medium

Medium—in its quest for financial sustainability—started getting more aggressive toward readers. First, Medium removed the ability to create an account with an email address, instead requiring a third-party social networking platform. Then, readers who were not signed in—perhaps because they didn't want yet-another-account tracking them across the Internet, or just because they were using a private browser—were shown modal pop-ups asking them to create an account.

Medium wants all readers to always be signed into an account so they can more easily track what individual readers are doing on their platform. They also restrict how many monetized articles individuals can read, which would be difficult without being tied to a user account.

Then Medium started getting aggressive toward authors and publications. With their new monetized platform in tow, they started switching authors' stories to be behind their paywall by default, with a tiny checkbox when publishing. Remember, this paywall actively reduces the potential readership of stories, as it restricts it to paying members. They also removed their API support (meaning no posting to Medium from another platform), removed custom domain support (meaning all posts are hosted at their branded Medium.com), and started putting the Medium branding more in competition with publications' branding.

For an independent and privacy-focused company like elementary, this didn't make sense. While we understand and empathize with the struggles of ethical monetization—and applaud Medium for refusing to monetize via ads and trackers—the result has been a worse experience for our readers.

The authorship experience was also lacking in a number of ways: they arbitrarily block lesser-known browsers like Epiphany from using the editing tools based on their user agent (instead of checking supported features), image handling has been broken in Firefox for years without any response from the support team, and formatting for posts seemingly randomly breaks based on global CSS changes on the site.

We've constantly gotten comments on Reddit, Twitter, and other social media asking us to move away from Medium—and those have increased substantially over time.

So we have.

## Finding a New Home

We explored several options when looking for a new home for the blog. First, we checked out [Write.as](https://write.as) since we'd had some experience with the platform, and the developers are really great folks. Write.as excels as a way to painlessly publish thoughts to the Internet—anonymously or otherwise. If you're an individual looking for a clean, reader-friendly Medium-like experience, Write.as is a perfect fit. However, it was lacking in some of the features we depend on, like multi-author blogs and collaborative authorship (i.e. having fellow team members review, privately comment on, and make suggestions to posts before they're public).

We also looked at several traditional blogging platforms: Wordpress, Ghost, etc. While these could have worked, we weren't enthused about spinning up yet-another complex dynamic web server, or paying someone else to do it for us.

We've used static Jekyll-powered sites, hosted via GitHub pages before: our [AppCenter](https://appcenter.elementary.io) site is exactly that. I also have extensive experience with Jekyll, having done a lot of personal, professional, and freelance work in that space. So, I set out to investigate using Jekyll for the elementary blog.

## Settling in with Jekyll

After a few days of spinning up a simply-themed Jekyll site on a private repo, I was convinced it was the way to go. It ticked all the boxes for us:

- **Fast**. Since it's a static site, there's no waiting around for pages to load and render on a server. They're served as-is directly off a fast CDN.
- **Total control.** Since we are writing the entirety of the HTML, it means we can decide _exactly_ what the blog is, looks like, etc.
- **Privacy-first.** Because we have total control and are leaning on the static nature of Jekyll, it means we can be fanatical about privacy: no external JavaScript, no analytics, no social tracking scripts, etc. Just what matters: the content.

The real selling point for us, however, was the authoring workflow. Since the code for the blog is hosted on GitHub, we can lean into our heavy knowledge and usage of the platform at the center of our normal workflow and apply it to the blog. If anyone in the org wants to write something on the blog, they just write it in Markdown and submit a pull request. The appropriate team can review that PR—just like all code PRs—and approve it before it is merged. Even better: anyone in the org can comment on, make suggestions to, and collaborate on the post using the GitHub UI. We even have CI running on the blog to make sure changes don't break the build, and we can even add HTML and CSS linters to that process pretty easily. It's an awesome collaborative workflow that we already know, but for the blog.

### Modern Features

Just because it's a simple static blog doesn't mean we don't support all the modern features you'd expect:

1. **[RSS feed](https://blog.elementary.io/feed)** for all the subscribing and cross-posting you could desire.
2. **Completely responsive** design from the start.
3. **Dark style** support from day zero (if your OS and browser support it).
4. **Rich image embedding** with side-by-side layouts, zooming in, and full-bleed support.
5. **Sharing to social media** except without the privacy-invasiveness that usually comes with it.

One thing we've actively chosen _not_ to implement or support is some sort of commenting system: while we could embed something like Disqus or another third-party commenting platform, it is just another place for people to worry about an account, for us to moderate, to track users, and to slow down the blog. Instead, we link to official posts that we've made about the story on social media, and offer up social sharing options (including a bare permalink) so readers can discuss it with us or on their platform of choice.

### How It's Made

So, how is the new elementary Blog actually put together? It's pretty simple: first, we're using the open source [Jekyll](https://jekyllrb.com/) project to generate a static site. Posts go into the `_posts` folder in the repository. These are Markdown files with a small amount of metadata up front like who wrote it and what image should be featured. That post is rendered by the `_layouts/post.html` template, which just sets up the header, wraps the content in an `<article>` tag, and pulls in a handful of `_includes` which help render reusable components like the author byline, the license, social links, and the "Up Next" posts.

We're also using a handful of open source plugins to Jekyll for common tasks like [generating an RSS feed](https://github.com/jekyll/jekyll-feed), paginating the homepage, and [generating a sitemap](https://github.com/jekyll/jekyll-sitemap). We're restricted with what we can use since GitHub Pages generates the site using a `--safe` environment, but if we wanted to add more plugins, we could lean on Travis CI to build and deploy the site. For now, though, the built-in GitHub Pages build and deploy works well.
