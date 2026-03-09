---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D. Candidate in Computer Science, Nanyang Technological University (NTU), Singapore
* B.Sc. in Statistics, Renmin University of China

Work experience
======
* Ph.D. Researcher, Nanyang Technological University
  * Research focus: scalable graph algorithms, graph neural networks, and Personalized PageRank (PPR)
  * Advisor: Prof. Siqiang Luo

* Research Intern, Samsung Research China - Beijing
  * Research mentorship: Dr. Yang Liu

Skills
======
* Graph Algorithms
* Graph Neural Networks
* Personalized PageRank (PPR)
* Python, Jupyter, Markdown, Git

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
{% assign talk_count = site.talks | size %}
{% if talk_count > 0 %}
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
{% else %}
No talks added yet.
{% endif %}
  
Teaching
======
{% assign teaching_count = site.teaching | size %}
{% if teaching_count > 0 %}
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% else %}
No teaching entries added yet.
{% endif %}
  
Service and leadership
======
* Reviewer and collaborator in data management and graph learning communities
