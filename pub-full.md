---
layout: pub
title: Full Publication List
permalink: /pub-full/
---

[Selected Publication List Here](/pub/)

(* indicates corresponding authors.)

<h2>Preprints</h2>
{% assign pubs = site.data.pub %}
{% assign print = 0 %}
<ul id="archive">
    {% for pub in pubs %}
        {% for author in pub.authors %}
        {% if author.author == "Youmin Chen" %}
            {% if pub.highlight == 3 %}
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
                </div>
            </div>
            </li>
        {% endif %}
        {% assign print = 0 %}
    {% endfor %}
</ul>

<h2>Conference Papers</h2>
{% assign pubs = site.data.pub %}
{% assign print = 0 %}
<ul id="archive">
    {% for pub in pubs %}
        {% for author in pub.authors %}
        {% if author.author == "Youmin Chen" %}
            {% if pub.type == "conference" %}
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


<h2>Journal Papers</h2>
{% assign pubs = site.data.pub %}
{% assign print = 0 %}
<ul id="archive">
    {% for pub in pubs %}
        {% for author in pub.authors %}
        {% if author.author == "Youmin Chen" %}
            {% if pub.type == "journal" %}
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

<h2>Thesis</h2>
<ul id="archive">
<li class="archiveposturl" style="background: transparent">
    <div class="lecture-container">
        <div class="content">
            <span style="font-weight: bold;">Research on Key Technologies for Persistent Memory Storage System.</span><br>
            PhD Dissertation (in Chinese) <a href="">PDF</a> <br />
            <strong><font color="#b00c00">Outstanding Doctoral Dissertation Award, China Computer Federation (CCF), 2021</font></strong><br />
            <strong><font color="#b00c00">ACM SIGOPS ChinaSys Doctoral Dissertation Award, 2021</font></strong><br />
            <strong><font color="#b00c00">Distinguished PhD Dissertation Award, Tsinghua University, 2021</font></strong>
        </div>
    </div>
</li>
</ul>
