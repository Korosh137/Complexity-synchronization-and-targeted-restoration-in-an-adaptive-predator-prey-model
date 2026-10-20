# Complexity Synchronization in an Adaptive Predator–Prey Model

**MATLAB code, saved results, and figure-reproduction scripts** accompanying the manuscript *“Complexity synchronization and targeted restoration in an adaptive predator–prey model.”*

## Overview

This repository provides the MATLAB scripts and supporting numerical results for investigating **complexity synchronization (CS)** in an adaptive predator–prey model. The study examines relationships among adaptive agent behavior, cooperation, and synchronization, including the effects of perturbations and targeted restoration.

The repository supports two ways of working with the results: running the original stochastic simulations and analyses, or regenerating figures directly from saved MATLAB data without repeating the computationally intensive simulations.

## Download the plotting-only package

The plotting-only MATLAB scripts and their saved `.mat` results are distributed separately as a ZIP archive on Google Drive because the complete package is too large for a convenient GitHub repository upload.

**[Download PlotOnly.zip from Google Drive](https://drive.google.com/file/d/1D96asBK4rSfGjMKaodmjvz_N3zSzhiAZ/view?usp=drivesdk)**

The archive is shared with **anyone who has the link (Viewer access)**. It contains the figure-specific `PLOT_ONLY_*.m` scripts, their corresponding `.mat` data files, `RUN_ALL_PLOTS.m`, and a `README.txt` with additional information.

The ZIP is approximately 496 MB (about 473 MiB). Download and extract it before running the plotting scripts.

## Repository structure

```text
.
├── Fig2_Animation.m
├── Fig3_trajectories.m
├── Fig4a_CCpayvsRS.m
├── Fig4b_CCpayTime.m
├── Fig5a_CStimeMDEAgraph.m
├── Fig5b_CStimeDFAgraph.m
├── Fig6_CvsCS_MDEA.m
├── Fig7_CvsCS_DFA.m
├── Fig8_CSperturbation_MDEA.m
├── Fig9_CSperturbation_DFA.m
├── Fig10_11andS1andS2.m
├── FigS3_CrossCorrelationRaw.m
├── FigS4_RenewalTest.m
├── FigS5_AutocorrelationTaus.m
└── PlotOnly/
    ├── README.txt
    ├── RUN_ALL_PLOTS.m
    ├── PLOT_ONLY_*.m
    └── *.mat
```

*File extensions are shown explicitly for clarity; Windows may hide them. The `PLOT_ONLY_*.m` and `*.mat` entries represent the corresponding individual figure files.*

## Reproducing the figures

### Option 1 — Plot from saved results (recommended)

1. Download or clone this repository.
2. Open MATLAB and navigate to the `PlotOnly` directory.
3. Run the `PLOT_ONLY_*.m` script corresponding to the figure you want to reproduce, or review `RUN_ALL_PLOTS.m` for batch plotting.
4. Ensure that the script's MAT-file path points to the matching `.mat` file in `PlotOnly`. Some scripts may require updating a local path.
5. Find the exported figure in the output directory specified by that script (typically a `Figures` subfolder).

These plotting-only scripts are intended to read saved numerical results rather than rerun the agent-based simulations or recompute MDEA/DFA analyses. See `PlotOnly/README.txt` for any additional instructions specific to these scripts.

### Option 2 — Run the original simulations

Run the original figure-specific MATLAB `.m` files in the repository root. These scripts generate or analyze model results and may take substantially longer to execute. Depending on the script, additional MATLAB toolboxes or helper functions may be required; consult the script headers and code before running.

## Reproducibility and stochastic variation

The predator–prey model contains stochastic processes. Independent simulation runs can therefore produce numerical differences, even when the qualitative behavior is comparable. The `.mat` files supplied in the linked Google Drive ZIP preserve saved results for direct figure reconstruction, avoiding the need to repeat lengthy simulations when the goal is simply to reproduce a plot.

**Important:** Each plotting-only script must be paired with its corresponding MAT file. A MAT file from a different analysis may contain different variables and cannot be used interchangeably.

## Citation

If you use these scripts or results, please cite the associated manuscript:

Mahmoodi, K., Kerick, S., Franaszczuk, P., Boothe, D., Grigolini, P., and West, B. *Complexity synchronization and targeted restoration in an adaptive predator–prey model.* Manuscript submitted to **PNAS Nexus**.

Please update the citation with the publication details and DOI if the paper is published.

## Questions and reuse

The code and data are shared to facilitate inspection, reproducibility, and further research on complexity synchronization in adaptive systems. Consult any license file in the repository for applicable reuse permissions; public availability alone does not establish a license.
