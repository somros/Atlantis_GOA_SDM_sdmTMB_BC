# Spatial distributions for Canada with `sdmTMB`

This code produces distribution maps of GOA species from DFO synoptic bottom trawl surveys and the `sdmTMB` [package](https://github.com/pbs-assess/sdmTMB) (Anderson et al. 2022), to inform Atlantis GOA initial conditions and seasonal distributions (i.e., S1-S4 parameters). 

This is the code that deals with British Columbia.

This code performs 3 tasks:

1. Starting from DFO bottom trawl data and length-weight relationships, it calculates the CPUE of juveniles and adults at each haul location. This is done in `catch_to_CPUE_DFO/catch_to_cpue_DFO.Rmd`.
2. Loads CPUE data into a knitter file, which subsets to the species of interest. This is done in `DFO_sdmTMB_knitter.R`.
3. Runs the `sdmTMB` routine: fits the model, produces figures, output tables and validation metrics by species and stage. This is done in `DFO_sdmTMB_template.Rmd`.

Utility scripts include `DFO_species.R`, which maps species names from the DFO data to the Atlantis GOA functional groups. See scripts for details on data sources and methods.

__References__

Anderson, S.C., E.J. Ward, P.A. English, L.A.K. Barnett. 2022. sdmTMB: an R package for fast, flexible, and user-friendly generalized linear mixed effects models with spatial and spatiotemporal random fields. bioRxiv 2022.03.24.485545; doi: https://doi.org/10.1101/2022.03.24.485545