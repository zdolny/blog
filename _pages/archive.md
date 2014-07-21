---
permalink: archive/
layout: page
title: Archive
---

## Blog Posts

{% for post in site.posts %}
  * {% assign m = post.date | date: "%-m" %}
    {{ post.date | date: "%-d" }}
    {% case m %}
        {% when '1' %}Sty
        {% when '2' %}Lut
        {% when '3' %}Mar
        {% when '4' %}Kwi
        {% when '5' %}Maj
        {% when '6' %}Cze
        {% when '7' %}Lip
        {% when '8' %}Sie
        {% when '9' %}Wrz
        {% when '10' %}Paź
        {% when '11' %}Lis
        {% when '12' %}Gru
    {% endcase %}{{ post.date | date: "%Y" }} 
    &raquo; [ {{ post.title }} ]({{ site.baseurl }}{{ post.url }})
{% endfor %}
