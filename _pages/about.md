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
  {% assign award_text = '' %}
  {% assign pub_year = '' %}
  {% if post.date %}
    {% assign pub_year = post.date | date: "%Y" %}
  {% endif %}
  {% if post.citation contains 'Best Paper Award' %}
    {% assign award_text = 'Best Paper Award' %}
  {% endif %}
  <div style="margin-bottom: 1.5rem;">
    <div style="font-weight: 600; font-size: 1.05rem;">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
    {% if post.authors %}
    <div>{{ post.authors }}</div>
    {% endif %}
    <div>
      {{ post.short_venue | default: post.venue }}{% if pub_year != '' and post.short_venue and post.short_venue contains pub_year == false %}, {{ pub_year }}{% elsif pub_year != '' and post.short_venue == nil and post.venue contains pub_year == false %}, {{ pub_year }}{% endif %}
    </div>
    {% if award_text != '' %}
    <div><strong>{{ award_text }}</strong></div>
    {% endif %}
    {% if post.paperurl %}
    <div><a href="{{ post.paperurl }}">[Paper]</a></div>
    {% endif %}
  </div>
{% endfor %}
