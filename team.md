---
layout: default
title: Team Members
permalink: /team/
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
          <p style="margin-top:0px;margin-bottom:40px;line-height:1;">{{ins.type}}, Joined in {{ins.year}} {{ins.tag}}, B.S. {{ins.bs}}</p>
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