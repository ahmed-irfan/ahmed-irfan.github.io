---
layout: default
title: Publications
---

<a class="back" href="./">← Home</a>

<h1>Publications</h1>

{% assign by_year = site.data.publications | group_by: "year" | sort: "name" | reverse %}
{% for group in by_year %}
<section>
  <h2 class="year-header">{{ group.name }}</h2>
  {% for pub in group.items %}{% include pub.html pub=pub %}{% endfor %}
</section>
{% endfor %}

<section>
  <h2>Theses</h2>
  {% for t in site.data.theses %}{% include pub.html pub=t %}{% endfor %}
</section>
