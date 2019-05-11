---
layout: page
title: Appartement à louer - Agadir Maroc
permalink: /appartements/
---

<p>Nous vous proposons toute l'année 3 appartements à louer à Agadir (Maroc) près de la plage. Les appartements sont tous équipés (draps, couvertures, eau chaude, vaisselle, cuisine équipée...).</p>

<p>Venez profiter d'Agadir, une station balnéaire familiale agréable l'été comme l'hiver: Bienvenue chez vous à Agadir, rien à dire comme diraient les locaux ! </p>
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
    </div>
</div>

{% endif %}

{% endfor %}