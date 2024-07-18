---
layout: pub
title: Selected Publications
permalink: /pub/
---

[Full Publication List Here](/pub-full/)

(* indicates corresponding authors.)

{% assign pubs = site.data.pub %}
{% assign print = 0 %}
<ul id="archive">
    {% for pub in pubs %}
        {% for author in pub.authors %}
        {% if author.author == "Youmin Chen" %}
            {% if pub.highlight == 1 %}
            {% assign print = 1 %}
            {% endif %}
        {% endif %}
        {% endfor %}
        {% if print == 1 %}
            <li class="archiveposturl" style="background: transparent">
            <div class="lecture-container">
                <div class="content">
                    <span style="font-weight: bold;">{{ pub.title }}</span><br>
                    {% for author in pub.authors %}
                        {% if author.author == "Youmin Chen" %}
                        <strong><font color="#000000">{{ author.author }}</font></strong>
                            {% if author.author == pub.corresponding %}
                                <font color="#000000">*</font>
                            {% endif %}
                            <font color="#000000">,</font>
                        {% else %}
                            <font color="#888888">{{ author.author }},</font> 
                        {% endif %}
                    {% endfor %} <br />

                    {{ pub.pubname }} 
                    {% if pub.pubnamebrief %}<strong>({{ pub.pubnamebrief }})</strong>{% endif %}, 
                    {{ pub.year }}<br />
                    <a href="{{ pub.link }}">PDF</a>
                </div>
            </div>
            </li>
        {% endif %}
        {% assign print = 0 %}
    {% endfor %}
</ul>

