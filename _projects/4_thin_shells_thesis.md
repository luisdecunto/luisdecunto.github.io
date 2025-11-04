---
layout: page
title: Stress Localization in Thin Shells
description: Master's thesis on numerical study of stress concentration in thin shell structures using FEM and differential geometry
img: assets/img/thin_shells_thumb.jpg
importance: 4
category: Computational Mechanics
---

## Project Overview

My **Master's thesis** at Aarhus University explored **stress localization phenomena** in thin shell structures—a critical issue in engineering design where stress concentrates in small regions, potentially causing failure. This research combined **Finite Element Analysis**, **differential geometry**, and **mathematical modeling**.

## Research Motivation

Thin shells (structures where thickness << other dimensions) are ubiquitous:
- 🚗 **Automotive** - Car body panels
- ✈️ **Aerospace** - Aircraft fuselages, wing skins
- 🏗️ **Civil** - Domes, shells, pressure vessels
- 📦 **Packaging** - Cans, bottles, containers

Understanding where and why stress concentrates is essential for:
- Preventing catastrophic failures
- Optimizing material usage
- Designing efficient lightweight structures

## Research Objectives

1. Develop **high-fidelity FEM models** of thin shell structures
2. Analyze **stress localization patterns** in different geometries
3. Create a **curvature calculation method** based on FEM data
4. Investigate the relationship between **geometry and stress distribution**

## Technical Approach

### Case Studies Analyzed

**Case 1: Pressurized Cylinder with Geometric Defect**
- Studied how imperfections cause stress concentration
- Analyzed effect of defect size and shape
- Validated against analytical solutions

**Case 2: Shell with Sharp Crease**
- Investigated localization at geometric discontinuities
- Examined the role of curvature in stress distribution
- Compared different loading conditions

### Novel Methodology: Curvature from FEM Data

Developed a computational method to extract **Gaussian and mean curvature** directly from FEM displacement fields:

**Challenge:** Standard FEM gives displacements at nodes, but curvature requires second derivatives of the surface.

**Solution:** Applied **differential geometry** to discrete FEM data:
1. Reconstruct surface from nodal displacements
2. Compute first fundamental form (metric tensor)
3. Calculate second fundamental form (curvature tensor)
4. Extract principal curvatures κ₁ and κ₂
5. Compute Gaussian (K = κ₁κ₂) and mean (H = (κ₁+κ₂)/2) curvatures

This enabled **direct correlation** between local geometry and stress state.

## Key Findings

### 1. Geometry-Stress Relationship
- Stress localization **strongly correlates** with curvature changes
- Regions of high Gaussian curvature show elevated stress
- Sharp creases create **singular stress concentrations**

### 2. Localization Mechanisms
- **Geometric discontinuities** are primary drivers of localization
- **Boundary conditions** significantly influence stress patterns
- **Material thickness** plays crucial role in localization width

### 3. Predictive Capability
- Curvature analysis can **predict localization zones** without full stress analysis
- Useful for **preliminary design** optimization

## Technical Implementation

**Software & Tools:**
- **ABAQUS** - FEM simulations (shell elements)
- **Python** - Post-processing, curvature calculations
- **MATLAB** - Data analysis and visualization
- **ParaView** - 3D visualization of results

**Key Techniques:**
- Nonlinear geometric analysis (large deformations)
- Shell theory (Kirchhoff-Love, Mindlin-Reissner)
- Differential geometry on discrete surfaces
- Mesh convergence studies

## Mathematical Framework

**Governing Equations:**
- Equilibrium: ∇·σ + f = 0
- Shell kinematics: Kirchhoff-Love hypotheses
- Constitutive law: σ = E/(1-ν²) [ε + ν trace(ε)I]

**Curvature Tensor:**
```
b_αβ = -n · ∂²r/∂u^α∂u^β
```
where n is the surface normal and r is the position vector.

**Gaussian Curvature:**
```
K = det(b_αβ) / det(g_αβ)
```

## Impact & Applications

This research contributes to:
- **Better design guidelines** for thin shell structures
- **Early detection** of potential failure zones
- **Optimization algorithms** that account for stress localization
- **Understanding fundamental mechanics** of thin structures

## Skills Demonstrated

**Technical:**
- Advanced Finite Element Analysis
- Differential geometry and tensor calculus
- Numerical analysis and scientific computing
- Mathematical modeling of physical systems

**Research:**
- Literature review and synthesis
- Experimental design and validation
- Data analysis and interpretation
- Technical writing and presentation

**Programming:**
- Python scientific stack (NumPy, SciPy, Matplotlib)
- MATLAB for data processing
- ABAQUS Python API for automation
- Visualization and post-processing

## Future Research Directions

- Extend to **inelastic materials** (plasticity, viscoelasticity)
- Incorporate **material microstructure** effects
- Apply **machine learning** to predict localization from geometry
- Study **dynamic loading** scenarios

## Academic Output

**Thesis:** "Numerical Study of Stress Localization in Thin Shells"
**Grade:** High honors
**Supervisor:** PhD Marcelo A. Dias (now at University of Edinburgh)

---

**Project Period:** 2020 - 2021
**Institution:** Aarhus University
**Degree:** M.Sc. in Mechanical Engineering
