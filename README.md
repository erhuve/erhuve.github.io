[raymondluo.dev](https://raymondluo.dev/)

This GitHub Pages site redirects its rendered HTML pages, existing `/about/`
aliases and missing-page fallback to <https://flowershop.dev/>. All old page
paths lead to the new homepage. `CNAME` stays `raymondluo.dev`, preserving the old
domain's association with this Pages site.

The existing `jekyll-redirect-from` plugin applies the global `redirect_to`
default. The custom redirect layout uses JavaScript history replacement, an
immediate meta refresh, a canonical URL and a visible link fallback. The static
talk map is promoted to a Jekyll page so it receives the same redirect.

These are browser redirects, not HTTP 301 responses. Unknown paths initially
return HTTP 404 before the browser follows the redirect. Downloads, images and
other static assets remain available at their existing URLs.

To check the generated site with the GitHub Pages dependencies installed:

```sh
bundle exec jekyll build --safe
```

Forked from academicpages, which was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.
