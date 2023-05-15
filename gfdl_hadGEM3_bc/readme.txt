Author: Vince Cooper (2023) vcooper@uw.edu

Note: all files/boundary conditions in this folder are the same as 
those in "cam_bc" folder, only the file conventions are different.

2x_*.nc represent 2xCO2(LongRunMIP) boundary condition and monthly mean.
holo_*.nc represent "baseline" LGMR (Osman et al. 2021) late holocene (0-4 kya).
lgm_*.nc represent LGMR (Osman et al. 2021) LGM (19-23 kya).

*_n05_*.nc files represent scaled patterns with global-mean SST
anomaly equal to -0.5 K.

"bc" files are mid-month values intended for use as boundary condition.
"monmean" are monthly means.
Note that "bc" files will have nonphysical values (e.g., SIC > 1) which
are designed to be interpolated and clipped by the AGCM.


