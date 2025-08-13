---
layout: single
title: "Articles"
permalink: /articles/
---

{% assign pubs = site.publications | sort: 'date' | reverse %}

### Published / Forthcoming
{% for p in pubs %}
  {% if p.status == "published" or p.status == "forthcoming" %}
- **{{ p.title }}**{% if p.authors %} — {{ p.authors }}{% endif %}{% if p.venue %}, *{{ p.venue }}*{% endif %}{% if p.paperurl %}. [PDF/Link]({{ p.paperurl }}){% endif %}
  {% endif %}
{% endfor %}

### Working Papers / Drafts
{% for p in pubs %}
  {% if p.status == "working paper" or p.status == "draft" %}
- **{{ p.title }}**{% if p.authors %} — {{ p.authors }}{% endif %}{% if p.venue %}, {{ p.venue }}{% endif %}{% if p.paperurl %}. [PDF/Link]({{ p.paperurl }}){% endif %}
  {% endif %}
{% endfor %}
