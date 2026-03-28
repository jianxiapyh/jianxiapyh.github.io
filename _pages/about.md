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
  {% include archive-single.html %}
{% endfor %}


