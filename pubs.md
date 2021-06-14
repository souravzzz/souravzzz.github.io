---
layout: page
title: Publications
permalink: /pubs/
---

<ul class="publications">
{% for paper in site.data.papers %}

  {% if paper.title and paper.title != "" %}
  <li class="article">

      {% if paper.link and paper.link != "" %}
      <a class="page-link active" href="{{paper.link}}">
      {% endif %}
      <span class="title"> {{ paper.title }} </span>
      {% if paper.link and paper.link != "" %}
      </a>
      {% endif %}

      <span class="authors"> {{ paper.authors }} </span>

      {% if paper.award and paper.award != "" %}
      <span class="award"> [{{ paper.award }}] </span>
      {% endif %}

      <span class="journal"> {{ paper.journal }}, {{ paper.date }}. </span>

      {% if paper.asset and paper.asset != "" %}
      <a class="page-link active" href="{{paper.asset}}">&nbsp; 💾 &nbsp;</a>
      {% endif %}
    </li>
    {% endif %}

{% endfor %}
</ul>
