---
title: "Supernova Afterglow Simulations"
layout: post
date: 2024-08-20
status: "Completed"
duration: "May-July, 2024"
collaborators: "Dept. of Astronomy, Astrophysics and Space Engineering (DAASE), IIT Indore"
---

Gamma-Ray Bursts (GRBs) are among the most luminous explosions in the universe. They originate from catastrophic events such as massive stellar collapses or compact-object mergers, and were first discovered serendipitously by the Vela satellites in 1967. The afterglow emission that follows a GRB provides valuable information about the physics of ultra-relativistic jets and shock waves. Studying GRB afterglows is scientifically valuable: it sheds light on high-energy processes not reproducible on Earth, constrains models of stellar evolution and cosmic expansion, and is linked to gravitational wave sources. Despite their distance and high energies, GRBs pose no threat to Earth, and their study enriches our understanding of the cosmos.

## Scientific Motivation
The key reasons to simulate GRB afterglows include:
- **Ultra-relativistic jet physics:** Investigate shock propagation and jet interaction with the external medium.
- **Astrophysical environments:** Constrain models of massive star collapse and neutron star mergers.
- **Cosmology and evolution:** Use GRBs as probes of the early universe and cosmic expansion.
- **Multi-messenger astronomy:** Relate GRB jets to gravitational wave events from compact mergers.

## Simulation Framework

### Hydrodynamic Code & Visualization Software
We use state-of-the-art computational fluid dynamics codes:
- **PLUTO**: Modular code for computational astrophysics
- **Custom Solvers**: Specialized Riemann solvers for shock physics
- **VisIt**: Open Source, interactive, scalable, visualization, animation and analysis tool for large datasets

### Setup
We used the PLUTO code configured for special relativistic hydrodynamics in spherical coordinates. The computational grid is two-dimensional (radius *r* and polar angle *θ*) with *r* ∈ [1,1000] and *θ* ∈ [0,π/2]. The system is axisymmetric about the polar axis and symmetric about the equatorial plane, effectively modeling a conical jet slice. The simulation runs up to *t* = 10<sup>4</sup> (dimensionless units), saving outputs every Δ*t* = 100 (100 total snapshots). At *r* = 1 we impose a time-dependent jet inflow boundary (jet "nozzle"), and at the outer radius we use an outflow boundary. Reflecting boundaries are applied at θ = 0 and θ = π/2 to enforce symmetry.

Initial conditions include a relativistic jet region between *r* = 50 and *r* = 100 with a higher density and velocity than the surrounding medium. Specifically, the jet density is set to twice the ambient (ejecta) density, with a radial velocity *v* ≈ 0.1c and pressure *p* = 10<sup>-4</sup> of the jet pressure in this region. The ambient medium (ejecta) is initially at rest and denser, representing the interstellar environment. Two cases are simulated: a fast jet with Lorentz factor γ ≈ 50 and a slower jet with γ = 20. The table below summarizes the key parameters.

- **Geometry:** 2D spherical (r,θ), axisymmetric (no φ-dependence).
- **Grid Range:** r = 1 to 1000, θ = 0 to π/2.
- **Time Domain:** t<sub>max</sub> = 10<sup>4</sup> with Δt = 100 (100 outputs).
- **Jet Region:** 50 < r < 100; density = 2 × ambient, v = 0.1c, p = 10<sup>-4</sup> (jet).
- **Lorentz Factors:** γ ≈ 50 (fast case) and γ = 20 (slow case).

<img src="/assets/images/research/afterglow/Sedov%20model.png" alt="Initial density and pressure profiles for the GRB jet simulation (fast jet, γ ≈ 50)." style="max-width:70%;height:auto;display:block;margin:0.5rem auto;" />

## Main Results

The simulations reveal a dynamic interaction between the relativistic jet and the external medium. A strong forward shock propagates into the ambient ejecta, while a reverse shock travels back into the jet material. The jet drives a hot, over-pressured cocoon around the propagation axis. The following figures illustrate the time evolution of these quantities.

<img src="/assets/images/research/afterglow//beta=0.9998 evolutions.png" alt="Evolution of density in the relativistic jet and ambient medium (fast jet case, γ=50)." style="max-width:70%;height:auto;display:block;margin:0.5rem auto;" />
*Figure: Density snapshots (normalized) at times t = 100, 1000, 5000, 8000, 10000 for the fast jet (γ=50). A clear forward shock and cocoon are visible.*

In the fast jet case (γ ≈ 50), the maximum velocity approaches the speed of light. The shear at the jet boundary produces Kelvin–Helmholtz instabilities, evident as wavy structures along the interface. In the slower jet case (γ = 20), the jet advances more slowly and the resulting cocoon is broader and less collimated. The slower jet produces a weaker forward shock; internal shocks are more pronounced.

<img src="/assets/images/research/afterglow//gamma=20 evolutions.png" alt="Evolution of Density, Pressure and Velocity for slow jets γ=20." style="max-width:70%;height:auto;display:block;margin:0.5rem auto;" />  
*Figure: The slow jet yields a weaker shock and more diffuse cocoon.*

<video width="640" height="480" controls>
  <source src="/assets/images/research/afterglow/beta=0.9998_Density_Corrected.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Video: Animation of the GRB afterglow simulation.*


## Computational Challenges

This project pushes the boundaries of computational astrophysics:
- **Resolution**: Simulations with up to 10<sup>9</sup> computational cells
- **Timesteps**: Following evolution for 10,000+ years
- **Physics**: Coupling hydrodynamics, radiation, and magnetic fields

## Applications

### Observational Predictions
- X-ray emission profiles for comparison with Chandra observations
- Radio synchrotron emission from accelerated particles
- Infrared dust emission from processed materials

### Theoretical Insights
- Understanding shock acceleration mechanisms
- Quantifying element mixing in ejecta
- Predicting long-term remnant structure


## Future Directions

- Extension to Type Ia supernova explosions
- 3D simulations with full MHD physics
- Integration with stellar evolution codes


## Full Report

📄 **[Download Complete Research Report (PDF)]({{ '/assets/research/Supernova_afterglow_simulations_report.pdf' | relative_url }})**

---

*"The violent universe becomes comprehensible through careful simulation and patient analysis."*
