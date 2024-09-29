---
page_id: publications
layout: page
permalink: /pubs/
title: Recherche et publications
sections:
  - bibquery: "@unpublished"
    text: "Articles soumis"
  - bibquery: "@inproceedings"
    text: "Actes de colloques"
  - bibquery: "@misc"
    text: "Communications orales et par affiche"
years: [2024, 2023]
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{%- for section in page.sections %}
  <a id="{{section.text}}"></a>
  <p class="bibtitle">{{section.text}}</p>
  {%- for y in page.years %}

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count --file papers_fr --locale fr -q {{section.bibquery}}[year={{y}}] -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount !="0" %}

      {% bibliography --file papers_fr --locale fr -q {{section.bibquery}}[year={{y}}] %}

    {%- endif -%}

  {%- endfor %}

{%- endfor %}

</div>
