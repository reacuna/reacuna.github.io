---
layout: blog
title: Capistrano, rbenv, Bundler & Jekyll
---

The other day I was figuring out how to use Capistrano to deploy a Jekyll site.
I like using rbenv over other solutions, and I haven't had any problems before
deploying Rails apps using the capistrano-\* gems.

However, I didn't have a complete understanding on how to properly configure
capistrano to mark that the `jekyll` executable should be prefixed both by rbenv
and bundler.

Turns out, once you understand what you are doing, it's a lot easier:

```ruby
# Add jekyll to the commands that need to be exec'ed by rbenv
append :rbenv_map_bins, 'jekyll'

# Add jekyll to the commands that need to be exec'd by bundle
append :bundle_bins, 'jekyll'
```
