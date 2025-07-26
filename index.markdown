---
layout: single_page
---

# Introduction

{% assign media = site.mindoc_media | sort: "order" | where_exp: "item", "item.page == 'source'" | where_exp: "item", "item.media_type == 'video'" %}
{% include media.html pages=media %}

{% assign intro_images = site.mindoc_media | sort: "order" | where_exp: "item", "item.page == 'introduction'" | where_exp: "item", "item.media_type == 'image'" %}
{% include media.html pages=intro_images %}

# About this Source

# About this Edition

# Supplements

# Bibliography

# Credits and Acknowledgments

# About MinDoc



