# MHE Analysis
This project is for the analysis of CT data obtained by Yeager et al. at Los Alamos National Lab (LANL). This CT data consists of 2D image slices showing IDOX crystals within a binder material. The goal of this analysis is to develop a procedure for segmenting the IDOX crystals from each other and from the binder material.

Questions should be directed to C. Gus Becker (GitHub/GitLab: @cgusb).

## Procedure description
Segmentation procedure operates on the 2D slices. Current approach will be to adapt the procedure published by [Wälhby et al. 2004](https://onlinelibrary.wiley.com/doi/full/10.1111/j.0022-2720.2004.01338.x)* as follows:

- (A) Smooth image.
- (B) Calculate gradient magnitude of A.
- (C) Calculate foreground seeds found by extended h-maxima transformation.
- (D) Calculate background seeds found by extended h-maxima transformation of the gradient magnitude image followed by removal of small components.
- (E) Calculate seeded watershed segmentation.
- (F) Merge seeded objects based on edge strength. Poorly focused objects are also removed in this step.
- (G) Calculate distance transform of the objects in the segmented image. The brighter the intensity the further the pixel is from the background or a neighboring object.
- (H) Calculate watershed segmentation of the distance transform before merging.
- (I) Combine segmentation results based on intensity, edge and shape information.

<div class="csl-entry">* Wälhby, C., Sintorn, I. M., Erlandsson, F., Borgefors, G., &#38; Bengtsson, E. (2004). Combining intensity, edge and shape information for 2D and 3D segmentation of cell nuclei in tissue sections. <i>Journal of Microscopy</i>, <i>215</i>(1), 67–76. https://doi.org/10.1111/J.0022-2720.2004.01338.X</div>

## Change log
### merge-regions
2025-08-12: Add NB 50 to continue with development that started in NB 40
2025-08-12: Rename old branch `dev-region-merging` and merge changes from `main`

### ct-verif
2025-08-12: Update resolution calculations and full grain particle estimations
2025-08-11: Add NB 49 to develop workflow for CT verification paper

### Previous branches
2024-08-05: Add NB 46 for developing a radial_filter function
2024-05-08: Add NB 44 for creating frames of a slice-through animation of a sample.
2024-05-08: Add Change Log to README

