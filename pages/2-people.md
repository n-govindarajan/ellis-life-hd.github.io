---
layout: default
title: People
permalink: /people/
---

**People** at ELLIS Heidelberg 
==============================

The ELLIS unit Heidelberg will foster innovations at the interface of artificial intelligence and machine learning (AI/ML), and the biological and medical sciences. The mission of the unit is to facilitate breakthrough applications of AI/ML, delivering leading-edge analytics to fully exploit the rapidly growing volumes of biomedical data across Europe. The unit will conduct foundational research to address key challenges and obstacles for deploying AI in biomedicine. This includes methods to cope with the heterogeneous and often noisy nature of “omics” data and the scarcity of labeled data in medical imaging, algorithms and infrastructures to deal with ethical and privacy constraints of data access, algorithms to infer causal relationships, as well as novel modelling strategies to deliver interpretable, auditable decisions. 

<div class="container-fluid">
    <div class="row">
        {% for p in site.data.people %}
        <div class="col-xl-3 col-lg-4 col-md-6 col-sm-12 py-vw1">
            <a href="#{{ p.name | slugify }}">
                <div class="people-photowrap">
                    <div class="people-photo"><img src="/assets/img/{{ p.photo }}"></div>
                    <div class="people-name"><p>{% if p.role %}<span class="people-tag">{{ p.role | capitalize }}</span><br>{% endif %}{{ p.name }}</p></div>
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
        <div class="col-3 pl-4">
            <div class="people-photowrap">
                <div class="people-photo"><img src="/assets/img/{{ p.photo }}"></div>
                <div class="people-name">
                    <p>
                    {% if p.role %}<span class="people-tag">{{ p.role | capitalize }}</span><br>{% endif %}
                    {{ p.name }}
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
</div>
{% endfor %}
