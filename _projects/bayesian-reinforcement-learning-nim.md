---
layout: page
title: Bayesian Reinforcement Learning for the n-Pile Nim Game
summary: In this work, I study whether Bayesian reinforcement learning can recover the mathematical structure of optimal Nim play.
importance: 1
period: Jan–May 2026
context: Math Senior Seminar
preview: /assets/img/projects/nim-optimal-action-map.png
preview_alt: Learned optimal-action structure for the two-pile Nim setting
icon: fa-solid fa-chess-knight
accent: "#3f5f9e"
accent_light: "#7192d0"
links:
  - label: Code
    url: https://github.com/quyenlhtran/bayesian-rl-nim
    icon: fa-brands fa-github
  - label: Manuscript
    url: /assets/pdf/nim-bayesian-rl.pdf
    icon: fa-regular fa-file-pdf
---

<div class="project-detail-header">
  <p class="project-detail-byline"><strong>January–May 2026</strong><span>Math Senior Seminar, DePauw University</span></p>
  <div class="project-detail-actions">
    <a href="https://github.com/quyenlhtran/bayesian-rl-nim"><i class="fa-brands fa-github" aria-hidden="true"></i> View on GitHub</a>
    <a href="{{ '/assets/pdf/nim-bayesian-rl.pdf' | relative_url }}"><i class="fa-regular fa-file-pdf" aria-hidden="true"></i> View manuscript</a>
  </div>
</div>

## Abstract

Machine learning and reinforcement learning methods have achieved strong empirical performance across many applications, including game playing. However, this also raises concerns about the reliability, interpretability, and safety of model decisions, thereby motivating the study of learning algorithms in settings where the underlying problem structure is mathematically understood. Combinatorial games provide a useful setting for studying these questions because many admit mathematically characterized optimal strategies. Therefore, this paper uses the n-pile Nim game as a mathematically structured environment for studying Bayesian reinforcement learning through random-walk Metropolis Markov Chain Monte Carlo (MCMC) methods. The paper investigates how probabilistic posterior sampling over policy parameters influences the learned strategy and whether the resulting policy can recover the known combinatorial structure of optimal play. By combining theoretical analysis and empirical experiments, the paper shows that the proposed Bayesian reinforcement learning framework is able to recover the combinatorial structure underlying optimal play in the Nim game and achieve strong gameplay performance across multiple game settings.

## Results

<div class="project-figure-gallery">
  <figure>
    <a href="{{ '/assets/img/projects/nim-learned-policy.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/nim-learned-policy.png' | relative_url }}" alt="Learned-policy behavior for two-pile Nim, including posterior feature weights, optimal-action structure, and gameplay performance" loading="lazy">
    </a>
    <figcaption>Learned-policy behavior for the two-pile Nim setting, including posterior feature weights and optimal-action structure.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/nim-performance.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/nim-performance.png' | relative_url }}" alt="Nim win-rate and runtime comparisons across methods" loading="lazy">
    </a>
    <figcaption>Win rate and runtime across Bayesian MCMC, classical search, reinforcement-learning, and rule-based baselines.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/nim-feature-ablation.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/nim-feature-ablation.png' | relative_url }}" alt="Nim feature-ablation results" loading="lazy">
    </a>
    <figcaption>Feature-ablation results showing the role of nim-sum-related features in gameplay and optimal-action accuracy.</figcaption>
  </figure>
</div>
