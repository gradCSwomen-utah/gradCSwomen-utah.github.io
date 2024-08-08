---
layout: page
title: People
permalink: /officers
order: 4
---

<div class="row masonry-grid">
  {% assign sorted_officers = site.officers | sort:"order" %}
  {% for officer in sorted_officers %}
    {% include officerbox.html %} 
  {% endfor %}
</div>
