[README_BNOT.txt](https://github.com/user-attachments/files/24319359/README_BNOT.txt)
BNOT Figure Generation (BNOT_v2.ipynb)

This repository contains the simulation and plotting code used to
generate the numerical figures for the Bidirectional Nonlinear Optical
Tomography (BNOT) paper. All computations are performed in a single
Jupyter notebook:

-   BNOT_v2.ipynb

The notebook implements Monte Carlo simulations of squeezing and SHG
measurements, estimates input/output coupling efficiencies (η1, η2), and
produces high-resolution figure panels.

Contents

-   BNOT_v2.ipynb
    -   Defines physical constants and device parameters for nonlinear
        photonic systems.
    -   Implements core simulation functions:
        -   simulate_Sqz(…) – squeezing vs. pump power and couplings
        -   simulate_SHGeff(…) – SHG conversion efficiency
        -   cost_fixed_alpha(…) – cost function for efficiency
            estimation
        -   G(…), sinc(…) – auxiliary model functions
    -   Performs Monte Carlo sampling including realistic noise models
    -   Sweeps true coupling efficiencies and recovers estimator
        performance
    -   Saves figure files and cached .npy arrays

Generated files include:
Fig2a.png, Fig2b.png, Fig2c.png, Fig3a.png, Fig3b.png, Fig3c.png,
Fig4a.png, Fig4b.png, Fig4c.png, Fig4d.png
est_eta1.npy, est_eta2.npy, eta1_err.npy, eta2_err.npy

Requirements

Python 3.8+
NumPy
SciPy
Matplotlib
Jupyter / Google Colab

Install with:
pip install numpy scipy matplotlib jupyter

Running the Notebook

Google Colab

1.  Open BNOT_v2.ipynb in Colab
2.  Run the Drive-mount cell
3.  Run all cells
4.  Figures saved to Drive/Papers/BNOT/

Local Jupyter

1.  Clone repository
2.  Replace first cell with a local save_dir
3.  Remove Colab mounting code
4.  Run notebook to generate figures

Figure Mapping

Fig. 2 — squeezing/SHG distributions
Fig. 3 — estimator performance maps
Fig. 4 — RMS error and robustness surfaces

Customizing Parameters

Modify device parameters (d_eff, L, S_omega, S_2omega, lambda_omega,
n_omega, n_2omega, losses, Delta_k, noise levels) and simulation counts
(n_trials, numb, num_repeats) as needed.

Reproducibility

The notebook uses:
np.random.seed(97)

Cached arrays can be deleted for fresh runs.

Citation

Please cite the BNOT paper when published.

Contact

Open an Issue or contact the corresponding author.
