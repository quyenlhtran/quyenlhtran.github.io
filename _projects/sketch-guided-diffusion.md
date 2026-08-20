---
layout: page
title: Sketch-Guided Diffusion for Image-to-Image Generation
summary: In this work, I compare generative models for sketch- and text-guided image generation.
importance: 3
period: Sep–Dec 2025
context: Deep Learning
preview: /assets/img/projects/diffusion-results.png
preview_alt: Sketch-guided image generation results across model architectures
icon: fa-solid fa-wand-magic-sparkles
accent: "#4c5793"
accent_light: "#858fc6"
links:
  - label: Code
    url: https://github.com/quyenlhtran/final_project
    icon: fa-brands fa-github
  - label: Manuscript
    url: /assets/pdf/sketch-text-guided-diffusion.pdf
    icon: fa-regular fa-file-pdf
---

<div class="project-detail-header">
  <p class="project-detail-byline"><strong>September–December 2025</strong><span>Deep Learning Course Project, Budapest Semesters in Mathematics</span></p>
  <div class="project-detail-actions">
    <a href="https://github.com/quyenlhtran/final_project"><i class="fa-brands fa-github" aria-hidden="true"></i> View on GitHub</a>
    <a href="{{ '/assets/pdf/sketch-text-guided-diffusion.pdf' | relative_url }}"><i class="fa-regular fa-file-pdf" aria-hidden="true"></i> View manuscript</a>
  </div>
</div>

## Abstract

This work investigates diffusion-based image generation from sketch and text inputs. Using the DDPM framework, the denoising process is conditioned on a Canny-edge sketch, a CLIP text embedding, and the diffusion timestep. Three backbone architectures—U-Net, ResNet, and DiT—are trained under identical settings to isolate architectural differences. Due to computational constraints, training is performed at a small resolution and for a limited number of epochs. As a result, the outputs are preliminary but still informative. Qualitative results indicate that AE and VAE models tend to produce blurred images, while diffusion-based approaches preserve more structural detail from the sketch and capture richer color variations from the caption. These early findings suggest the potential of sketch- and text-guided diffusion models for producing images with more artist-like structure and interpretability.

## Results

<div class="project-figure-gallery project-figure-gallery-balanced">
  <figure>
    <a href="{{ '/assets/img/projects/diffusion-results.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/diffusion-results.png' | relative_url }}" alt="Sketch-guided image-generation results across model architectures" loading="lazy">
    </a>
    <figcaption>Qualitative outputs from baseline models and diffusion backbones for representative sketch–caption pairs.</figcaption>
  </figure>
  <figure>
    <a href="{{ '/assets/img/projects/diffusion-loss-curves.png' | relative_url }}">
      <img src="{{ '/assets/img/projects/diffusion-loss-curves.png' | relative_url }}" alt="Training and validation loss curves for generative models" loading="lazy">
    </a>
    <figcaption>Training and validation loss curves for the autoencoder, VAE, GAN, and diffusion variants.</figcaption>
  </figure>
</div>
