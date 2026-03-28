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
  {% assign citation_parts = post.citation | split: '. ' %}
  {% assign pub_authors = citation_parts | first %}
  {% assign award_text = '' %}
  {% if post.citation contains 'Best Paper Award' %}
    {% assign award_text = 'Best Paper Award' %}
  {% endif %}
  <div style="margin-bottom: 1.5rem;">
    <div style="font-weight: 600; font-size: 1.05rem;">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
    {% if pub_authors != blank %}
    <div>{{ pub_authors }}</div>
    {% endif %}
    <div>
      {{ post.venue }}{% if post.date %}, {{ post.date | date: "%Y" }}{% endif %}{% if award_text != '' %}. {{ award_text }}{% endif %}
    </div>
    {% if post.paperurl %}
    <div><a href="{{ post.paperurl }}">[Paper]</a></div>
    {% endif %}
  </div>
{% endfor %}

