## Solution of transperancy issue while saving figures in .eps format ##
It is noticed that while using transpeancy ("alpha" in matplotlib) in figures and finally saving .eps format, the figure disregard the transperancy and save the figure in whole color where "alpha" is used. This notebook illustrates this issue and provide soultion for that.
## Solution ##
Three cases are discussed here.
## Case I ##
Here, "alpha" is used in a line plot with "fill_between". Although two figures look same in the notbook page, but after saving, the first figure will show the transperancy shade but the 2nd figure will show whole color (blue here). The main tricks is to apply "set_zorder" and "set_rasterization_zorder" cleverly.
## Case II ##
This case is a typical case used in meteorology, where we are drawing some different plots keeping enso shade in the background. The Multivariate ENSO Index Version 2 (MEI.v2) data is used here and is given in the repo (https://psl.noaa.gov/enso/mei/data/meiv2.data). Most importantly, here you need to use "set_zorder" and "set_rasterization_zorder" at the enso color bar axis also.
## Case III ##
This is a general case.
