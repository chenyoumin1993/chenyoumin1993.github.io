---
layout: default
title: Full Publication List
permalink: /misc/
---

<h2>Honors</h2>

<ul style="overflow: hidden">
{% for honor in site.data.cym.honors %}
  <li>{{ honor.title }}</li>
{% endfor %}
</ul>



<h2>Invited Talks</h2>

<ul style="overflow: hidden">
{% for talk in site.data.cym.talks %}
  <li>{{ talk.title }}</li>
{% endfor %}
</ul>


<h2>Professional Services</h2>

<ul style="overflow: hidden">
{% for service in site.data.cym.services %}
  <li>{{ service.title }}</li>
{% endfor %}
</ul>