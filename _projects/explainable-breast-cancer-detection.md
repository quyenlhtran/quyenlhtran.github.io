---
layout: page
title: Explainable Breast Cancer Detection Model
summary: In this work, we build a Vision Transformer with attention maps for explainable breast cancer prediction.
importance: 4
period: Mar–Oct 2025
context: Independent Research
preview: /assets/img/projects/breast-attention-correct-1.png
preview_alt: Mammogram prediction with its Vision Transformer attention map
icon: fa-solid fa-microscope
accent: "#3e718b"
accent_light: "#76a8ba"
---

<div class="project-detail-header">
  <p class="project-detail-byline">
    <strong>March–October 2025</strong><span>Independent Research</span><span>Advisor: <a href="https://scholar.google.com/citations?hl=en&amp;user=DoxEPT4AAAAJ">Dr. Mehmet Gulum</a></span><span>Collaborators: <a href="https://scholar.google.com/citations?user=5V6M-kEAAAAJ&amp;hl=en">Hieu Tran</a>, Tri Dang, and Dat Nguyen</span>
  </p>
</div>

## Abstract

In this work, we developed a Vision Transformer for breast cancer prediction with attention-based explanations to help clinicians interpret and verify model predictions.

## Results

<div class="project-figure-gallery project-figure-gallery-balanced">
  <figure>
    <a href="{{ '/assets/img/projects/breast-attention-correct-1.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/breast-attention-correct-1.png' | relative_url }}" alt="Correct benign mammogram prediction with its attention map" loading="lazy">
    </a>
    <figcaption>A correctly classified benign calcification example and the corresponding Vision Transformer attention map.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/breast-attention-malignant.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/breast-attention-malignant.png' | relative_url }}" alt="Malignant mammogram prediction with its attention map" loading="lazy">
    </a>
    <figcaption>A malignant prediction with attention concentrated on a localized region of the mammogram.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/breast-attention-correct-2.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/breast-attention-correct-2.png' | relative_url }}" alt="Second correct benign mammogram prediction with its attention map" loading="lazy">
    </a>
    <figcaption>A second correctly classified benign calcification example with localized model attention.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/breast-attention-error.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/breast-attention-error.png' | relative_url }}" alt="Misclassified malignant mammogram with its attention map" loading="lazy">
    </a>
    <figcaption>A malignant case predicted as benign, included to show a model failure and its diffuse attention pattern.</figcaption>
  </figure>
</div>
