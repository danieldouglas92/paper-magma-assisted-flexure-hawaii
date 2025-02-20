This repository is assosciated with the publication

*Magma-Assisted Flexure of Hawaiian Lithosphere Inferred From Three-Dimensional Models of Lithospheric Flexure Constrained by Active Souce Seismic Data*

by

Douglas, D.,
Ito, G.,
Boston, B.,
Dunn, R.,
Naliboff, J.,
Wessel, P.,
Watts, A. B.,
Shillington, D.,
Cilli, P.,

which is currently in review.

# Software
Our numerical simulations were run using the open source geodynamics software ASPECT ([https://aspect.geodynamics.org/](https://aspect.geodynamics.org/)). Specifically, we utilize a branch of the developmental versions of ASPECT (2.6.0-pre) with a copy of the the source code included in this repository and on Zenodo [![DOI](https://zenodo.org/badge/835081143.svg)](https://doi.org/10.5281/zenodo.14897977).

# Overview
The source code and all input files required to reproduce the results from Douglas et al., (2024), "Magma-Assisted Flexure of Hawaiian Lithosphere Inferred From Three-Dimensional Models of Lithospheric Flexure Constrained by Active Souce Seismic Data" submitted to *JGR: Solid Earth* is contained within this repository. The contents of this repository is outlined below.

## ASPECT_parameter_files
Includes the input files needed to reproduce the ASPECT models. The .prm files are formatted in such a way that once ASPECT has been built, they can be run consistently within the repository as long as the model is run from the directory where the .prm file is located.

## ASPECT_source
Contains the source code for the version of ASPECT used to run the models. A guide to compiling ASPECT can be found in the ASPECT manual at ([https://aspect-documentation.readthedocs.io/en/latest/user/install/index.html](https://aspect-documentation.readthedocs.io/en/latest/user/install/index.html)).

## data_files
Contains ASCII data files which are read by ASPECT during model runs to prescribe the topographic load of the growing Hawaiian Islands (aspect_traction_files), the initial thermal state of the model, and to heat the lithosphere locally beneath the Hawaiian Islands (aspect_heating_files). Within aspect_heating_files, there are 3 directories which prescribe heating equivalent to a 30 Myr reduction in seafloor age, a 50 Myr reduction in seafloor age, or a 70 Myr reduction in seafloor age.

## seismic_and_coral_data
Contains observations used to constrain the numerical models. `Adjusted_east.txt`,  `Adjusted_mid.txt`, and `Adjusted_west.txt` contain the depth to the top of the oceanic crust from reprocessed seismic reflections from Cilli et al., (2023). `cartesian_corrected_hawaii_moho.txt` contain the imaged Moho obtained from tomographic inversions along Line 1 from MacGregor et al., (2023). `cartesian_corrected_kaena_moho.txt` contain the imaged Moho obtained from tomographic inversions along Line 2 from Dunn et al., (2024). The files `correction_basement_MCSX.txt`, where X=1,2,3,4,5,6,7,8, represent the top of the oceanic crust from seismic reflections from Boston et al., (in review).

### island_growth.mp4
An animation showcasing how the Hawaiian Islands are grown in the ASPECT models.
