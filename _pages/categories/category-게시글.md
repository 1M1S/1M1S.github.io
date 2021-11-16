---
title: "게시글"
layout: archive
permalink: categories/게시글
author_profile: false
sidebar_main: true
---


{% assign posts = site.categories.게시글 %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}