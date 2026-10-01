---
layout: research
title: Adaptive computation in neuron–astrocyte networks
description: Understanding how interactions among neurons, synapses, and astrocytes support learning across contexts and timescales.
permalink: /projects/astrocyte-neuron/
research: true
importance: 2
perspective: adaptive-computation
topic: Dynamical models of adaptive computation in neuron–astrocyte networks
label: Neuron–astrocyte networks
# Export PLOS Computational Biology Fig. 1A–C to
# assets/img/projects/astrocyte-network.png, then set img to that path.
img: ""
image_alt: A tripartite synapse, a neuron–astrocyte hypernetwork, and feedback among neurons, synapses, and astrocytes.
figure_caption: Neurons, plastic synapses, and astrocytes form interacting feedback loops that connect circuit structure to context-dependent dynamics.
figure_source_url: https://doi.org/10.1371/journal.pcbi.1012186.g001
figure_source_label: Gong et al. (2024), Fig. 1A–C
figures:
  # Optional: export Fig. 4A and 4C together, retaining their legends.
  # Set image to assets/img/projects/astrocyte-learning.png.
  - image: ""
    alt: Learning performance in a changing bandit task and its dependence on separation of neuronal and astrocytic timescales.
    caption: The model connects adaptation in a changing bandit task with the separation of neuronal and astrocytic timescales.
    source_url: https://doi.org/10.1371/journal.pcbi.1012186.g004
    source_label: Gong et al. (2024), Fig. 4A and 4C
  # Optional collaborative preprint figure, March 18, 2026 revision: Fig. 4a–d.
  # Set image to assets/img/projects/astrocyte-actor-critic.png.
  - image: ""
    alt: Neuron–astrocyte actor–critic model and its heterogeneous activity during a learned sequence task.
    caption: A neuron–astrocyte actor–critic model develops fast transients and slower task-related activity during learning. Collaborative preprint.
    source_url: https://doi.org/10.64898/2026.01.05.697758
    source_label: Li et al. (2026), Fig. 4a–d
overview: >-
  How do feedback and interactions across timescales support adaptive behavior? I investigate this question through mechanistic models of neurons, plastic synapses, and astrocytes. By connecting circuit dynamics to learning tasks, I study how these interacting components help a network retain contextual information and adapt its decisions when the environment changes.
papers:
  - title: Astrocytes as a mechanism for contextually-guided network dynamics and function
    authors: Lulu Gong, Fabio Pasqualetti, Thomas Papouin, and ShiNung Ching
    venue: PLOS Computational Biology, 20(5), e1012186
    year: 2024
    url: https://doi.org/10.1371/journal.pcbi.1012186
    pdf: /assets/pdf/journal.pcbi.1012186.pdf
    code: https://github.com/lukegong20/Neuro-astrocyte-networks-and-Multi-armed-bandits
    note: A dynamical model of neuron–synapse–astrocyte interactions, mathematical analysis, and learning in context-dependent bandit tasks.
  - title: Multi-timescale Computation by Astrocytes
    authors: Chang Li, Lulu Gong, Chenghui Song, ShiNung Ching, Lucas Pozzo-Miller, and Wei Li
    venue: bioRxiv
    year: 2026
    kind: Preprint
    url: https://doi.org/10.64898/2026.01.05.697758
    note: Collaborative experimental and computational work connecting fast and slow astrocytic activity to reward-guided behavior and an actor–critic network model.
---

## Context-dependent network dynamics

In our *PLOS Computational Biology* study, I developed and analyzed a dynamical model of neuron–synapse–astrocyte interactions. Astrocytic activity modulates synaptic adaptation and responds to neural activity and contextual inputs. This creates nested feedback loops whose components evolve at different rates. Mathematical analysis shows how slowly varying astrocytic signals can alter the attractor structure of faster neural and synaptic dynamics.

We then trained these networks on bandit tasks with changing contexts. The model links astrocytic modulation to learning in nonstationary environments, providing a mechanistic example of how slower biological processes can support flexible behavior. My contributions included model formulation, mathematical analysis, software, and computational experiments.

## Connecting models with experimental observations

In a subsequent collaboration, I contributed computational modeling and analysis to a study of multi-timescale astrocytic computation during reward-guided behavior. Experimental collaborators characterized fast and slow calcium signals in cerebellar astrocytes and their distinct relationships to behavior. A neuron–astrocyte actor–critic network trained on a related sequence task developed heterogeneous temporal activity resembling these observed patterns.

The collaborative study remains a preprint. Its actor–critic interpretation provides a computational hypothesis for the observed division of function, linking state evaluation and the modulation of neuronal learning.

Together, these projects connect mechanistic modeling with reinforcement learning and experimental neuroscience. They use explicit interactions among neurons, synapses, and astrocytes to test how biological architecture can support contextual adaptation.

My complementary work on [learning dynamical components from neural population data]({{ '/projects/molds/' | relative_url }}) and [inferring their timescales]({{ '/projects/mts-slds/' | relative_url }}) asks how recordings can reveal dynamical structure when the underlying mechanisms are not directly observed.
