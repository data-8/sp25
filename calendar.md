---
layout: page
title: 🏠 Home
description: Listing of course modules and topics.
nav_order: 1
permalink: /
---

# **Data 8: Foundations of Data Science**

{: .mb-2 }
UC Berkeley, Spring 2025
{: .mb-2 .fs-6}

[Ed](){: .btn .btn-ed}
[Gradescope](){: .btn .btn-gradescope}
[Lecture Recordings](){: .btn .btn-bcourses}
[Jump to Current Week](){: .btn .btn-currweek}

{% include announcements-navigation.html %}

{% assign mods = site.modules | where: 'class', 'Berkeley' %}
{% assign active-mods = '' | split: '' %}

{% for mod in mods %}
  {% if mod.status == 'Active' %}
    {% assign active-mods = active-mods | push: mod %}
  {% endif %}
{% endfor %}

{% for module in active-mods %}
  {{ module }}
{% endfor %}

<script src="{{ '/assets/scripts/announcement-navigation.js' | relative_url }}"></script>