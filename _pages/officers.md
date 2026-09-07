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

{% assign past_officers = site.officers | sort:"order" %}

<h3 class="past-members-year">2024-2025</h3>
<div class="table-responsive">
  <table class="table past-members-table">
    <thead>
      <tr>
        <th scope="col">Position</th>
        <th scope="col">Person</th>
      </tr>
    </thead>
    <tbody>
      {% for officer in past_officers %}
        {% if officer.path contains '/past_members/2024-2025/' %}
          <tr>
            <td>{{ officer.title }}</td>
            <td>{% unless officer.name == blank %}{{ officer.name }}{% else %}{{ officer.title }}{% endunless %}</td>
          </tr>
        {% endif %}
      {% endfor %}
    </tbody>
  </table>
</div>

<h3 class="past-members-year">2023-2024</h3>
<div class="table-responsive">
  <table class="table past-members-table">
    <thead>
      <tr>
        <th scope="col">Position</th>
        <th scope="col">Person</th>
      </tr>
    </thead>
    <tbody>
      {% for officer in past_officers %}
        {% if officer.path contains '/past_members/2023-2024/' %}
          <tr>
            <td>{{ officer.title }}</td>
            <td>{% unless officer.name == blank %}{{ officer.name }}{% else %}{{ officer.title }}{% endunless %}</td>
          </tr>
        {% endif %}
      {% endfor %}
    </tbody>
  </table>
</div>
