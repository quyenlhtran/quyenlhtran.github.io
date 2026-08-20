---
layout: page
title: Statistical Structure of Random Event Sequences
summary: In this work, I study finite-sample methods for ranking and predicting random event sequences.
importance: 5
period: Aug 2024–Apr 2025
context: Independent Research
preview: /assets/img/projects/random-prediction-distribution.png
preview_alt: Distribution of final cumulative accuracy across one thousand simulations
icon: fa-solid fa-chart-line
accent: "#34598a"
accent_light: "#7091bc"
links:
  - label: Prediction paper
    url: /assets/pdf/predicting-outcomes.pdf
    icon: fa-regular fa-file-lines
  - label: Ranking paper
    url: /assets/pdf/ranking-events.pdf
    icon: fa-regular fa-file-lines
---

<div class="project-detail-header">
  <p class="project-detail-byline">
    <strong>August 2024–April 2025</strong><span>Independent Research</span><span>Advisor: <a href="https://science.indianapolis.iu.edu/people-directory/people/sarkar-jyoti.html">Dr. Jyotirmoy Sarkar</a></span>
  </p>
</div>

## Papers

[Predicting Outcomes of Random Phenomena]({{ '/assets/pdf/predicting-outcomes.pdf' | relative_url }})  
[Ranking Events Based on a Random Sample]({{ '/assets/pdf/ranking-events.pdf' | relative_url }})

## Abstract

This project began by asking how observed data should be used to predict the next outcome of a random process. We compared fixed, adaptive, memory-based, and randomized prediction strategies for categorical and real-valued outcomes under several loss functions. That work led to a related question: because effective prediction often depends on identifying which outcomes are more likely, how much data is needed before a ranking based on observed frequencies can be trusted? We then developed exact and simulation-based methods for determining the probability of a correct ranking and the sample size required to reach a desired level of confidence.

## Predicting the next outcome

We first compared strategies that always make one prediction, estimate probabilities after an initial sample, update estimates continuously, repeat or avoid the latest outcome, or randomize. In the three-outcome experiment with probabilities \((0.5, 0.3, 0.2)\), the estimate-based strategies converge to an accuracy near 0.50, while repeat adherence reaches about 0.38, uniform randomization reaches about 0.33, and repeat avoidance reaches about 0.31. The prediction results show that a useful rule should depend on both the observed data and the cost assigned to different errors. Across the settings we studied, adding unrelated randomness did not improve prediction performance.

<div class="project-figure-gallery project-figure-gallery-balanced">
  <figure>
    <a href="{{ '/assets/img/projects/random-prediction-accuracy.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/random-prediction-accuracy.png' | relative_url }}" alt="Cumulative accuracy of six prediction strategies over two thousand three-outcome predictions" loading="lazy">
    </a>
    <figcaption>Cumulative accuracy over 2,000 predictions shows the data-driven strategies approaching the best attainable accuracy.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/random-prediction-distribution.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/random-prediction-distribution.png' | relative_url }}" alt="Distribution of final cumulative accuracy for six prediction strategies over one thousand simulations" loading="lazy">
    </a>
    <figcaption>Across 1,000 simulations, estimate-based strategies remain concentrated near 0.50 and outperform randomized and short-memory alternatives.</figcaption>
  </figure>
</div>

## Ranking events from a finite sample

Observed frequencies are natural estimates of unknown event probabilities, but small samples can produce ties or reverse the true order. For three outcomes, the possible frequency triples form a triangular lattice. Partitioning this support by the six possible orderings—and accounting for ties—allows us to compute the exact probability that sorting the observed frequencies produces the correct ranking.

<div class="project-figure-gallery">
  <figure>
    <a href="{{ '/assets/img/projects/random-ranking-support.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/random-ranking-support.png' | relative_url }}" alt="Three-outcome multinomial support represented in three dimensions and as a partitioned triangular lattice" loading="lazy">
    </a>
    <figcaption>The multinomial support for three outcomes and its partition into regions used to calculate ranking probabilities.</figcaption>
  </figure>
</div>

The same calculation reveals how ranking confidence changes across the parameter space. When the true probabilities are \((0.37, 0.33, 0.30)\), at least 2,210 observations are needed to reach a 95% probability of recovering the complete ordering. The required sample grows quickly when the probabilities become closer because the categories are harder to distinguish.

<div class="project-figure-gallery">
  <figure>
    <a href="{{ '/assets/img/projects/random-ranking-contour.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/random-ranking-contour.png' | relative_url }}" alt="Triangular parameter space and contour plot of correct three-outcome ranking probabilities" loading="lazy">
    </a>
    <figcaption>For a sample of 100 observations, the contour plot maps the probability of correctly concluding that \(p &gt; q &gt; r\) across the corresponding region of the parameter space.</figcaption>
  </figure>
</div>
