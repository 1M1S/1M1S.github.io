---
title: "/api/user"
layout: archive
permalink: categories/user
author_profile: false
sidebar_main: true
---


{% assign posts = site.categories.user %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}