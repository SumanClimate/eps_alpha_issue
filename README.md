## Solution of transperancy issue while saving figures in .eps format ##
It is noticed that while using transpeancy ("alpha" in matplotlib) in figures and finally saving .eps format, the figure disregard the transperancy and save the figure in whole color where "alpha" is used. This notebook illustrates this issue and provide soultion for that.
## Solution ##
Three cases are discussed here.
## Case I ##
Here, "alpha" is used in a line plot with "fill_between". Although two figures look same in the notbook page, but after saving the first will show the transperancy shade but the 2nd figure will show whole color (blue here). The main tricks is to use "set_zorder" and "set_rasterization_zorder" cleverly.
## Case II ##
This case is a typical case in meteorology, where we are plotting some other plot keeping enso shade in the background. The Multivariate ENSO Index Version 2 (MEI.v2) is given in the repo (https://psl.noaa.gov/enso/mei/data/meiv2.data). Most importantly, here you need to use "set_zorder" and "set_rasterization_zorder" at the color legend axis also.
## Case III ##
This is a general case.
