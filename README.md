# 🌬️ Dynamics of Static Stall
### Numerical Study of Flow Transition over a 2D Flat Plate at Low Reynolds Numbers

![Mechanical Engineering](https://img.shields.io/badge/Domain-Mechanical%20Engineering-blue)
![CFD](https://img.shields.io/badge/Tool-ANSYS%20Fluent-orange)
![MATLAB](https://img.shields.io/badge/Analysis-MATLAB-red)
![Institution](https://img.shields.io/badge/Institution-NIE%20Mysuru-green)

---

## 📌 About the Project

This project investigates the transition of flow from **laminar (static) to chaotic** behaviour over a two-dimensional flat plate operating at a **low Reynolds number regime**. The study was conducted numerically using ANSYS Fluent with varying **angles of attack (AOA)** ranging from **0° to 32.5°** at an air velocity of **0.148 m/s**.

The results help understand the **stalling phenomenon** — how it occurs, when it begins, and the changes in flow behaviour associated with it, from coherent vortex structures to fully turbulent chaotic states.

---

## 👨‍🎓 Project Team

| Name | USN |
|------|-----|
| D Ashrith | 4NI18ME404 |
| Shashank S S | 4NI18ME424 |
| Sumanth C T | 4NI18ME428 |
| Venkatesha T E | 4NI18ME431 |

**Guide:** Mr. P Srinag, Assistant Professor
**Institution:** Department of Mechanical Engineering, The National Institute of Engineering, Mysuru – 570008
**Academic Year:** 2020–21

---

## 🎯 Objectives

- Simulate 2D flow over a flat plate at low Reynolds number using Direct Numerical Simulation (DNS)
- Study the **stall phenomenon** and identify the critical angle of attack
- Identify flow transition from **periodic → quasi-periodic → chaotic** regimes
- Quantify **vortex energy** at leading edge (LEV) and trailing edge (TEV)
- Apply **dynamical systems theory** to characterise aerodynamic flow behaviour

---

## ⚙️ Simulation Setup

| Parameter | Value |
|-----------|-------|
| Flow Type | 2D Incompressible Viscous |
| Solver | ANSYS Fluent (DNS) |
| Air Velocity (V∞) | 0.148 m/s |
| Flat Plate Dimensions | 10 × 0.2 cm |
| Domain Size | 12C × 8C |
| Angles of Attack | 0° to 32.5° |
| Time Step (Δt) | 0.003 s |
| Total Time Steps | 100,000 |
| Mesh Nodes | ~2.02 Lakhs |
| Min. Kolmogorov Length Scale | 0.56 mm |

---

## 📊 Key Results

### Flow Regimes Identified

| Angle of Attack | Flow Behaviour |
|-----------------|----------------|
| 0° – 9° | Steady laminar — attached flow, no shedding |
| 10° – 20.5° | Periodic Kármán vortex shedding |
| 20.5° – 22° | Quasi-periodic — transition begins |
| 23° – 25° | Chaotic — stall condition reached |
| 26° – 32.5° | Post-stall re-stabilisation |

- **Stall angle** observed between **24° and 25°**
- Sudden jump in CL from AoA 22° → 23°, followed by a sharp drop at 24° → 25°

---

## 🔬 Analysis Techniques

### 1. Recurrence Quantification Analysis (RQA)
Used to identify periodic, quasi-periodic, and chaotic regimes from lift coefficient time series data.

| AoA | Embedding Dim | Delay | Recurrence Rate (%) | Determinism (%) |
|-----|--------------|-------|----------------------|-----------------|
| 15° | 3 | 86 | 10.22 | 99.40 |
| 22° | 3 | 90 | 6.62 | 97.86 |
| 25° | 3 | 210 | 5.40 | 93.58 |

> Decreasing determinism confirms transition to chaos as AoA increases.

### 2. Fast Fourier Transform (FFT)
Converts time-series lift signal into frequency and energy domain to identify dominant shedding frequencies.

### 3. Continuous Wavelet Transform (CWT)
Provides time-frequency localisation with energy density — addresses the temporal limitation of FFT.

### 4. Empirical Mode Decomposition (EMD) + Hilbert-Huang Transform (HHT)
Decomposes non-linear, non-stationary signals into Intrinsic Mode Functions (IMFs) for instantaneous frequency and energy analysis.

---

## 🗂️ Repository Structure

```
Dynamics-of-Static-Stall/
│
├── README.md
│
├── Report/
│   └── Final_Report.pdf
│
├── Simulation/
│   ├── Geometry/          # ANSYS Workbench geometry files
│   ├── Mesh/              # Overset and background mesh files
│   └── Fluent_Setup/      # Boundary conditions and solver settings
│
├── MATLAB/
│   ├── RQA.m              # Recurrence Quantification Analysis
│   ├── FFT_Analysis.m     # Fast Fourier Transform
│   ├── CWT_Analysis.m     # Continuous Wavelet Transform
│   └── EMD_HHT.m         # Empirical Mode Decomposition & HHT
│
├── Results/
│   ├── Vortex_Patterns/   # Q-criterion vortex visualisations
│   ├── CL_CD_Plots/       # Lift and drag time histories
│   ├── RQA_Plots/         # Recurrence and attractor diagrams
│   └── Time_Series/       # FFT, CWT, EMD, HHT plots
│
└── References/
    └── reference_list.md
```

---

## 🛠️ Tools & Software

- **ANSYS Workbench** — Geometry and mesh generation
- **ANSYS Fluent** — CFD simulation (DNS model)
- **MATLAB** — RQA, FFT, CWT, EMD, and HHT analysis
- **Q-criterion** — Vortex identification and animation

---

## 📚 References

Key references used in this study:

- J D Anderson (2003) — *Fundamentals of Aerodynamics*
- Yan Liu et al. (2012) — *Numerical bifurcation analysis of static stall*
- D Durante et al. (2020) — *Bifurcations and chaos transition at low Reynolds number*
- Norden E. Huang et al. (1998) — *EMD and Hilbert spectrum for nonlinear time series*
- J. P. Eckmann et al. (1987) — *Recurrence Plots of Dynamical Systems*

---

## 🏷️ Topics

`cfd` `aerodynamics` `flat-plate` `ansys-fluent` `matlab` `low-reynolds-number` `static-stall` `vortex-dynamics` `recurrence-quantification-analysis` `empirical-mode-decomposition` `wavelet-transform` `dns` `mechanical-engineering`

---

## 📄 License

This project was submitted in partial fulfillment of the **Bachelor of Engineering in Mechanical Engineering** at The National Institute of Engineering, Mysuru (2020–21). All rights reserved by the authors.
