---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<p class="archive__lead">Peer-reviewed research on building performance, daylighting, intelligent systems, and computational methods.</p>

{% assign pubs = site.publications | sort: "date" | reverse %}
{% assign journals = pubs | where: "type", "Journal article" %}

<p class="archive__count">
  {{ pubs | size }} publications &middot; {{ journals | size }} journal articles
  {% if author.googlescholar %}&middot; <a href="{{ author.googlescholar }}">Google Scholar</a>{% endif %}
</p>

{% assign years = pubs | group_by_exp: "item", "item.date | date: '%Y'" %}
{% for year in years %}
  <section class="pub-year">
    <h2 class="pub-year__label" aria-hidden="true">{{ year.name }}</h2>
    <div class="pub-year__items">
      <h2 class="sr-only">{{ year.name }}</h2>
      {% for post in year.items %}
        {% include archive-single.html type="publication" %}
      {% endfor %}
    </div>
  </section>
{% endfor %}
