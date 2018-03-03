# NAMD_Trajectory-Analysis

  For generating the psf file we needed some topology files which we imported (top_all27_protein_lipid_na.inp). We load the instruction file and split the chains and create the chains. Then the psf file is ready. It will create a new pdf and psf file. The new pdb file (5eu1_autopsf.pdb) is bigger than the size of the original pdb file (5eu1.pdb) because the new one is having H in it.

  Then we used the solvation module to solvate the molecule so it will feel the water molecules as a box. We fix the boundary and padding for the waterbox as well. Then we used the solvated molecule for simulation and further NAMD simulations. So we got new pdb and psf files (solvate.pdb and solvate.psf). Now we wrote an NAMD script to do the minimization. The topologies we use for creating psf file and the parameters file we use for running the NAMD simulation. So kept the parameter file (par_all36_lipid_prot_carb) in the same working directory. This parameter file is nothing but the combination of the carbohydrate files and lipid files and protein files. So we made that file, otherwise we can use default parameter files available.

Next we wrote the NAMD configuration file (minimize.namd) and for calculating the box size we wrote another script file(findbox.tcl). We need to find out the box size and put in the configuration script.
