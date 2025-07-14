# MinDocMini Documentation

## Overview
MinDocMini is a Jekyll-based single-page documentation site generator that combines all content into one scrollable page.

## Setup
1. Install Jekyll: `gem install jekyll bundler`
2. Install dependencies: `bundle install`
3. Serve locally: `bundle exec jekyll serve`

## Configuration
Edit `_config.yml`:
```yaml
title: Your Document Title
description: by Your Name
baseurl: "/your-repo-name"
```

## Adding Content
Edit `index.markdown` to modify the single-page content. Content is organized in sections with H1 headers.

## Media Files
Place media descriptions in `_mindoc_media/` directory. Reference them using:
```liquid
{% assign media = site.mindoc_media | where: "page", "section-name" %}
{% include media.html pages=media %}
```

## Styling
Customize appearance by editing `_sass/main.scss`. The layout uses:
- `.single-page-content` for main container
- `.title-section` for header area
- Standard markdown styling for content sections

## Build
Generate static site: `bundle exec jekyll build`
Output appears in `_site/` directory.