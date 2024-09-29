---
page_id: publications
layout: page
permalink: /pubs/
title: Recherche et publications
years: [2024, 2023]
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography --locale fr --type_names {unpublished: Sousmis, article: Articles de revue, inproceedings: Actes de colloque, misc: Commnunications orales et par affiche} %}

</div>
