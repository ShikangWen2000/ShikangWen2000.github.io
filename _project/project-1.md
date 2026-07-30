---
title: "Daylight and shading optimization"
excerpt: "A multi-objective framework for comparing shading strategies while balancing glare control and occupants' daylight satisfaction."
collection: project
status: "Published research"
period: "Mar 2021 - Jun 2022"
header:
  teaser: "projects/daylight-shading/cover.jpg"
---

## Overview

This project developed a performance-based framework for selecting and designing shading strategies in a university library. The work balanced glare reduction with satisfactory daylight conditions rather than optimizing either objective in isolation.

<figure class="fig">
  <img src="/images/projects/daylight-shading/overview.jpg" alt="Floor plan of the simulated library reading area, an axonometric view of the building, and photographs of glare conditions at the study desks.">
  <figcaption>The case-study library: simulated region, sensor layout, and observed glare conditions along the west facade.</figcaption>
</figure>

## Method

Annual daylight simulations were combined with an artificial neural network and a multi-objective genetic algorithm. Four strategies - perforated aluminum sheets, vertical slats, and south- or north-facing serrated windows - were evaluated through spatial glare autonomy and a daylight-satisfaction indicator derived from field-survey data.

<figure class="fig">
  <img src="/images/projects/daylight-shading/framework.png" alt="Flow chart linking daylight simulation, neural-network prediction, and the multi-objective genetic algorithm.">
  <figcaption>Three-stage workflow: annual daylight simulation, neural-network surrogate modelling, and multi-objective optimization.</figcaption>
</figure>

<figure class="fig">
  <img src="/images/projects/daylight-shading/shading-devices.png" alt="Parametric diagrams of a perforated aluminum sheet, vertical slats, and serrated windows with their design variables labelled.">
  <figcaption>Design variables of the three shading device families used to generate the search space.</figcaption>
</figure>

## Key findings

The four strategies produced distinct Pareto performance curves. North-facing serrated windows were the most effective at reducing glare, while vertical slats provided the most satisfactory illuminance levels. The near-optimal perforated-sheet, vertical-slat, north-facing serrated-window, and south-facing serrated-window designs reduced the complementary glare indicator by 9%, 22%, 8%, and 8%, respectively, while maintaining daylight satisfaction close to the original space.

<figure class="fig">
  <img src="/images/projects/daylight-shading/pareto-comparison.png" alt="Pareto fronts of the four shading strategies plotted as spatial daylight visual autonomy against spatial glare autonomy.">
  <figcaption>Pareto fronts of the four strategies, compared against the performance of the original space.</figcaption>
</figure>

## Contribution

Conceptualization, data curation, methodology, software, visualization, and original-draft writing.

## Related outputs

- [Journal of Building Engineering article](https://doi.org/10.1016/j.jobe.2022.105532)
- [Building Simulation 2023 conference paper](https://doi.org/10.26868/25222708.2023.1141)
