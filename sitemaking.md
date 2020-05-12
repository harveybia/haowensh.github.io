---
layout: default
---

# Hosting

This site is hosted on [GitHub Pages][github_pages]. For custom domain name,
I set my domain's DNS `ALIAS` record to point towards
[GitHub server][apex_domain] and `CNAME` to point my www domain to my
GitHub pages domain (harveybia.github.io).

# Site Generation
I use a static website generator called [Jekyll][jekyll_link] and it
integrates well with GitHub pages.

# Theme

### Minimal
I use a theme called [minimal][min_theme]. You can get a preview of what the
theme looks like at this [example page][min_example].

### Dark Mode Support
I made my own modifications to this theme to support the ever-popular dark
mode.

This was achieved using CSS media queries. In my CSS I
added this simple query to override element colors when the preferred
color scheme is `dark`.

```css
@media (prefers-color-scheme:dark) {
  body {
    color:#dcdcdc;
    background:#2a2a2a;
  }

  /* ... */
}
```

# Source Code

You can view this website's source code here:

<a class="github-button" href="https://github.com/harveybia/harveybia.github.io" data-color-scheme="no-preference: light; light: light; dark: dark;" data-size="large" data-show-count="true" aria-label="Star harveybia/harveybia.github.io on GitHub">
harveybia.github.io
</a>

[github_pages]: https://pages.github.com/
[jekyll_link]: https://github.com/jekyll/jekyll
[apex_domain]: https://help.github.com/en/articles/setting-up-an-apex-domain
[min_theme]: https://github.com/pages-themes/minimal/
[min_example]: https://pages-themes.github.io/minimal/
[webkit_darkmode]: https://webkit.org/blog/8475/release-notes-for-safari-technology-preview-68/
[darkmode]: https://support.apple.com/en-us/HT208976/
