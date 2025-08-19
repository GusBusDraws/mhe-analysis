# Image Analysis Dev
This project is for developing image analysis and segmentation routines for
research efforts related to the
[Multidisciplinary Simulation Center](https://micromorph.gitlab.io/)*,
with which Gus has been associated as a PhD student at Colorado School of Mines
and as a Research Associate at the University of Colorado Boulder.
Much of the associated data are 3D computed tomography scans,
consisting of 2D image slice making up a 3D volume. Most of these data
represent material systems are crystalline particulates in a polymeric binder
matrix. Often the goal of these analyses are to better improve the segmentation
of the particulate materials (which vary drastically in size) from the binder
and void space to create 3D surfaces that can be used to initialize physics
simulations.

\*The full name of the research center is:
The Predictive Science Academic Alliance Program (PSAAP)
Multi-disciplinary Simulation Center (MSC) for
Micromorphic Multiphysics Porous and Particulate Materials Simulations
Within Exascale Computing Workflows

## Change log
### merge-regions
2025-08-19: Add NB 51 for downsampling & segmenting the prill for testing
2025-08-12: Create concatenated CSV file with combined info about split segmentations
2025-08-12: Add NB 50 to continue with development that started in NB 40
2025-08-12: Rename old branch `dev-region-merging` and merge changes from `main`

### ct-verif
2025-08-12: Update resolution calculations and full grain particle estimations
2025-08-11: Add NB 49 to develop workflow for CT verification paper

### Previous branches
2024-08-05: Add NB 46 for developing a radial_filter function
2024-05-08: Add NB 44 for creating frames of a slice-through animation of a sample.
2024-05-08: Add Change Log to README

