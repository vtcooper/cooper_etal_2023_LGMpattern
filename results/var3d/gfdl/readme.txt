Due to filesize limitations on backup, gfdl results are stored in 3 separate 
files for each experiment. T and Q (3-D variables) are stored individually,
and the remaining variables (which are 2-D) needed for kernel analysis are
in the "2Dvars" files. 

This nuance is only for GFDL output because of higher model resolution.

Note that some GFDL variables have been renamed to match their counterparts
using CESM naming conventions. This renaming enables the GFDL output to 
be compatible with CAM5 kernels.
