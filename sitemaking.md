---
layout: default
---

# Hosting and Technology

This site is hosted on [Github Pages][github_pages]. For custom domain name,
I set my domain's DNS `ALIAS` record to point towards
[github server][apex_domain] and `CNAME` to point my www domain to my
Github pages domain (harveybia.github.io).

# Theme

### Minimal
I use a theme called [minimal][min_theme]. You can get a preview of what the
theme looks like at this [example page][min_example].

# Dark Mode Support
I made my own modifications on this theme to support the ever-popular dark
mode theme.

For example, in macOS 10.14+ and iOS 13+ you can set this option and
observe this website's color scheme change accordingly.

<div class="row">
  <div class="column">
    <img src="/assets/img/sitemaking/macos-mojave-system-preferences-general-dark-mode.png" alt="macOS Dark Mode Toggle" style="width:100%">
  </div>
  <div class="column">
    <img src="/assets/img/sitemaking/how-to-enable-dark-mode-in-ios-13-1.png" alt="iOS Dark Mode Toggle" style="width:100%">
  </div>
</div>

This was simply achieved by taking advantage of CSS media queries. In my CSS I
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

#### Known supported browsers:

**Safari**\\
Apple's
WebKit [introduced][webkit_darkmode] `prefers-color-scheme` media query "for
styling dark mode content" back in 2018.

# Source Code

You can view this website's source code here:

<div class="github-card" data-github="harveybia/harveybia.github.io" data-width="350" data-height="" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

[github_pages]: https://pages.github.com/
[apex_domain]: https://help.github.com/en/articles/setting-up-an-apex-domain
[min_theme]: https://github.com/pages-themes/minimal/
[min_example]: https://pages-themes.github.io/minimal/
[webkit_darkmode]: https://webkit.org/blog/8475/release-notes-for-safari-technology-preview-68/
[darkmode]: https://support.apple.com/en-us/HT208976/
