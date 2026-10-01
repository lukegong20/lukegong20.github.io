---
layout: research
title: Inferring neural population dynamics across timescales
description: Identifying coexisting fast and slow latent dynamics and characterizing their changes across behavioral regimes.
permalink: /projects/mts-slds/
research: true
importance: 4
perspective: dynamics-from-data
topic: Learning and inference from neural population data across modes and timescales
label: MTS-SLDS · Ongoing work
# Export panel C of your existing fig_S1_recovery_v2.pdf, including its legend,
# to assets/img/projects/mts-slds-timescale-recovery.png, then set img below.
# This manuscript figure has no public source URL yet.
img: ""
image_alt: Synthetic recovery of three latent timescales, comparing ground truth with MTS-SLDS, SLDS, and autocorrelation-based estimates.
figure_caption: Recovery of three latent timescales in synthetic data, comparing model-based estimates and an autocorrelation-based estimate with ground truth. From an ongoing manuscript.
figure_source_url: ""
figure_source_label: ""
overview: >-
  Neural population activity contains fluctuations that evolve over different timescales. Some modes decay quickly, while others persist over longer intervals. These temporal properties can also change during behavior. I am developing methods to identify multiple latent timescales from population recordings and characterize how they vary across dynamical regimes.
resources_note: This project is ongoing. Manuscript and code links will be added when publicly available.
---

## From population recordings to latent timescales

The central idea is to infer population dynamics before extracting their timescales. In a **multi-timescale switching linear dynamical system (MTS-SLDS)**, a low-dimensional latent state evolves according to a regime-specific transition matrix. Gaussian or Poisson observation models connect that state to continuous measurements or spike counts. One regime describes a single set of latent dynamics; several regimes allow the dynamics to change within a recording.

For a decaying eigenmode of a fitted transition matrix, its eigenvalue determines the relaxation timescale:

<div class="research-equation" role="math" aria-label="Tau equals negative delta t divided by log of the magnitude of lambda, for lambda magnitude strictly between zero and one.">
  &tau; = &minus;&Delta;t / log|&lambda;|, &nbsp; 0 &lt; |&lambda;| &lt; 1.
</div>

Here, &Delta;t is the sampling interval and &lambda; is a transition eigenvalue. This timescale describes decay with the regime held fixed. Complex eigenvalues additionally encode oscillation. Several modes can coexist within one regime, and their decay timescales differ from the duration for which that regime remains active.

## Learning dynamics across regimes

My approach combines **multi-lag moment initialization** with **regime-conditioned Laplace EM**. The initialization uses temporal structure in the observations. The refinement stage retains regime dependence in the latent-state statistics used to update the model; Poisson observations use local Laplace approximations. I evaluate the approach through synthetic recovery experiments and neural recordings from visual and somatosensory cortex.

## Interpreting the estimates

These are **effective dynamical timescales**. Without additional assumptions or interventions, they do not separate intrinsic circuit dynamics from unobserved input-driven effects. This distinction guides the interpretation of the estimates and future work on stimulus- and input-dependent dynamics.

For a related published approach to differences across trials and conditions, see the [MoLDS project]({{ '/projects/molds/' | relative_url }}).
