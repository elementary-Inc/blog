# blog

Testing the idea of a static, privacy-respecting blog

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
bundle exec jekyll serve
```

The site should now be available at http://127.0.0.1:4000/blog/

