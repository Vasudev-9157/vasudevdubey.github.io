---
layout: post
title: "Constraining the Equation of State of Neutron Stars"
date: 2025-06-10
status: "Completed"
duration: "2023-2024"
collaborators: "Dr. Rahul Kashyap, Yugesh Bhoge, Ish Gupta"
---

## Overview

In this study, we aim to constrain the **Equation of State (EoS)** of neutron stars by using data from **Neutron Star-Black Hole (NSBH) mergers**. By leveraging **Bayesian Inference** methods, we analyze how different EoS models influence the tidal properties of neutron stars and their detection in gravitational wave signals.

The core objective is to assess the **tidal deformability** of neutron stars, which is sensitive to the EoS. The analysis of tidal deformability using gravitational waves provides insight into the star's internal structure and the nuclear matter properties under extreme conditions.

### Scientific Motivation

Neutron stars are dense remnants of massive stars, and their EoS plays a crucial role in determining their mass-radius relationship, thermal properties, and other structural details. By observing **tidal deformability** during mergers, we can better understand their internal composition.

\[
\Lambda = \frac{2}{3} \frac{c^2}{G} \left( \frac{R}{M} \right) ^5
\]
Where \( R \) is the radius and \( M \) is the mass of the neutron star.

---

## Methodology

### Bayesian Inference with BILBY

We applied a **Bayesian Inference** framework to estimate the posterior distribution of physical parameters in the NSBH system. Using the **BILBY library**, we incorporated prior knowledge about the binary components and the EoS to explore the system's properties through simulated gravitational wave data.

Our analysis was based on multiple **gravitational waveform models**:
- **IMRPhenomNSBH** for asymmetric binaries (where \( q < 0.6 \))
- **IMRPhenomPv2_NRTidalv2** for symmetric binaries (where \( q > 0.6 \))

---

### Tidal Deformability

We used the **effective tidal deformability** parameter, \( \Lambda_{\text{eff}} \), to quantify the tidal response of the neutron star. This value plays a critical role in distinguishing between **NSBH** and **BNS** (binary neutron star) mergers.

\[
\Lambda_{\text{eff}} = \frac{(1 + 2q) \Lambda_1 + q \Lambda_2}{(1 + q)^2}
\]

Where \( \Lambda_1 \) and \( \Lambda_2 \) are the tidal deformabilities of the individual components, and \( q \) is the mass ratio.

---

## Results

### Posterior Distributions

Our Bayesian analysis provided the posterior distributions of several key parameters, such as the **chirp mass**, **mass ratio**, and **tidal deformability**. The results are shown below:

![Posterior Distribution of Chirp Mass](assets/images/posterior_mass.png)
*Figure: Posterior distribution of chirp mass from the analysis.*

![Posterior Distribution of Tidal Deformability](assets/images/posterior_deformability.png)
*Figure: Posterior distribution of tidal deformability \( \Lambda_{\text{eff}} \).*

### EOS Models Comparison

We compared multiple EoS models, including **APR4**, **SLy**, and **DD2**, and assessed how they affect the tidal deformability and other neutron star properties.

![EOS Models Comparison](assets/images/eos_comparison.png)
*Figure: Comparison of different EoS models and their effect on neutron star radius and mass.*

---

### Computational Challenges

The primary computational challenge was the high dimensionality of the parameter space. We used the **Dynesty** sampler to efficiently explore the space and accurately estimate the posterior distributions.

---

## Applications and Implications

This study's findings have important implications for **gravitational wave astronomy**:
- **EoS Constraints**: The results help refine the neutron star EoS and provide a better understanding of their internal structure.
- **Distinguishing NSBH and BNS Mergers**: The effective tidal deformability \( \Lambda_{\text{eff}} \) serves as a distinguishing feature between these two types of mergers.

---

## Full Report

📄 [Download the full research report (PDF)](/assets/research/Master_Thesis_Report.pdf)

---

## Publications

**"Constraining the Equation of State of Neutron Stars using NSBH mergers"**  
*V. Dubey et al.*, (2025) - *In Preparation*

---

"The violent universe becomes comprehensible through careful simulation and patient analysis."
