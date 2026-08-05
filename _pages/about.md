---
permalink: /
title: "Haoyu Liu"
hide_title: true
description: "Haoyu Liu is a Ph.D. candidate at Nanyang Technological University working on scalable graph algorithms, graph neural networks, Personalized PageRank, and Graph-LLM integration."
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

{% include base_path %}

<style>
  #main .page {
    width: 100%;
    float: none;
    margin: 0;
    padding: 0;
  }

  @media (min-width: 80em) {
    #main {
      max-width: 1380px;
    }
  }
</style>

<div class="home-page">
  <section class="home-hero" aria-labelledby="home-title">
    <div class="home-hero__profile">
      <img src="{{ base_path }}/images/avatar.png" alt="Portrait of Haoyu Liu" fetchpriority="high">
    </div>
    <div class="home-hero__main">
      <p class="home-kicker">Computer Science · Algorithms &amp; Efficiency</p>
      <h1 id="home-title">Haoyu Liu</h1>
      <p class="home-hero__lead">Ph.D. candidate in Computer Science at <a href="https://www.ntu.edu.sg/computing">NTU CCDS</a>, working with <a href="https://siqiangluo.com/">Prof. Siqiang Luo</a> in Singapore.</p>
      <p class="home-hero__copy">I design scalable graph algorithms and efficient learning methods for large, dynamic graphs. My research spans Personalized PageRank, graph kernels, approximation algorithms, and data structures, alongside lightweight and heterophilous Graph Neural Networks and spectral benchmarking. More recently, I have worked on Graph-LLM integration and temporal retrieval, with a consistent focus on reducing computation and memory while preserving theoretical guarantees and practical effectiveness.</p>
      <div class="home-actions">
        <a class="home-action home-action--primary" href="{{ base_path }}/publications/">Browse publications <span aria-hidden="true">↗</span></a>
        <a class="home-action" href="{{ base_path }}/cv/">View CV <span aria-hidden="true">↗</span></a>
        <a class="home-action" href="mailto:haoyu.liu@ntu.edu.sg">Email me <span aria-hidden="true">↗</span></a>
      </div>
    </div>

    <aside class="home-hero__aside" aria-label="Current position">
      <p class="home-hero__aside-label">Now</p>
      <p class="home-hero__aside-title">Ph.D. candidate</p>
      <p class="home-hero__aside-copy">Computer Science<br>NTU CCDS · Singapore</p>
      <div class="home-hero__aside-rule"></div>
      <p class="home-hero__aside-label">Research lens</p>
      <p class="home-hero__aside-stat">Theory → efficiency → impact</p>
    </aside>
  </section>

  <section class="home-section home-context" aria-labelledby="context-title">
    <div class="home-context__column">
      <p class="home-kicker">01 / Background</p>
      <h2 id="context-title">From statistics to graph algorithms.</h2>
      <div class="home-timeline">
        <div class="home-timeline__item">
          <span class="home-timeline__year">Now</span>
          <div><h3>Ph.D. in Computer Science</h3><p><a href="https://www.ntu.edu.sg/">Nanyang Technological University</a>, Singapore · advised by <a href="https://siqiangluo.com/">Prof. Siqiang Luo</a>.</p></div>
        </div>
        <div class="home-timeline__item">
          <span class="home-timeline__year">Earlier</span>
          <div><h3>Research Intern</h3><p>AI Lab, <a href="https://research.samsung.com/src-b">Samsung Research China - Beijing</a>, under <a href="https://scholar.google.com/citations?hl=en&amp;user=EpG5ODwAAAAJ&amp;view_op=list_works&amp;sortby=pubdate">Dr. Yang Liu</a>. Worked on embodied AI agents and household instruction following.</p></div>
        </div>
        <div class="home-timeline__item">
          <span class="home-timeline__year">Foundation</span>
          <div><h3>B.Sc. in Statistics and Big Data</h3><p><a href="http://stat.ruc.edu.cn/">Renmin University of China</a>.</p></div>
        </div>
      </div>
    </div>

    <div class="home-context__column home-context__column--award">
      <p class="home-kicker">02 / Recognition</p>
      <h2>Research that travels.</h2>
      <div class="home-award">
        <span class="home-award__icon"><i class="fa fa-trophy" aria-hidden="true"></i></span>
        <div><strong>Best Newcomer Research Paper Award</strong><p>SIGMOD/PODS 2026 · for <em>Near-Optimality for Single-Source Personalized PageRank</em></p></div>
      </div>
      <div class="home-award">
        <span class="home-award__icon"><i class="fa fa-trophy" aria-hidden="true"></i></span>
        <div><strong>PREMIA Best Student Paper Award</strong><p>2025 in Singapore · for the spectral GNN benchmark study</p></div>
      </div>
      <div class="home-award home-award--quiet">
        <span class="home-award__icon"><i class="fa fa-star" aria-hidden="true"></i></span>
        <div><strong>3rd place, CVPR 2022 ALFRED Challenge</strong><p>For embodied vision-and-language interaction agents.</p></div>
      </div>
    </div>
  </section>

  <section class="home-section home-publications" aria-labelledby="selected-publications-title">
    <div class="home-section__heading home-section__heading--row home-publications__heading">
      <div class="home-publications__heading-copy">
        <p class="home-kicker">03 / Publications</p>
        <h2 id="selected-publications-title">Recent work</h2>
        <p>Selected papers from my publication record.</p>
      </div>
      <a class="home-section__link" href="{{ base_path }}/publications/">View all publications <span aria-hidden="true">↗</span></a>
    </div>

    <p class="home-publications__legend"><strong>†</strong> alphabetical author order <span>·</span> <strong>*</strong> equal contribution</p>

    {% assign homepage_year_groups = site.publications | group_by_exp: "publication_year", "item.date | date: '%Y'" | sort: "name" | reverse %}
    {% assign homepage_displayed = 0 %}
    <div class="home-publication-list">
      {% for year_group in homepage_year_groups %}
        {% assign homepage_year_publications = year_group.items | sort: "date" | reverse %}
        {% assign homepage_lead_publications = homepage_year_publications | where: "first_author", true %}
        {% assign homepage_coauthor_publications = homepage_year_publications | where: "first_author", false %}
        {% for post in homepage_lead_publications %}
          {% if homepage_displayed < 8 %}
            {% include home-publication-entry.html %}
            {% assign homepage_displayed = homepage_displayed | plus: 1 %}
          {% endif %}
        {% endfor %}
        {% for post in homepage_coauthor_publications %}
          {% if homepage_displayed < 8 %}
            {% include home-publication-entry.html %}
            {% assign homepage_displayed = homepage_displayed | plus: 1 %}
          {% endif %}
        {% endfor %}
      {% endfor %}
    </div>
  </section>

  <section class="home-contact" aria-labelledby="contact-title">
    <div>
      <p class="home-kicker">Open to conversations</p>
      <h2 id="contact-title">Have a graph problem worth scaling?</h2>
      <p>I am happy to discuss algorithms, efficiency, and collaboration at the intersection of graph data and machine learning.</p>
    </div>
    <div class="home-contact__links">
      <a href="mailto:haoyu.liu@ntu.edu.sg"><i class="fa fa-envelope" aria-hidden="true"></i> haoyu.liu@ntu.edu.sg</a>
      <a href="https://scholar.google.com/citations?hl=zh-CN&amp;user=DI_fmh0AAAAJ&amp;view_op=list_works&amp;sortby=pubdate"><i class="ai ai-google-scholar" aria-hidden="true"></i> Google Scholar</a>
      <a href="https://github.com/hyLiu-777"><i class="fab fa-github" aria-hidden="true"></i> GitHub</a>
      <a href="https://www.linkedin.com/in/haoyu-liu-9070a932b/"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>
      <a href="https://orcid.org/0000-0002-0839-5460"><i class="ai ai-orcid" aria-hidden="true"></i> ORCID</a>
    </div>
  </section>
</div>
