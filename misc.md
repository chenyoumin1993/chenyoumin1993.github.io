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

<div class="container mt-4">
  <h2>Current Students</h2>

  <h4>Ph.D. Students</h4>
  {% assign counter = 0 %}

  {% for ins in site.data.cym.students %}
    
    {% if counter == 0 %}
      <div class="row">
    {% endif %}

    {% if ins.type == "PhD" %}

      <div class="col-md-4 align-items-center text-center">
          <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="image--cover">
          {% if ins.webpage %}
          <p><a href="{{ ins.webpage }}">{{ins.name}}</a></p>
          {% else %}
          <p>{{ins.name}}</p>
          {% endif %}
          <p>Start in {{ins.year}} {{ins.tag}}</p>
          <p>B.S. {{ins.bs}}</p>
      </div>

      {% assign counter = counter | plus: 1 %}

    {% endif %}

    {% if counter == 3 %}
      {% assign counter = 0 %}
      </div>
    {% endif %}
  {% endfor %}

  {% if counter > 0 %}
    </div>
  {% endif %}

  <h4>Master Students</h4>
  
  {% assign counter = 0 %}

  {% for ins in site.data.cym.students %}
    
    {% if counter == 0 %}
      <div class="row">
    {% endif %}

    {% if ins.type == "Master" %}

      <div class="col-md-4 align-items-center text-center">
          <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="image--cover">
          {% if ins.webpage %}
          <p><a href="{{ ins.webpage }}">{{ins.name}}</a></p>
          {% else %}
          <p>{{ins.name}}</p>
          {% endif %}
          <p>Start in {{ins.year}} {{ins.tag}}</p>
          <p>B.S. {{ins.bs}}</p>
      </div>

      {% assign counter = counter | plus: 1 %}

    {% endif %}

    {% if counter == 3 %}
      {% assign counter = 0 %}
      </div>
    {% endif %}
  {% endfor %}

  {% if counter > 0 %}
    </div>
  {% endif %}

  <h4>Undergraduate Students</h4>

  {% assign counter = 0 %}

  {% for ins in site.data.cym.students %}
    
    {% if counter == 0 %}
      <div class="row">
    {% endif %}

    {% if ins.type == "Undergrad" %}

      <div class="col-md-4 align-items-center text-center">
          <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="image--cover">
          {% if ins.webpage %}
          <p><a href="{{ ins.webpage }}">{{ins.name}}</a></p>
          {% else %}
          <p>{{ins.name}}</p>
          {% endif %}
          <p>Joined in {{ins.year}}</p>
      </div>

      {% assign counter = counter | plus: 1 %}

    {% endif %}

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