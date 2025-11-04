---
layout: page
title: KurvedWind - ML Surrogate Modeling
description: FEM simulation and machine learning surrogate model for spring-back prediction in thermoforming processes
img: assets/img/kurvedwind_thumb.jpg
importance: 1
category: Machine Learning
---

## Project Overview

The **KurvedWind Project** combines advanced **Finite Element Modeling (FEM)** with **Machine Learning** to predict spring-back behavior in thermoforming processes of foam core materials. This project demonstrates the power of surrogate modeling to accelerate engineering workflows.

## Challenge

Traditional FEM simulations of thermoforming processes are computationally expensive, often taking hours to complete. Engineers need rapid predictions during the design phase to:
- Optimize process parameters
- Predict final part geometry
- Reduce trial-and-error iterations

## Solution

Developed a hybrid approach combining physics-based simulation with data-driven ML:

### 1. FEM Simulation Development
- Built high-fidelity FEM models of the thermoforming process
- Simulated material behavior under various temperature and pressure conditions
- Validated models against experimental data

### 2. Machine Learning Surrogate Model
- Generated training dataset from FEM simulations (500+ runs)
- Trained ML model to predict spring-back displacement
- Achieved **1000x speedup** compared to full FEM simulation
- Maintained high accuracy (R² > 0.95)

### 3. Technical Reports & Documentation
- Authored comprehensive technical reports
- Documented methodology for future research

## Technical Details

**Tools & Technologies:**
- **FEM Software:** ABAQUS
- **Programming:** Python (scikit-learn, NumPy, pandas)
- **ML Techniques:** Gaussian Process Regression, Neural Networks
- **Visualization:** Matplotlib, Seaborn

**Key Features:**
- Nonlinear material modeling
- Temperature-dependent properties
- Contact mechanics
- Large deformation analysis

## Impact

- ⚡ **Reduced computation time** from 2 hours → 0.1 seconds per prediction
- 📊 **Enabled real-time design optimization** during engineering meetings
- 🎯 **Improved accuracy** of spring-back predictions compared to analytical models
- 💡 **Demonstrated feasibility** of ML-augmented engineering workflows

## Skills Demonstrated

- Finite Element Analysis (FEA)
- Machine Learning model development
- Surrogate modeling (Gaussian Processes)
- Data preprocessing and feature engineering
- Model validation and uncertainty quantification
- Technical documentation and reporting

## Future Work

- Extend model to handle multiple material types
- Incorporate uncertainty quantification
- Deploy as web application for easy access by engineers
- Integrate with optimization algorithms for automated design

---

**Project Period:** 2021 - Present
**Organization:** Aarhus University - Mechanics and Geometry of Solids (MGS) Lab
**Supervisor:** PhD Souhayl Sadik
