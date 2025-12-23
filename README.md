# BNOT Figure Generation (BNOT_v2.ipynb)

This repository contains the simulation and plotting code used to generate the numerical figures for the **Bidirectional Nonlinear Optical Tomography (BNOT)** paper. All computations are performed in a single Jupyter notebook:

- `BNOT_v2.ipynb`

The notebook implements Monte Carlo simulations of squeezing and SHG measurements, estimates input/output coupling efficiencies \(\eta_1, \eta_2\), and produces high-resolution figure panels.

---

## Contents

- **BNOT_v2.ipynb**
  - Defines physical constants and device parameters for nonlinear photonic systems.
  - Implements core simulation functions:
    - `simulate_Sqz(...)` – squeezing vs. pump power and couplings.
    - `simulate_SHGeff(...)` – SHG conversion efficiency.
    - `cost_fixed_alpha(...)` – cost function for \(\eta_1,\eta_2\) estimation.
    - `G(...)`, `sinc(...)` – auxiliary nonlinear-optics model functions.
  - Performs Monte Carlo sampling including realistic noise models.
  - Sweeps true coupling efficiencies \((\eta_1,\eta_2)\) and recovers estimator performance.
  - Saves all figures and cached `.npy` arrays.

Generated files include:
- Figures: `Fig2a.png`, `Fig2b.png`, `Fig2c.png`, `Fig3a.png`, `Fig3b.png`, `Fig3c.png`, `Fig4a.png`, `Fig4b.png`, `Fig4c.png`, `Fig4d.png`
- Cached arrays: `est_eta1.npy`, `est_eta2.npy`, `eta1_err.npy`, `eta2_err.npy`

---

## Requirements

The notebook uses standard scientific Python packages:

- Python 3.8+
- NumPy
- SciPy
- Matplotlib
- Jupyter / Google Colab

Install with:

```bash
pip install numpy scipy matplotlib jupyter


## Citation

If you use this code, please cite the BNOT paper (arXiv:2510.13110).
