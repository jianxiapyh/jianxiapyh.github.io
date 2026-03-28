---
permalink: /
title: "Welcome"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Thanks for stopping by!

I am a Ph.D. student in Computer Science at the University of Illinois Urbana-Champaign, where I work with Professor Sarita Adve. 

My research focuses on energy-efficient systems for extended reality (XR). 

I received my B.S. and M.S. in Computer Engineering from Virginia Tech.

## Publications

{% if author.googlescholar %}
You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% for post in site.publications reversed %}
  {% assign awards = '' %}
  {% if post.citation contains 'Best Paper Award' %}
    {% assign awards = 'Best Paper Award' %}
  {% endif %}
  {% if post.citation contains 'IEEE Micro Top Pick' %}
    {% if awards != '' %}
      {% assign awards = awards | append: '; IEEE Micro Top Pick' %}
    {% else %}
      {% assign awards = 'IEEE Micro Top Pick' %}
    {% endif %}
  {% endif %}
  <div style="margin-bottom: 1.5rem;">
    <div style="font-weight: 600; font-size: 1.05rem;">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
    {% if post.authors %}
    <div>{{ post.authors }}</div>
    {% endif %}
    <div>
      {{ post.display_venue | default: post.venue }}
    </div>
    {% if awards != '' %}
    <div><strong>{{ awards }}</strong></div>
    {% endif %}
  </div>
{% endfor %}
