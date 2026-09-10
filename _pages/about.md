---
permalink: /
title: "About Me"
excerpt: "Systems for spatial computing and embodied AI, scalable infrastructure, and algorithm–system co-design."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Ph.D. student in Computer Science at the University of Illinois Urbana-Champaign, advised by Professor Sarita Adve. I expect to graduate in **May 2027**.

My research focuses on **systems for spatial computing and embodied AI**, with interests in scalable infrastructure, algorithm–system co-design, and distributed systems. I build energy-efficient XR systems that balance power, latency, and quality, including **Boba** for physics-based Gaussian digital twins and **Ada** for real-time scene provisioning. I also contribute to the Illinois Extended Reality Testbed (ILLIXR) and have collaborated with Meta Reality Labs since 2024.

In summer 2026, I was a Ph.D. intern on **NVIDIA's XR team**, working on scalable ML training and data infrastructure for 3D hand reconstruction. Previously, I received my B.S. and M.S. in Computer Engineering from Virginia Tech, where I worked with Professor Binoy Ravindran during my master's studies.

[CV (September 2026, PDF)]({{ '/files/Yihan_Pang_cv_Sept2026.pdf' | relative_url }}) · [Email](mailto:{{ site.author.email }}){% if site.author.googlescholar %} · [Google Scholar]({{ site.author.googlescholar }}){% endif %}

{% assign publications = site.publications | sort: 'date' | reverse %}
{% assign selected_publications = publications | where: 'selected', true %}

## Selected Publications

{% include publication-list.html publications=selected_publications %}

## Other Publications

{% assign other_publications = publications | where_exp: 'publication', 'publication.selected != true' %}
{% include publication-list.html publications=other_publications %}

## Manuscripts Under Review

{% include publication-list.html publications=site.data.manuscripts %}
