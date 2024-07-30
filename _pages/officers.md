---
layout: page
title: People
permalink: /officers
order: 6
---

<div class="row masonry-grid">
  {% assign sorted_officers = site.officers | sort:"order" %}
  {% for officer in sorted_officers %}
   <p>{{ officer.name }}</p>
    {% include officerbox.html %} 
  {% endfor %}
</div>
