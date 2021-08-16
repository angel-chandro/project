# README

Dhalos_ROCKSTARhaloes directory: contains files related to running ROCKSTAR haloes on DHaloes (or at least try it). The different files are:

* DHalos/ROCKSTAR.test.param: parameter file for ROCKSTAR haloes that has been created.
* DHalos/Build_Trees/ROCKSTAR_reader.f90: file created to read ROCKSTAR haloes so that DHalos makes the halo trees. Still not finished, need to check the halo ID format necessary to proccess ROCKSTAR haloes (search information on DHalos papers connected with IDCorr variable). In principle, IDCorr must keep as in "nifty_reader.f90" file (maybe information here [Link](http://gavo.mpa-garching.mpg.de/Millennium/pages/help/HelpSingleHTML.jsp#identifiers))
* DHalos/Build_Trees/tree_files.f90, DHalos/Build_Trees/subhalo_data.f90, DHalos/Build_Trees/merger_trees.f90, DHalos/Build_Trees/CMakeLists.txt: files that have been modified.

* ROCKSTAR_parent_test.py: python file used to run find_parents tool over different ROCKSTAR halo list outputs (this find_parents tool adds a column with "pid": parent ID). Because the current strategy is to create the halo trees based on ROCKSTAR halo catalogues and to do that, it is necessary to know if the halo is a host halo ("pid" = -1) or is a subhalo that belongs to a host halo ("pid" = host halo ID).
The other strategy that has been left aside so far is to run DHalos over ConsistentTrees halo catalogues, what is a possibility since "pid" (different from the one above) and "upid" properties only differs in a 1% of the halos (here we have a 3 level hierarchy, not 2 level). The property to distinguish host haloes and subhaloes would be "upid" in this case.

Useful information about the project can be found in different links below:
* DHalos info: [Link](https://arxiv.org/pdf/1311.6649.pdf)
* ROCKSTAR info: [Link](https://arxiv.org/pdf/1110.4370.pdf), [Link](https://arxiv.org/pdf/1110.4372.pdf)
* UNIT info: [Link](https://arxiv.org/pdf/1811.02111.pdf)
* SHARK info: [Link](https://arxiv.org/pdf/1807.11180.pdf)
* SAMs info: [Link](https://arxiv.org/pdf/1412.2712.pdf), [Link](https://arxiv.org/pdf/astro-ph/0610031.pdf)
* ROCKSTAR concentration info: [Link](https://arxiv.org/pdf/2007.09012.pdf) (4.3 section)
* Calibration model info: [Link](https://arxiv.org/pdf/2103.01072.pdf)
* Approximations made on baryonic matter info: [Link](https://arxiv.org/pdf/1804.03097.pdf)
* Differences ROCKSTAR-VELOCIraptor in DHalos info: [Link](https://arxiv.org/pdf/2106.12664.pdf)