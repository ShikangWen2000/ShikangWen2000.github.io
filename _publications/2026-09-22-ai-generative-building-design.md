---
title: "An AI-assisted workflow for generative building design and energy modeling: Converting natural language design intent and images into 3D building energy model inputs"
permalink: /publication/2026-ai-generative-building-design
redirect_from:
  - /publication/2026-2d-to-3d-building-design
excerpt: "An AI-assisted workflow that converts natural language design intent and images into EnergyPlus-compatible 3D building energy model inputs."
date: 2026-09-22
venue: "Advanced Engineering Informatics"
type: "Journal article"
paperurl: "https://doi.org/10.1016/j.aei.2026.105313"
citation: "Wen, S., & Chen, Q. (2027). An AI-assisted workflow for generative building design and energy modeling: Converting natural language design intent and images into 3D building energy model inputs. Advanced Engineering Informatics, 77, 105313."
---

## Abstract

Building energy use contributes substantially to carbon emissions. Integrating conceptual design with building energy modeling can support energy-efficient design, yet few studies have connected artificial intelligence (AI)-assisted generative design with building energy simulation while explicitly converting generative outputs into EnergyPlus-compatible geometry. This study presents an AI-assisted workflow that translates high-level design intent into building energy model (BEM) geometry inputs. In the workflow, ChatGPT-image generates or preprocesses 2D architectural representations, Hunyuan3D-2.1 reconstructs 3D geometry, and a mesh-to-EnergyPlus method converts the reconstructed mesh into simulation-ready geometry. A graph neural network (GNN) classifier trained on a purpose-built synthetic dataset of 13,000 buildings classifies mesh faces into building components. The workflow was evaluated using multiple footprint shapes at three scales across five Chinese climate zones, and its practical applicability was demonstrated through image-based reconstruction and text-driven design exploration for a campus office building in Hong Kong. Across the multi-scale synthetic cases, deterministic calibration kept the target gross floor area (GFA) and window-to-wall ratio (WWR) close to their prescribed values, while energy use intensity (EUI) remained consistent with manually created reference models under identical boundary conditions. The workflow was further demonstrated by reconstructing a Hong Kong campus office building from a single image and generating six alternative designs from one constrained prompt. These results support the use of generative AI to connect unstructured design intent and visual inputs with structured BEM geometry for rapid, energy-oriented design exploration.
