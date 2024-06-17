This repository contains the results of decomposition of 159 distant galaxies with spiral arms.

Fit_results:
The following data is presented for each galaxy in each band in which decomposition was performed:
- Image, mask, error map (sigma.fits), PSF;
- The parametric description of a model from IMFIT (fit.imfit); modified IMFIT version from https://github.com/IVChugunov/IMFIT_spirals is required.
- .fits image of a model (model.fits).

Tables:
A set of .csv files with measured parameters of a galaxy and its spiral arms.
- basic_parameters.csv: the general parameters of galaxies, either measured or taken from literature, in particular:
- - t_L: lookback time corresponding to z;
- - λ_rf: rest-frame wavelength for a given filter and z;
- - M_rf: absolute magnitude for rest-frame wavelength;
- - M_F814W: absolute magnitude in F814W filter in rest-frame.
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
- all_parameters.csv: previous three tables combined in one;
- individual_spiral_parameters.csv: parameters of individual spiral arms in a galaxy, the set of parameters is mostly similar to spirals_parameters.csv

Images:
A set of mosaics, each one showing multiple cropped images of all galaxies, the corresponding models with spiral arms and residual images.