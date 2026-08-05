---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p>
  <a href="{{ base_path }}/files/cv.pdf" class="btn btn--primary">Download CV as PDF</a>
</p>

Education
======
* Ph.D. Candidate in Computer Science, Nanyang Technological University, Singapore
* B.Sc. in Statistics, Renmin University of China

Research Interests
======
* Scalable Graph Algorithms
* Graph Neural Networks
* Personalized PageRank (PPR)

Experience
======
* Ph.D. Researcher, Nanyang Technological University
  * Advisor: Prof. Siqiang Luo
  * Research focus: scalable graph algorithms, graph neural networks, and PPR-related topics

* Research Intern, Samsung Research China - Beijing
  * AI Lab, under Dr. Yang Liu

Skills
======
* Graph Algorithms
* Graph Neural Networks
* Personalized PageRank
* Python, Jupyter, Markdown, Git

Publications
======
<ul>
{% assign publications_sorted = site.publications | sort: "date" | reverse %}
{% for post in publications_sorted %}
  {% include archive-single-cv.html show_citation=false %}
{% endfor %}
</ul>
