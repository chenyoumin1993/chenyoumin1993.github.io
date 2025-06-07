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

<div>
    <div style="width:100%; float: left">
        <!-- <h2>Instructors</h2> -->
        <!-- <div class="image--cover-container">
            <img src="{{site.data.people.instructor.profile_pic | prepend: site.baseurl }}" class="image--cover">
            <p>{{site.data.people.instructor.name}}</p>
        </div> -->

        <div class="profile-pic-gallary ">
            <h2>Current Students</h2>
            {% assign counter = 0 %}
            {% for ins in site.data.cym.students %}
            <div class="image--cover-container" style="width:20%; float: left">
                <img src="{{ins.profile_pic | prepend: site.baseurl }}" class="image--cover">
                {% if ins.webpage %}
                <p><a href="{{ ins.webpage }}">{{ins.name}}</a></p>
                {% else %}
                <p>{{ins.name}}</p>
                {% endif %}
                <p>Start in {{ins.year}}, {{ins.type}}</p>
            </div>
            {% increment counter %}
              {% if counter == 4 %}
                {% assign counter = 0 %}
                <br />
              {% endif %}
            {% endfor %}
        </div>
    </div>
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