---
layout: page
title: Team Members
permalink: /team/
---
<!-- <h2>Current Students</h2>
<ul style="overflow: hidden">
{% for stu in site.data.cym.stu %}
  <li>{{ stu.title }}</li>
{% endfor %}
</ul> -->
I lead the **S**torage, **O**perating, and **A**I Systems **R**esearch (**SOAR**) group, 
focusing on innovative approaches to system design that prioritize efficiency, scalability, and resilience.

<h3>PhD Students</h3>
<div class="row">
  {% for ins in site.data.cym.phd %}
    <div class="col-md-6" style="margin-top:0px;margin-bottom:20px">
      <div class="card mb-3 border-0">
        <div class="row g-0">
          <div class="col-md-4">
            <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="img-fluid rounded w-100" alt="...">
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title"><b>{{ins.name}}</b></h5>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">Joined in {{ins.year}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">B.S. from {{ins.bs}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">
                <small class="text-muted">{{ins.tag}}</small>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<h3>Master Students</h3>
<div class="row">
  {% for ins in site.data.cym.master %}
    <div class="col-md-6" style="margin-top:0px;margin-bottom:20px">
      <div class="card mb-3 border-0">
        <div class="row g-0">
          <div class="col-md-4">
            <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="img-fluid rounded w-100" alt="...">
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title"><b>{{ins.name}}</b></h5>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">Joined in {{ins.year}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">B.S. from {{ins.bs}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">
                <small class="text-muted">{{ins.tag}}</small>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<h3>Undergraduate Interns</h3>
<div class="row">
  {% for ins in site.data.cym.undergrad %}
    <div class="col-md-6" style="margin-top:0px;margin-bottom:20px">
      <div class="card mb-3 border-0">
        <div class="row g-0">
          <div class="col-md-4">
            <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="img-fluid rounded w-100" alt="...">
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title"><b>{{ins.name}}</b></h5>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">Joined in {{ins.year}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">{{ins.bs}}</p>
              <p class="card-text" style="margin-top:0px;margin-bottom:0px">
                <small class="text-muted">{{ins.tag}}</small>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<!-- 
<h3>PhD Students</h3>

<div class="container mt-4">
  {% assign counter = 0 %}

  {% for ins in site.data.cym.phd %}
    
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

<h3>Master Students</h3>

<div class="container mt-4">
  {% assign counter = 0 %}

  {% for ins in site.data.cym.master %}
    
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


<h3>Undergraduate Interns</h3>

<div class="container mt-4">
  {% assign counter = 0 %}

  {% for ins in site.data.cym.undergrad %}
    
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
</div> -->