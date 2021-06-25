---
layout: default
title: People
permalink: /people/
---

**Meet our team**
=================

We are a passionate bunch of researchers working on AI/ML applications in the life sciences. 

<div class="container-fluid">
    <div class="row">
        {% for p in site.data.people %}
        <div class="col-xl-3 col-lg-4 col-md-6 col-sm-12 py-vw1">
            <a href="#{{ p.name | slugify }}">
                <div class="people-photowrap">
                    <div class="people-photo"><img src="/assets/img/{{ p.photo }}"></div>
                    <div class="people-name"><p>{{ p.name }}{% if p.role %}<br><span class="people-tag">{{ p.role | capitalize }}</span>{% endif %}</p></div>
                </div>
            </a>
        </div>
        {% endfor %}
    </div>
</div>
<br>
<br>

{% for p in site.data.people %}
<div class="people-tile">
    <a id="{{ p.name | slugify }}">
        <!-- <hr {% if forloop.first == true %}class="hr-primary" {% endif %}/> -->
        <hr />
    </a>
    <div class="row py-vw1">
        <div class="col-md-3 pl-4">
            <div class="people-photowrap">
                <div class="people-photo"><img src="/assets/img/{{ p.photo }}"></div>
                <div class="people-name">
                    <p>
                    {{ p.name }}
                    {% if p.role %}<br><span class="people-tag">{{ p.role | capitalize }}</span>{% endif %}
                    {% for g in p.websites %}
                        {% for h in g %}
                            {% if h[0] == 'DKFZ' %}
                                <br><span class="people-below dkfz">DKFZ</span>
                            {% elsif h[0] == 'EMBL' %}
                                <br><span class="people-below embl">EMBL</span>
                            {% elsif h[0] == 'Heidelberg University' %}
                                <br><span class="people-below unihd">Heidelberg University</span>
                            {% else %}
                                <br><span class="people-below">{{ h[0] }}</span>
                            {% endif %}
                        {% endfor %}
                    {% endfor %}
                </p></div>
            </div>
        </div>
        <div class="col-md-7">
            <div class="people-description my-4 my-sm-0">
                {{ p.description | markdownify }}
            </div>
        </div>
        <div class="col-md-2 people-website">
            <ul>
            {% for g in p.websites %}
                {% for h in g %}
                    <li><a href="{{ h[1] }}" target="_blank" class="decorate-link">{% if p.websites.size > 1 %}{{ h[0] }} {% endif %}Group Website</a></li>
                {% endfor %}
            {% endfor %}
            </ul>
        </div>
    </div>
</div>
{% endfor %}
