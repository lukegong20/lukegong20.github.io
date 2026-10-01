---
layout: research
title: Learning neural population dynamics across modes
description: Discovering distinct dynamical components across neural trials and conditions through moment-based identification and statistical learning.
permalink: /projects/molds/
research: true
importance: 3
perspective: dynamics-from-data
topic: Learning and inference from neural population data across modes and timescales
label: MoLDS · ICLR 2026
# Export ICLR 2026 Fig. 1 to assets/img/projects/molds-overview.png,
# then set img to that path.
img: ""
image_alt: Overview of a mixture of linear dynamical systems and its application to neural population recordings.
figure_caption: MoLDS models neural trials using a collection of latent dynamical systems, revealing structure across trajectories and experimental conditions.
figure_source_url: https://proceedings.iclr.cc/paper_files/paper/2026/file/84a0b7b706a4783f00762baad845fad9-Paper-Conference.pdf
figure_source_label: Gong and Saxena (2026), Fig. 1
figures:
  # Optional: export Fig. 5c with its ring labels and legend.
  # Set image to assets/img/projects/molds-area2-clusters.png.
  - image: ""
    alt: Polar plots comparing trial clusters across reaching directions in Area2, with Tensor-EM in the outer ring and comparison methods in the inner rings.
    caption: In somatosensory cortex, trial groupings inferred from population dynamics can be compared with the directions of reaching movements.
    source_url: https://proceedings.iclr.cc/paper_files/paper/2026/file/84a0b7b706a4783f00762baad845fad9-Paper-Conference.pdf
    source_label: Gong and Saxena (2026), Fig. 5c
overview: >-
  How can we identify the dynamical systems that generate neural activity when recordings contain several different task conditions? A population may follow one set of dynamics during one type of movement and another set during a different movement. I develop methods that discover these differences directly from the temporal structure of population recordings.
papers:
  - title: Learning Mixtures of Linear Dynamical Systems via Hybrid Tensor-EM Method
    authors: Lulu Gong and Shreya Saxena
    venue: International Conference on Learning Representations (ICLR)
    year: 2026
    url: https://proceedings.iclr.cc/paper_files/paper/2026/hash/84a0b7b706a4783f00762baad845fad9-Abstract-Conference.html
    preprint: https://arxiv.org/abs/2510.06091
    note: Tensor-based identification followed by Kalman EM refinement, with synthetic benchmarks and applications to primate reaching datasets.
---

## Discovering distinct population dynamics

Fitting all trajectories with one model can obscure differences among conditions. Fitting each labeled condition separately, meanwhile, makes it harder to discover groups that differ from the experimental categories.

I study **mixtures of linear dynamical systems (MoLDS)**, in which each trajectory is associated with an unobserved dynamical component. The goal is to estimate these components and infer which trajectories they explain. This groups recordings by their temporal dynamics and lets us examine how the resulting groups relate to behavior. In this model, component identity is fixed within a trajectory; it can differ across trajectories.

## Combining identification and learning

With Shreya Saxena, I introduced **Tensor-EM**, which combines moment-based identification with likelihood-based refinement. The first stage constructs tensors from input-output statistics and uses simultaneous matrix diagonalization to estimate mixture weights and system parameters. Under the model's assumptions, this stage supports identifiable recovery. A subsequent Kalman EM stage refines the latent-state estimates and model parameters using the observed trajectories.

We evaluate recovery in synthetic systems and apply the method to two primate neural datasets collected during reaching tasks. These applications show how a mixture model can reveal condition-related differences in population dynamics.

This project connects a mathematical question—when distinct dynamical systems can be identified from data—to a neuroscience question: how population dynamics vary across behavioral conditions. The complementary [MTS-SLDS project]({{ '/projects/mts-slds/' | relative_url }}) examines multiple decay timescales and regime changes within a recording.
