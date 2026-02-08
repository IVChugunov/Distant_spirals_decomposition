This repository contains the data related to the decomposition of 159 distant galaxies ($0.1 \leq z \leq 3.3$) with spiral arms. The first work published as [Chugunov et al., 2025a](https://ui.adsabs.harvard.edu/abs/2025PASA...42...29C/abstract) is dealing with spiral arms, and the next (Chugunov et al., in prep.) involves clumps.

The data is arranged in folders in a following way:

## Fit_results
Subfolders are organized for each galaxy and each filter which was used for analysis. Each one contains:
- Image, mask, error map (sigma.fits), PSF as .fits files;
- .fits image of a model with spiral arms (model_sp.fits).
- The parametric description of the said model (fit_sp.imfit) obtained with IMFIT; these models work only with the modified IMFIT version from https://github.com/IVChugunov/IMFIT_spirals, specifically version [Beta](https://github.com/IVChugunov/IMFIT_spirals/tree/Beta).
Files related to the work on clumps:
- Residual image (image minus model_sp) which was used for clumps detection (residual_sp.fits);
- Mask image used for clumps identification (mask_c.fits), as clumps could have been masked at previous step;
- .fits image of a model of clumps (model_c.fits). In order to get a complete photometric model of a galaxy, one should sum model_sp and model_c;
- The parametric description of the said model (fit_c.imfit) obtained with IMFIT.
If folder lacks them, it means that no clumps were found in a galaxy.

## Tables:
A set of .csv files with measured parameters of a galaxy, its spiral arms and clumps.
- basic_parameters.csv: the general parameters of galaxies, either measured or taken from literature, in particular:
- - t_L: lookback time corresponding to z;
- - λ_rf: rest-frame wavelength for a given filter and z;
- - M_rf: absolute magnitude for rest-frame wavelength;
- - M_F814W: absolute magnitude in F814W filter in rest-frame;
- - R_25: optical radius (of 25 mag isophote) in rest-frame.
- components_parameters.csv: components contribution to the total luminosity and the parameters of traditional components, in particular:
- - D/T, B/T, Bar/T, R/T, S/T: the contribution of disc, bulge, bar, ring and spiral structure to the total luminosity, respectively
- spirals_parameters.csv: parameters of the spiral structure, in particular:
- - μ: pitch angle;
- - Δμ: pitch angle increase from the beginning to the end of arms;
- - l_ψ: azimuthal length of arms;
- - w: spiral arms width;
- - r_end: spiral arms extent;
- - h_s: spiral arms exponential scale;
- - W_i: ratio between the end width and the beginning width;
- - S: skewness of the arm perpendicular profile;
- - A_sp: asymmetry of the spiral pattern.
- clumps_parameters.csv: parameters of the clump structure, in particular:
- - N_c: number of clumps in a galaxy;
- - C/T: clump-to-total ratio;
- - C/T_F814W: clump-to-total ratio normalised to the rest-frame wavelength of F814W filter
- - r_c/h: average galactocentric distance of clumps normalised to the disc exponential scale of a galaxy
- - f_cs(0.2): clumps concentration towards spirals
- all_parameters.csv: previous tables combined in one;

- individual_spiral_parameters.csv: parameters of individual spiral arms in a galaxy, the set of parameters is mostly similar to spirals_parameters.csv
- individual_clump_parameters.csv: parameters of individual clumps in a galaxy, the set of parameters is mostly similar to clumps_parameters.csv

## Images:
A set of mosaics, each one showing multiple cropped images of all galaxies, the corresponding models with spiral arms and residual images.