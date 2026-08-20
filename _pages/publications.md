---
layout: page
permalink: /publications/
title: Research Outputs
description:
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<section class="research-output-section" aria-labelledby="published-work-label">
  <div id="published-work-label" class="research-output-label">Publications</div>
  <div class="publications compact-publications">

{% bibliography --query @article %}

  </div>
</section>

<section class="research-output-section" aria-labelledby="manuscripts-label">
  <div id="manuscripts-label" class="research-output-label">Manuscripts</div>
  <div class="publications compact-publications">

{% bibliography --query @*[category=manuscript]* %}

  </div>
</section>

<section class="research-output-section" aria-labelledby="posters-label">
  <div id="posters-label" class="research-output-label">Posters</div>
  <div class="publications compact-publications">

{% bibliography --query @*[category=poster]* %}

  </div>
</section>
