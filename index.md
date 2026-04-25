---
layout: default
title: Ahmed Irfan
---

<header>
  <h1>Ahmed Irfan</h1>
  <p class="bio">
    I work on automated reasoning, SAT and SMT solving, formal methods,
    model checking, and neurosymbolic AI. I'm one of the developers of the
    <a href="https://yices.csl.sri.com">Yices2</a> SMT solver and co-chair of
    <a href="https://fmcad.forsyte.at/FMCAD25/">FMCAD 2025</a>. I previously
    worked on neural network verification.
  </p>
  <nav class="contact">
    <a href="https://scholar.google.com/citations?user=rYIFql4AAAAJ&hl=en">Google Scholar</a>
    <a href="https://dblp.org/pid/149/3835.html">DBLP</a>
    <a href="https://github.com/ahmed-irfan">GitHub</a>
    <a href="https://www.linkedin.com/in/ahmed-irfan-phd">LinkedIn</a>
  </nav>
</header>

<section>
  <h2>Publications</h2>
  {% assign selected_pubs = site.data.publications | where: "selected", true %}
  {% for pub in selected_pubs %}{% include pub.html pub=pub %}{% endfor %}
  <p class="more"><a href="publications.html">All publications →</a></p>
</section>

<section>
  <h2>Software</h2>
  {% for proj in site.data.projects.visible %}{% include project.html proj=proj %}{% endfor %}

  <details>
    <summary>More past projects</summary>
    <div style="margin-top:12px">
      {% for proj in site.data.projects.hidden %}{% include project.html proj=proj %}{% endfor %}
    </div>
  </details>
</section>

<section>
  <h2>Service</h2>
  <ul class="compact">
    {% for item in site.data.service.recent %}<li><span class="role-text">{{ item.role }}, {% for v in item.venues %}{% if v.url %}<a href="{{ v.url }}">{{ v.name }}</a>{% else %}{{ v.name }}{% endif %}{% unless forloop.last %} · {% endunless %}{% endfor %}</span><span class="yr">{{ item.year }}</span></li>
    {% endfor %}
  </ul>
  <details>
    <summary>Earlier service</summary>
    <ul class="compact" style="margin-top:12px">
      {% for item in site.data.service.earlier %}<li><span class="role-text">{{ item.role }}, {% for v in item.venues %}{% if v.url %}<a href="{{ v.url }}">{{ v.name }}</a>{% else %}{{ v.name }}{% endif %}{% unless forloop.last %} · {% endunless %}{% endfor %}</span><span class="yr">{{ item.year }}</span></li>
      {% endfor %}
    </ul>
  </details>
</section>

<section>
  <h2>Competitions</h2>
  <ul class="compact">
    {% for c in site.data.competitions.recent %}<li><span class="role-text">{% if c.url %}<a href="{{ c.url }}">{{ c.label }}</a>{% else %}{{ c.label }}{% endif %}</span><span class="yr">{{ c.year }}</span></li>
    {% endfor %}
  </ul>
  <details>
    <summary>Earlier entries</summary>
    <ul class="compact" style="margin-top:12px">
      {% for c in site.data.competitions.earlier %}<li><span class="role-text">{% if c.url %}<a href="{{ c.url }}">{{ c.label }}</a>{% else %}{{ c.label }}{% endif %}</span><span class="yr">{{ c.year }}</span></li>
      {% endfor %}
    </ul>
  </details>
</section>
