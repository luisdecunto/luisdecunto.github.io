---
layout: page
title: XFEM Hydraulic Fracturing Simulation
description: MATLAB implementation of Extended Finite Element Method for fluid-structure interaction in hydraulic fracturing
img: assets/img/xfem_thumb.jpg
importance: 3
category: Computational Mechanics
---

## Project Overview

This project implements a **complete numerical simulation** of **hydraulic fracturing** using the **Extended Finite Element Method (XFEM)** in MATLAB. The code simultaneously solves:
- ✅ Solid deformation (rock mechanics)
- ✅ Fluid flow (pressure field in fractures)
- ✅ Crack propagation (dynamic fracture mechanics)

This was my **final undergraduate project** at Instituto Tecnológico de Buenos Aires (ITBA), demonstrating the complexity of coupled multi-physics simulations.

## What is Hydraulic Fracturing?

Hydraulic fracturing (fracking) is a technique used to extract oil and gas by:
1. Injecting high-pressure fluid into rock formations
2. Creating fractures in the rock
3. Allowing trapped hydrocarbons to flow

**Engineering Challenge:** Predicting crack paths and required injection pressures requires solving a complex **fluid-structure interaction (FSI)** problem.

## Technical Approach

### Extended Finite Element Method (XFEM)

Traditional FEM requires remeshing as cracks grow. **XFEM** overcomes this by:
- Enriching shape functions to capture discontinuities
- Allowing cracks to propagate through elements
- No remeshing required during simulation

### Mathematical Formulation

The coupled problem involves:

**1. Solid Mechanics (Elasticity):**
- Equilibrium equations: ∇·σ = 0
- Constitutive model: σ = C:ε
- Displacement field u(x,y)

**2. Fluid Flow (Lubrication Theory):**
- Reynolds equation for thin film flow
- Pressure-driven flow in fracture: q = -k∇p
- Fluid continuity: ∇·q = 0

**3. Fracture Mechanics:**
- Stress intensity factors (K_I, K_II)
- Crack growth criterion (K > K_c)
- Crack direction based on maximum hoop stress

### Implementation Highlights

**MATLAB Code Features:**
- Fully coded from scratch (no external FEM libraries)
- Iterative solver for coupled FSI problem
- Crack tip enrichment functions
- Automatic crack propagation algorithm
- Post-processing and visualization

**Key Algorithms:**
1. **Newton-Raphson** for nonlinear solid mechanics
2. **Level set method** for tracking crack geometry
3. **Conjugate gradient** solver for large sparse systems
4. **Adaptive time stepping** for stability

## Results & Validation

### Validation Cases
- ✅ Compared with analytical solutions (penny-shaped crack)
- ✅ Benchmarked against literature results
- ✅ Mesh convergence studies

### Key Findings
- Successfully predicted crack initiation and propagation
- Captured pressure distribution in fracture
- Demonstrated coupling between fluid pressure and solid deformation

## Technical Skills Demonstrated

**Numerical Methods:**
- Finite Element Method (FEM)
- Extended Finite Element Method (XFEM)
- Iterative solvers for large systems
- Fluid-Structure Interaction (FSI)

**Programming:**
- MATLAB advanced features (sparse matrices, vectorization)
- Algorithm optimization for computational efficiency
- Scientific visualization
- Code documentation and testing

**Mathematical Modeling:**
- Linear elasticity
- Fracture mechanics
- Fluid mechanics
- Coupled multi-physics problems

## Challenges Overcome

1. **Coupling complexity** - Solid and fluid physics have different time scales
2. **Numerical stability** - Iterative convergence required careful parameter tuning
3. **Crack propagation** - Implementing robust criteria for crack direction
4. **Computational cost** - Optimizing MATLAB code for reasonable run times

## Applications

This simulation framework is applicable to:
- **Oil & Gas** - Hydraulic fracturing optimization
- **Geothermal Energy** - Enhanced geothermal systems
- **Civil Engineering** - Dam stability, concrete cracking
- **Materials Science** - Composite delamination

## Future Enhancements

If continuing this project:
- 3D extension (currently 2D)
- Multiple crack interaction
- Poroelasticity (fluid flow in porous media)
- Parallel computing for larger problems

---

**Project Period:** 2017 - 2018
**Institution:** Instituto Tecnológico de Buenos Aires (ITBA)
**Supervisor:** PhD Sebastián D'hers
**Grade:** Excellent

<!-- Add code snippets or visualizations when available -->
<!--
```matlab
% Example: XFEM enrichment function
function [N_enriched] = xfem_enrichment(x, y, crack_tip)
    % Level set functions
    phi = signed_distance(x, y, crack_tip);
    psi = tangential_distance(x, y, crack_tip);

    % Heaviside enrichment (discontinuity across crack)
    H = sign(phi);

    % Crack tip enrichment (near-tip asymptotic fields)
    r = sqrt(phi^2 + psi^2);
    theta = atan2(phi, psi);
    F = [sqrt(r)*sin(theta/2), sqrt(r)*cos(theta/2), ...
         sqrt(r)*sin(theta/2)*sin(theta), sqrt(r)*cos(theta/2)*sin(theta)];

    N_enriched = [H, F];
end
```
-->
