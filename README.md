# blog

A static, privacy-respecting blog. In ways inspired by both Medium and the popular Medium-look-alike [mediumish-theme-jekyll](https://github.com/wowthemesnet/mediumish-theme-jekyll).

## Goals

Remember, we moved away from other platforms for very specific reasons.

1. **Completely frictionless** for readers.
2. **As few external resources as possible**—it slows things down and introduces potential privacy issues.
3. **Little-to-no JavaScript**—it’s a blog, not a web app.

## Modern Niceties

Just because it's static and privacy-respecting doesn't mean it's not modern and featureful.

1. **RSS feed support** for all the cross-posting you could desire.
2. **Completely responsive** design from the start.
3. **Dark style** support for everything from day zero.

## Editing workflow

Use the GitHub workflow!

1. **Use PRs to propose** and work. That means draft PRs for things that aren't ready to publish, too.
2. **All PRs should be reviewed** and approved before publishing.
3. **Use reviews and inline comments**/suggestions to collaboratively edit.

## Running Locally

GitHub has pretty good docs for [running GitHub Pages sites locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll). This README assumes you're on elementary OS.

### First time

```shell
sudo apt install ruby ruby-dev
gem install bundler
bundle install
```

### Serve

```shell
bundle exec jekyll serve --host 0.0.0.0 --drafts
```

The site should now be available at http://0.0.0.0:4000/ on your local machine, and your local machine's IP address on your network—great for testing on mobile OSes. Drafts in the `_drafts` folder will show up based on their last-edited time.

