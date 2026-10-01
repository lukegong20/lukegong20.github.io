---
layout: research
title: Nonlinear dynamics and control of biological systems
description: Understanding how population–environment feedback shapes stability and oscillations, and how interventions can regulate these dynamics.
permalink: /projects/eco-evolution/
research: true
importance: 1
perspective: nonlinear-dynamics
topic: Nonlinear dynamics and control of biological systems
label: Eco-evolutionary systems · PhD research
# Export Automatica Fig. 1 to assets/img/projects/eco-evolution-feedback.png,
# then set img to that path. Blank image fields render nothing.
img: ""
image_alt: Feedback between population strategy dynamics and environmental resources through resource-dependent payoffs.
figure_caption: Population strategies change the environment, while environmental conditions change the incentives that drive strategy selection.
figure_source_url: https://doi.org/10.1016/j.automatica.2022.110536
figure_source_label: Gong et al. (2022), Fig. 1
figures:
  # Optional result image from Automatica Fig. 3.
  # Set image to assets/img/projects/eco-evolution-bifurcation.png after adding it.
  - image: ""
    alt: Bifurcation diagram showing equilibrium and stable limit-cycle branches as the mutation rate changes.
    caption: Changing the mutation rate reshapes stable oscillations and eventually stabilizes the equilibrium in a coupled population–environment system.
    source_url: https://doi.org/10.1016/j.automatica.2022.110536
    source_label: Gong et al. (2022), Fig. 3
overview: >-
  When interacting processes change one another, feedback can stabilize a system or produce persistent oscillations. During my PhD at the University of Groningen, I studied these questions in eco-evolutionary systems, where population behavior and environmental resources co-evolve. Evolutionary game theory, bifurcation analysis, and control provided a way to connect the structure of this feedback to its long-term consequences.
papers:
   

  - title=Strong anti-Hebbian plasticity alters the convexity of network attractor landscapes
    authors: Lulu Gong and Xudong Chen and ShiNung Ching
    year: 2025
    url: https://ieeexplore.ieee.org/document/10981480
    note: Bifurcation analysis of neural-synpatic recurrent network dynamics
    
  - title: Limit cycles analysis and control of evolutionary game dynamics with environmental feedback
    authors: Lulu Gong, Weijia Yao, Jian Gao, and Ming Cao
    venue: Automatica, 145, 110536
    year: 2022
    url: https://doi.org/10.1016/j.automatica.2022.110536
    pdf: /assets/pdf/1-s2.0-S0005109822003971-main.pdf
    preprint: https://arxiv.org/abs/2205.10734
    note: Bifurcation analysis of replicator–mutator dynamics with environmental feedback, stable limit cycles, and incentive-based control.
  - title: Different Environment Feedback in Fast-Slow Eco-Evolutionary Dynamics and Resulting Limit Cycles
    authors: Lulu Gong and Ming Cao
    venue: IEEE Control Systems Letters, 6, 1184–1189
    year: 2022
    url: https://doi.org/10.1109/LCSYS.2021.3089989
    preprint: https://arxiv.org/abs/2105.04659
    note: How different resource feedback mechanisms shape oscillatory dynamics. Published online in 2021.
  - title: Limit Cycles in Replicator-Mutator Dynamics with Game-Environment Feedback
    authors: Lulu Gong, Weijia Yao, Jian Gao, and Ming Cao
    venue: IFAC-PapersOnLine, 53(2), 2850–2855
    year: 2020
    url: https://doi.org/10.1016/j.ifacol.2020.12.955
  - title: Evolutionary Dynamics of Two Communities Under Environmental Feedback
    authors: Yu Kawano, Lulu Gong, Brian D. O. Anderson, and Ming Cao
    venue: IEEE Control Systems Letters, 3(2), 254–259
    year: 2019
    url: https://doi.org/10.1109/LCSYS.2018.2866775
    note: Published online in 2018.
  - title: Evolutionary Game Dynamics for Two Interacting Populations in a Co-evolving Environment
    authors: Lulu Gong, Jian Gao, and Ming Cao
    venue: IEEE Conference on Decision and Control, 3535–3540
    year: 2018
    url: https://doi.org/10.1109/CDC.2018.8619801
    preprint: https://arxiv.org/abs/1806.03194
---

## Feedback, stability, and oscillations

The models describe how the frequencies of competing strategies evolve alongside environmental resources. My work asks when the coupled system settles to an equilibrium, when it develops persistent oscillations, and how the feedback mechanism changes these outcomes. Stability analysis and bifurcation theory explain the behavior observed in simulations and identify the conditions under which it changes.

## From mathematical analysis to control

In our *Automatica* paper, we analyzed replicator–mutator dynamics with environmental feedback. We established conditions for Hopf and heteroclinic bifurcations that generate stable limit cycles and studied their persistence and stability. We also examined an incentive-based control policy, connecting the mathematical analysis to interventions that change the long-term behavior of the coupled system.

Related work investigates how resource dynamics and timescale separation affect these conclusions. Comparing self-renewing and externally supplied resources reveals that systems with similar equilibrium structure can exhibit different global oscillatory behavior. Earlier studies extend the analysis to two interacting populations or communities, where environmental feedback can support recurrent collective dynamics.

## A foundation for modeling biological systems

This research established the mathematical foundation for my broader work on biological dynamics. Questions about feedback, stability, and separated timescales also motivate my [models of neuron–astrocyte networks]({{ '/projects/astrocyte-neuron/' | relative_url }}), where the focus shifts from population–environment interactions to the mechanisms supporting adaptive computation.
