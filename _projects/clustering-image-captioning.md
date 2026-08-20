---
layout: page
title: Clustering-Based Lightweight Architecture for Image Captioning
summary: In this work, we test whether clustering can make image captions more specific and context-aware.
importance: 2
period: Jan–May 2026
context: Data Mining
preview: /assets/img/projects/captioning-examples.jpeg
preview_alt: Examples comparing global and cluster-specific image captions
icon: fa-solid fa-images
accent: "#366b8c"
accent_light: "#72a8c7"
links:
  - label: Code
    url: https://github.com/quyenlhtran/image-captioning
    icon: fa-brands fa-github
  - label: Manuscript
    url: /assets/pdf/image-captioning.pdf
    icon: fa-regular fa-file-pdf
---

<div class="project-detail-header">
  <p class="project-detail-byline">
    <strong>January–May 2026</strong><span>Data Mining Course Project, DePauw University</span><span>Collaborator: Hung Nguyen</span>
  </p>
  <div class="project-detail-actions">
    <a href="https://github.com/quyenlhtran/image-captioning"><i class="fa-brands fa-github" aria-hidden="true"></i> View on GitHub</a>
    <a href="{{ '/assets/pdf/image-captioning.pdf' | relative_url }}"><i class="fa-regular fa-file-pdf" aria-hidden="true"></i> View manuscript</a>
  </div>
</div>

## Abstract

Recent advances in vision–language models have significantly improved image captioning performance; however, existing systems often produce generic or semantically shallow descriptions, particularly when trained on large and non-uniform datasets. In this work, we propose a clustering-based framework for image captioning that organizes image–caption pairs into semantically coherent groups prior to model training. We then train a cluster-conditioned caption generation model that leverages cluster identity as additional contextual information, enabling more specialized and context-aware caption generation. We evaluate our approach on the Microsoft COCO dataset with BLEU, ROUGE-L, and METEOR across three models: ViT-GPT2, GIT, and BLIP. The results show that clustering does not consistently improve overall performance compared to training on the full dataset, with mixed results depending on the model and metric. However, when we look more closely at individual examples, we find that clustering can help generate more specific and relevant captions in certain cases.

## Results

<div class="project-figure-gallery">
  <figure>
    <a href="{{ '/assets/img/projects/captioning-examples.jpeg' | relative_url }}">
      <img src="{{ '/assets/img/projects/captioning-examples.jpeg' | relative_url }}" alt="Qualitative comparison of global and clustered image captions" loading="lazy">
    </a>
    <figcaption>Qualitative examples comparing globally trained and cluster-specific captions across ViT-GPT2, GIT, and BLIP.</figcaption>
  </figure>
</div>
