# pyaxe_ISSUES
Cases of some issues with pyaxe

## pyaxe_issue_flux_calib

  This case tests pyaxe version '0.1.dev29+gf57de55.d20200106' (with sextractor version 2.19.5 (2014-11-16)). The object is GD153 downloaded from MAST (before pipeline update in Dec 2019) with PID 14544. Only G141 and F160W flt files were downloaded. Totally, we have 12 flt files in G141 and F160W each, and they paired 1-1 to each other. A subset of this data set was analyzed and shown as an example for the pyaxe_template which can be accessed (here)[https://github.com/bkornpob/pyaxe_template/tree/master/Example02].
  
  The file 02_compare_with_standard.ipynb in this repo shows the issue. The notebook reads pyaxe spectrum outputs (i.e., SPC.fits or opt.SPC.fits files). GD153 is equivalent to the object ID = 74. From 12 files of G141, we calculate sigma-clipped median given common wavelength grids. Linear interpolation interpolates fluxes to the common grids. These fluxes from individual images + median fluxes are plotted. One sequence is from opt.SPC.fits, and the other from SPC.fits. STANDARD fluxes are from gd153_mod_010.fits downloaded from CALSPEC. The STANDARD fluxes are also interpolated to the common grids. The second figure shows the ratio between STANDARD and MEDIAN (of each sequence). The results show significant discrepancy between the STANDARD and the pyaxe outputs.
  
  
