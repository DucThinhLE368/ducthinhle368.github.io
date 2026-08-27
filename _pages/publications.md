---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 3
toc:
  sidebar: left
---

See [Google Scholar](https://scholar.google.com/citations?user=CYdHeacAAAAJ&hl=en&oi=ao) for the most up-to-date information.

<!-- _pages/publications.md -->

<!-- Stats, computed at build time from _data/citations.yml (auto-refreshed from Google Scholar) -->

{% assign total_papers = 0 %}
{% assign total_citations = 0 %}
{% assign min_year = 9999 %}
{% assign max_year = 0 %}
{% for pair in site.data.citations.papers %}
{% assign total_papers = total_papers | plus: 1 %}
{% assign total_citations = total_citations | plus: pair[1].citations %}
{% assign y = pair[1].year | plus: 0 %}
{% if y < min_year %}{% assign min_year = y %}{% endif %}
{% if y > max_year %}{% assign max_year = y %}{% endif %}
{% endfor %}

{% assign h_index = 0 %}
{% for h in (1..total_papers) %}
{% assign count_ge = 0 %}
{% for pair in site.data.citations.papers %}
{% if pair[1].citations >= h %}
{% assign count_ge = count_ge | plus: 1 %}
{% endif %}
{% endfor %}
{% if count_ge >= h %}
{% assign h_index = h %}
{% endif %}
{% endfor %}

| Publications | Citations | h-index | Active years |
|:---:|:---:|:---:|:---:|
| {{ total_papers }} | {{ total_citations }} | {{ h_index }} | {{ min_year }}&ndash;{{ max_year }} |

## Journal Papers
{: .bibliography }
<div class="publications">

{% bibliography --query @article* --group_by none %}

</div>

## Conference Papers
{: .bibliography }
<div class="publications">

{% bibliography --query @inproceedings* --group_by none %}

</div>

## Submitted
{: .bibliography }
<div class="publications">

{% bibliography --query @unpublished* --group_by none %}

</div>
