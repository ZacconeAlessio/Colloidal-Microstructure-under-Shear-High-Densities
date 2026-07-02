# High-Density Colloids under Shear: Integral-Equation Theory

Python, Jupyter and Mathematica implementation accompanying

**L. Banetta, F. Leone, C. Anzivino, M. S. Murillo and A. Zaccone**

*Microscopic theory for the pair correlation function of liquidlike colloidal suspensions under shear flow*

Physical Review E **106**, 044610 (2022)

---

## Overview

This repository contains the notebooks and input data used to extend the intermediate-asymptotics theory of sheared colloidal suspensions to finite particle concentrations using liquid-state integral equation theory.

The workflow combines:

- analytical intermediate-asymptotics solutions of the pair Smoluchowski equation with shear flow,
- construction of an effective potential of mean force,
- Ornstein–Zernike integral equation,
- Percus–Yevick (PY),
- Hypernetted Chain (HNC),
- Modified Hypernetted Chain (MHNC)

to compute

- pair correlation functions \(g(r)\),
- static structure factors \(S(k)\)

of colloidal suspensions under shear flow.

---

## Computational workflow

![Computational workflow](results/figures/workflow.png)

---

## Representative result

Structure factor of sheared hard-sphere colloidal suspensions predicted by the integral-equation theory. Increasing Péclet number enhances long-wavelength density fluctuations and modifies the main structural peak.

![Representative result](results/figures/overview.png)

---

## Computational workflow

```
Intermediate-asymptotics solution (two-body)
            │
            ▼
Angular averaging
            │
            ▼
Interpolation onto uniform grid
            │
            ▼
Effective potential
            │
            ▼
Ornstein–Zernike equation
            │
            ▼
PY / HNC / MHNC closures
            │
            ▼
g(r) and S(k)
```

---

## Repository structure

```
notebooks/
```

Jupyter and Mathematica notebooks implementing the theoretical workflow.

```
data/
```

Input data generated from the intermediate-asymptotics calculations.

```
papers/
```

Associated publication.

---

## Companion repository

The intermediate-asymptotics MATLAB implementation is available in the companion repository

**Colloidal-Microstructure-under-Shear**

which generates the dilute-regime pair correlation functions used here as input.

---

## Note

Some notebooks are archival research notebooks and may reference intermediate files not included in the current repository; see `notebooks/README.md` for details.

---

## Reproducibility

This repository contains the notebooks, analytical derivations, and representative input datasets used in the calculations reported in

> Banetta, Leone, Anzivino, Murillo & Zaccone,
> *Microscopic theory for the pair correlation function of liquidlike colloidal suspensions under shear flow*,
> **Physical Review E** 106, 044610 (2022).

Most of the computational workflow can be reproduced directly from the material provided here. However, a small number of intermediate data files generated during the original research workflow were not preserved in the archived project. Consequently, some notebooks may require regeneration of intermediate inputs before they can be executed completely from start to finish.

The repository is therefore intended both as a companion to the published article and as a reference implementation of the integral-equation methodology.

---

# Citation

**If you use this code in academic work, please cite**

L. Banetta, F. Leone, C. Anzivino, M. S. Murillo and A. Zaccone,

*Microscopic theory for the pair correlation function of liquidlike colloidal suspensions under shear flow*,

Physical Review E **106**, 044610 (2022).
