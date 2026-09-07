---
layout: page
title: People
permalink: /officers
order: 4
---

<div class="member-section-title">
  <h2><span>Current Officers</span></h2>
</div>

<div class="row masonry-grid">
  {% assign current_officers = site.officers | sort:"order" %}
  {% for officer in current_officers %}
    {% unless officer.path contains '/past_members/' %}
      {% include officerbox.html %}
    {% endunless %}
  {% endfor %}
</div>

<div class="member-section-title">
  <h2><span>Past Members</span></h2>
</div>

<div class="table-responsive">
  <table class="table past-members-table">
    <thead>
      <tr>
        <th scope="col">Position</th>
        <th scope="col">Person</th>
      </tr>
    </thead>
    <tbody>
  {% assign past_officers = site.officers | where_exp: "officer", "officer.path contains '/past_members/'" | sort:"order" %}
  {% for officer in past_officers %}
      <tr>
        <td>{{ officer.title }}</td>
        <td>{{ officer.name }}</td>
      </tr>
  {% endfor %}
    </tbody>
  </table>
</div>
