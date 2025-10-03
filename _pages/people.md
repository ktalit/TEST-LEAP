---
layout: page
title: People
permalink: /people/
---

Below is our team & collaborators list. If you want headshots, save them into `/assets/people/` and set the `photo_url` fields in `_data/people.yml`.

<ul>
{% assign folks = site.data.people %}
{% for p in folks %}
  <li style="margin:0 0 1rem 0;">
    <strong>{{ p.name }}</strong>{% if p.affiliation %} — {{ p.affiliation }}{% endif %}
    {% if p.homepage %}<br><a href="{{ p.homepage }}">Homepage</a>{% endif %}
    {% if p.photo_url %}
      <br><img src="{{ p.photo_url }}" alt="{{ p.name }}" style="max-width:140px; border-radius:12px; margin-top:6px;">
    {% endif %}
    {% if p.note %}<br><em>{{ p.note }}</em>{% endif %}
  </li>
{% endfor %}
</ul>

