---
layout: default
title: People
permalink: /people/
---

**People** at ELLIS Heidelberg 
==============================
{% for p in site.data.people %}
<hr {% if forloop.first == true %}class="hr-primary" {% endif %}/>
<div class="row py-vw1">
    <div class="col-3 pl-4">
        <div class="people-photowrap">
            <div class="people-photo"><img src="/assets/img/{{ p.photo }}"></div>
            <div class="people-name"><p>{{ p.name }}
                {% if p.role %}<br><span class="people-below">{{ p.role | capitalize }}</span>{% endif %}
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
    <div class="col-7">
        <div class="people-description">
            {{ p.description | markdownify }}
        </div>
    </div>
    <div class="col-2 decorate-link">
        <ul>
        {% for g in p.websites %}
            {% for h in g %}
                <li><a href="{{ h[1] }}" target="_blank">{% if p.websites.size > 1 %}{{ h[0] }} {% endif %}Group Website</a></li>
            {% endfor %}
        {% endfor %}
        </ul>
    </div>
</div>
{% endfor %}
