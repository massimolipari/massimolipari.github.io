---
page_id: publications
layout: page
permalink: /pubs/
title: Publications
sections:
  - bibquery: "@article"
    text: "Articles de revue"
  - bibquery: "@inbook"
    text: "Chapitres de livres numériques"
  - bibquery: "@inproceedings"
    text: "Actes de colloques"
years: ["Soumis", 2025, 2024, 2023]
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

    {%- comment -%}  Count bibliography in actual section and year {%- endcomment -%}
    {%- capture citecount -%}
    {%- bibliography_count --file papers_fr -q {{section.bibquery}}[year={{y}}] -%}
    {%- endcapture -%}

    {%- comment -%} If exist bibliography in actual section and year, print {%- endcomment -%}
    {%- if citecount != "0" %}

      {% bibliography --file papers_fr -q {{section.bibquery}}[year={{y}}] %}

    {%- endif -%}

  {%- endfor %}

{%- endfor %}

</div>
