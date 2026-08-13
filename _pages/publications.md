---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

You can find all of my articles on <a href="https://orcid.org/0009-0008-7975-5997" target="_blank">my ORCID profile</a>.

(* = equal contribution)

{% include base_path %}

---

## 🔍 Social AI for Older Adults

{% assign publicationsByYear = site.publications | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in publicationsByYear reversed %}
<!--   <h1 style="margin: 1.5em 0px -0.5em; padding: 0px; color: brown;">{{ year.name }}</h1> -->
  {% assign publicationsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in publicationsByMonth reversed %}
    {% for post in month.items reversed %}
      {% if post.selected == "true" %}
        {% if post.topic == "fact_faith" %}
          {% include archive-single.html %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endfor %}


## 🔍 Masculinity

{% assign publicationsByYear = site.publications | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in publicationsByYear reversed %}
<!--   <h1 style="margin: 1.5em 0px -0.5em; padding: 0px; color: brown;">{{ year.name }}</h1> -->
  {% assign publicationsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in publicationsByMonth reversed %}
    {% for post in month.items reversed %}
      {% if post.selected == "true" %}
        {% if post.topic == "fairness" %}
          {% include archive-single.html %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endfor %}


