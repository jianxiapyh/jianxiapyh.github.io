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
    {% if post.citation contains 'ISMAR 2025' %}
      {% assign awards = 'Best Paper Award (ISMAR 2025)' %}
    {% else %}
      {% assign awards = 'Best Paper Award' %}
    {% endif %}
  {% endif %}
  {% if post.citation contains 'IEEE Micro Top Pick' %}
    {% if awards != '' %}
      {% assign awards = awards | append: '; IEEE Micro Top Pick' %}
    {% else %}
      {% assign awards = 'IEEE Micro Top Pick' %}
    {% endif %}
  {% endif %}
  {% assign display_authors = post.authors | replace: 'Y. Pang', '<strong>Y. Pang</strong>' %}
  <div style="margin-bottom: 1rem; font-size: 0.9rem; line-height: 1.35;">
    <div style="font-weight: 600; font-size: 0.98rem;">
      {{ post.title }}
    </div>
    {% if post.authors %}
    <div>{{ display_authors }}</div>
    {% endif %}
    <div>
      {{ post.display_venue | default: post.venue }}
    </div>
    {% if awards != '' %}
    <div><strong>{{ awards }}</strong></div>
    {% endif %}
  </div>
{% endfor %}
