# MnF2 field-amplified exchange data

This repository contains the numerical data associated with “Field-amplified readouts of weak altermagnetic exchange in MnF2”.

## Contents

- `data/01_dft_energy_mapping/` contains the crystal structures, collinear magnetic configurations, and recorded total energies used for the 20-Mn and 28-Mn mappings.
- `data/02_exchange_parameters/` contains the stored bootstrap distributions, production exchange parameters, effective-Hubbard scan, and mapping diagnostics. `exchange_20Mn_J7_Ueff4p8.csv` contains only the stored seventh-neighbor quantities `J7a`, `J7b`, and `deltaJ7` for the 20-Mn mapping.
- `data/03_single_ion_anisotropy/` contains the site tensors, the Mn2 tensor rotated into the Mn1 frame, the symmetrized tensor, and the scalar SIA summary.
- `data/04_fef2_transfer/` contains only the parameter and compensation-field data for the FeF2 transfer test reported in the Supplemental Material.

## DFT energy mapping

The 20-Mn dataset contains 240 configurations. All 240 reached the electronic convergence requirement and were used in the parameter fitting.

The 28-Mn dataset contains 240 configurations. Of these, 235 reached the electronic convergence requirement and were used in the parameter fitting. Five non-converged configurations, with zero-based identifiers 95, 113, 158, 199, and 232, are retained for completeness but are explicitly marked `converged=false` and `used_in_fit=false`.

## Data conventions

- Positive exchange values correspond to antiferromagnetic coupling.
- `deltaJ7 = J7b - J7a`.
- DFT total energies are reported in eV per magnetic supercell.
- Exchange and SIA values are reported in microelectronvolts unless otherwise stated.
- Configuration identifiers are zero-based.

## Repository scope

This repository contains numerical data only. Simulation and analysis source code is not included.

The release does not include raw VASP output files, dipolar or Ewald convergence datasets, plotting data, or synthetic feasibility datasets.
