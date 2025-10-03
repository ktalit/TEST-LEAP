---
layout: page
title: People
permalink: /people/
---

Last updated: {{ site.time | date: "%Y-%m-%d %H:%M:%S %z" }}

<ul>
{% assign folks = site.data.people %}
{% for p in folks %}
  <li style="margin:0 0 1rem 0;">
    <strong>{{ p.name }}</strong>{% if p.affiliation %} — {{ p.affiliation }}{% endif %}
    {% if p.homepage %}<br><a href="{{ p.homepage }}">Homepage</a>{% endif %}
  </li>
{% endfor %}
</ul>
