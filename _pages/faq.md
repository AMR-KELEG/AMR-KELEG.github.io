---
layout: page
title: FAQ
permalink: /faq/
description: My answers to questions that I usually get
nav: true
---

<div class="projects grid">

  {% assign faq = site.faq | sort: "importance" %}
  {% for q in faq %}
  <div class="grid-item">
    {% if q.redirect %}
    <a href="{{ q.redirect }}" target="_blank">
    {% else %}
    <a href="{{ q.url | relative_url }}">
    {% endif %}
      <div class="card hoverable">
        {% if q.img %}
        <img src="{{ q.img | relative_url }}" alt="question thumbnail">
        {% endif %}
        <div class="card-body">
          <h2 class="card-title text-lowercase">{{ q.title }}</h2>
          <p class="card-text">{{ q.description }}</p>
          <div class="row ml-1 mr-1 p-0">
            {% if q.github %}
            <div class="github-icon">
              <div class="icon" data-toggle="tooltip" title="Code Repository">
                <a href="{{ q.github }}" target="_blank"><i class="fab fa-github gh-icon"></i></a>
              </div>
              {% if q.github_stars %}
              <span class="stars" data-toggle="tooltip" title="GitHub Stars">
                <i class="fas fa-star"></i>
                <span id="{{ q.github_stars }}-stars"></span>
              </span>
              {% endif %}
            </div>
            {% endif %}
          </div>
        </div>
      </div>
    </a>
  </div>
{% endfor %}

</div>
