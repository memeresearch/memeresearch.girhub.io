---
layout: default
permalink: /team/
projectName: 'SEEDS'

---

## The MEME Team

{% assign groups = site.data.members | group_by: "status" | sort: "value" %}
{% for group in groups %}
<h3>{{ group.name }}s</h3><ul>
{% assign itemsSorted = group.items | sort: "last" %}
{% for item in itemsSorted %}<li>{% if item.url %}<a href="{{ item.url }}" target="_blank">{% endif %}{{ item.first }} {{ item.last }}{% if item.url %}</a>{% endif %}{% if item.affiliation %}, {{ item.affiliation }}{% endif %}. <em>{{ item.role }}</em></li>{% endfor %}
</ul>
{% endfor %}

<h3>Software Development</h3>
<ul>
  <li>The MEME software was developed by Ben Loh at <a href="http://www.inquirium.net" target="_blank">Inquirium</a> and Sri Seah (<a href="https://davidseah.com/" target="_blank">https://davidseah.com/</a>).</li>
</ul>
