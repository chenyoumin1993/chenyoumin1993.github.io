---
layout: default
title: Full Publication List
permalink: /misc/
---
<!-- <h2>Current Students</h2>
<ul style="overflow: hidden">
{% for stu in site.data.cym.stu %}
  <li>{{ stu.title }}</li>
{% endfor %}
</ul> -->
<h2>Current Students</h2>

<div class="container mt-4">
  {% assign counter = 0 %}

  {% for ins in site.data.cym.students %}
    
    {% if counter == 0 %}
      <div class="row">
    {% endif %}

      <div class="col-md-4 align-items-center text-center">
          <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="rounded w-50">
          {% if ins.webpage %}
          <p style="margin-top:0px;margin-bottom:0px"><a href="{{ ins.webpage }}">{{ins.name}}</a></p>
          {% else %}
          <p style="margin-top:0px;margin-bottom:0px">{{ins.name}}</p>
          {% endif %}
          <p style="margin-top:0px;margin-bottom:10px;line-height:1;">{{ins.type}}, Joined in {{ins.year}} {{ins.tag}}, B.S. {{ins.bs}}</p>
      </div>

      {% assign counter = counter | plus: 1 %}

    {% if counter == 3 %}
      {% assign counter = 0 %}
      </div>
    {% endif %}
  {% endfor %}

  {% if counter > 0 %}
    </div>
  {% endif %}
</div>



<h2>Teaching</h2>
<ul style="overflow: hidden">
{% for teach in site.data.cym.teach %}
  <li>{{ teach.title }}</li>
{% endfor %}
</ul>

<h2>Honors</h2>

<ul style="overflow: hidden">
{% for honor in site.data.cym.honors %}
  <li>{{ honor.title }}</li>
{% endfor %}
</ul>

<!-- 
<h2>Invited Talks</h2>

<ul style="overflow: hidden">
{% for talk in site.data.cym.talks %}
  <li>{{ talk.title }}</li>
{% endfor %}
</ul> -->


<h2>Professional Services</h2>

<ul style="overflow: hidden">
{% for service in site.data.cym.services %}
  <li>{{ service.title }}</li>
{% endfor %}
</ul>