---
title: "Real-time glare detection and luminance reconstruction"
excerpt: "A deep-learning workflow for reconstructing fisheye luminance maps from a single low-dynamic-range image."
collection: project
status: "Published research"
period: "Jul 2022 - Mar 2023"
header:
  teaser: "projects/luminance-reconstruction/cover.jpg"
---

## Overview

Conventional visual-comfort assessment often depends on high-dynamic-range image capture and time-consuming calibration. This project investigated a faster image-based workflow for reconstructing luminance information from a single exposure.

<figure class="fig">
  <img src="/images/projects/luminance-reconstruction/overview.jpg" alt="Grid of fisheye scenes comparing the input image, reference luminance map, and reconstructions from several methods in false colour.">
  <figcaption>Reconstructed luminance maps compared with the reference across a range of indoor daylight scenes.</figcaption>
</figure>

## Method

A two-step network, SingleLM-Net, was developed to transform a low-dynamic-range fisheye image into a luminance map suitable for visual-comfort analysis. The first stage restores information in under- and overexposed regions using a generative adversarial network; the second reconstructs luminance values with a U-Net-based model. Training and evaluation used a dataset of 884 scenes, each assembled from 15 exposure levels.

<figure class="fig">
  <img src="/images/projects/luminance-reconstruction/pipeline.png" alt="Diagram showing a low dynamic range fisheye image passing through an LDR-GAN and a reconstruction network to produce a luminance map.">
  <figcaption>SingleLM-Net: a single low dynamic range fisheye image is restored, then converted to a luminance map.</figcaption>
</figure>

<figure class="fig">
  <img src="/images/projects/luminance-reconstruction/network.png" alt="Architecture of the generative adversarial network with downsampling and upsampling paths and residual blocks.">
  <figcaption>Architecture of the restoration stage, which recovers detail in under- and overexposed regions.</figcaption>
</figure>

## Key findings

The method achieved a peak signal-to-noise ratio of 59.24 and an R² of 0.9054 for daylight glare probability on the test set. It processed each image in approximately 0.1 seconds on an RTX 2060 GPU and reduced processing time by up to 95 times compared with the conventional HDR workflow.

<figure class="fig">
  <img src="/images/projects/luminance-reconstruction/validation.png" alt="Scatter plot of vertical illuminance from the reconstructed HDR image against illuminance meter readings, with an R-squared of 0.9411.">
  <figcaption>Field validation against illuminance-meter readings (R² = 0.9411).</figcaption>
</figure>

## Contribution

Conceptualization, data curation, methodology, software, visualization, and original-draft writing.

## Related output

- [Automation in Construction article](https://doi.org/10.1016/j.autcon.2024.105294)
- [Code and dataset](https://github.com/ShikangWen2000/SingleLM-Net)
