---
layout: post
author: shawn phy
---

## Introduction 
Seo refers to site engine optimization, and is the technology behind ensuring you appear in browser searches first. Jekyll has simple intergration to optimize your site for SEO purposes. This is achieved by use of jekyll plugins.

### jekyll-seo-plugin
this is a plugin that is used to Ensure SEO without using much javascript. 

# Installing Jekyll SEO Tag

1. Add the following to your site's `Gemfile`:

  ```ruby
  gem 'jekyll-seo-tag'
  ```

2. Add the following to your site's `_config.yml`:

  ```yml
  plugins:
    - jekyll-seo-tag
  ```

If you are using a Jekyll version less than `3.5.0`, use the `gems` key instead of `plugins`.

3. Add the following right before `</head>` in your site's template(s):

<!-- {% raw %} -->
  ```liquid
  {% seo %}
  ```
<!-- {% endraw %} -->