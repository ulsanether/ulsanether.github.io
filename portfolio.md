---
layout: page
title: 완료
permalink: /portfolio/
---
<<<<<<< HEAD
{% for project in site.portfolio reversed %}

  {% if project.redirect %}
    <div class="project">
        <div class="thumbnail">
            <a href="{{ project.redirect }}" target="_blank">
            {% if project.img %}
            <img class="thumbnail" src="{{ project.img }}"/>
            {% else %}
            <div class="thumbnail blankbox"></div>
            {% endif %}    
            <span>
                <h1>{{ project.title }}</h1>
                <br/>
                <p>{{ project.description }}</p>
            </span>
            </a>
        </div>
    </div>

  {% else %}
    <div class="project ">
        <div class="thumbnail">
            <a href="{{ site.baseurl }}{{ project.url }}">
            {% if project.img %}
            <img class="thumbnail" src="{{ project.img }}"/>
            {% else %}
            <div class="thumbnail blankbox"></div>
            {% endif %}    
            <span>
                <h1>{{ project.title }}</h1>
                <br/>
                <p>{{ project.description }}</p>
            </span>
            </a>
        </div>
=======

{% for project in site.portfolio %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
>>>>>>> parent of 08cd726 (Update portfolio.md)
    </div>
</div>

{% endif %}

{% endfor %}
