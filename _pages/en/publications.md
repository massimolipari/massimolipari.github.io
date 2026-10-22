---
page_id: publications
layout: page
permalink: /pubs/
title: Publications
sections:
  - bibquery: "@article"
    text: "Journal articles"
  - bibquery: "@inebook,@incollection"
    text: "Book chapters"
  - bibquery: "@inproceedings"
    text: "Conference proceedings"
years: ["Accepted", "In revision", "Submitted", 2026, 2025, 2024, 2023]
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{%- for section in page.sections %}
  <a id="{{section.text}}"></a>
  <p class="bibtitle">{{section.text}}</p>
  {%- for y in page.years %}

    {%- comment -%} Build query: apply the year filter to each type in bibquery {%- endcomment -%}
    {%- assign types = section.bibquery | split: "," -%}
    {%- capture query -%}{%- for t in types -%}{{ t | strip }}[year={{y}}] {% endfor -%}{%- endcapture -%}

    {%- capture citecount -%}
    {%- bibliography_count -f {{site.scholar.bibliography}} -q {{query}} -%}
    {%- endcapture -%}

    {%- if citecount != "0" %}
      {% bibliography -f {{site.scholar.bibliography}} -q {{query}} %}
    {%- endif -%}

  {%- endfor %}

{%- endfor %}

</div>
