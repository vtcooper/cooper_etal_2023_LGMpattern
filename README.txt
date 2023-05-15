Author: Vince Cooper (May 2023) vcooper@uw.edu

SST/SIC boundary conditions (LGM values are adjusted to modern-day land mask) 
for atmosphere-only model simulations of LGM and 2xCO2(LongRunMIP). 
Postprocessed results are included for five AGCMs:
CAM4, CAM5, CAM6, GFDL-AM4, HadGEM3-GC3.1-LL.

Boundary condition files include monthly means and mid-month values (mid-month 
values are designed for input in AGCM).

Folders:
-cam_bc: boundary condition files designed for CAM ("...prediddle" variables 
are the monthly means)
-gfdl_hadGEM3_bc: boundary condition files designed to mimic AMIP boundary 
condition files (for input in models other than CAM, although further preprocessing
is likely required); note that 'dates' are all dummy values
-results: postprocessed AGCM output

Guide to filenames:
-Baseline: represents LGMR Late Holocene (mean of 0-4ka) from Osman et al. (2021)
-LGMR: LGM (mean of 19-23 ka) from Osman et al. (2021)
	--anomalies are added to Baseline (SST)
	--SIC is used directly
-2xCO2: LongRunMIP (Rugenstein et al. 2019) mean of 6 models;
	--anomalies are computed as:  (mean of final 200 years of
	  each 2xCO2 simulation) less (mean of final 200 years of
	  each control simulation) [for SST]
	--SST anomalies are added to Baseline
	--SIC is used directly as multi-model mean of final 200
	  years of each 2xCO2 simulation
	--Note: some are 1pct2x and others are abrupt2xCO2, but
	  each are run to near-equilibrium
	--Note: only MIROC included monthly SST (rather than 
	  annual), so the SST climatology for each model is
	  scaled to match MIROC's seasonal cycle. All models
	  include monthly SIC.
--...by0.5K: same datasets as above, but SST anomalies have been multiplied by
	a constant scale factor (determined separately for each boundary condition) 
	that reduces global annual mean SST anomaly to -0.5 K
	--sea ice is held constant at Baseline


Details below of model years used for composing the 2xCO2 boundary condition:
CESM 104
a2x: 2300-2500 
control: 800-1000

CNRM CM61
a2x: 550-750
Control: 1800-2000

HadCM3L
a2x: 500-700
control: 500-700
(Output issue occurs in year ~800 of control)
“HadCM3L has a jump of about 80W/m2 in surface heat fluxes 
constructed by atmospheric variables hfls, hfss, rls, 
rsds, rsus after 800 years of control.“ -longrunmip.org

MPI ESM 12
a2x: 800-1000
control: 1300-1500

MIROC 32
1pct2x: 1803-2003
control: 481-681

GFDL ESM2M:
1pct2x: 4300-4500
control: 1140-1340




