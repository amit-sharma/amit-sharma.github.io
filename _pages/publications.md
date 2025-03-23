---
layout: page
permalink: /publications/
title: publications
description:

nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

An up-to-date list is available at <a href="https://scholar.google.com/citations?user=CXgQufgAAAAJ&hl=en">Google Scholar</a>.

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

### Preprints

<div class="publications"> 
{% bibliography --query @*[status=review] %}

</div>

### Publications

<div class="publications"> 
{% bibliography --query @*[status!=review && status!=unpublished] %}

</div>
