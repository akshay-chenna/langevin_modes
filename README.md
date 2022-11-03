## Reading the pdb file
### PDB file is read using the parsePDB() command from prody package and saved as structure for further analysis.

## Getting infromation for residues
### Once we have the structure, we see the hierarchial view and find out all the different chain and number of residues present in each chains. After getting these residue we can get different information using .get<tab> command.

## Hessian Matrix
### Hessian matrix is build with the help of anm model and using the hessian matrix, we get the mass weighted hessian matrix. Masses used for the calculation of mass weighted hessian matrix is calculated with the help of get_residue_mass(residue_name) fuction.

## Calcualtion of fluctions
### Once we have the mass weighted hessian matrix, we take this H_m as input for anm model and calulate fluctuations directly using calcFlucts(anm). Or the fluctuations are calculated by calculating the covariance matrix as inverse of H_m. 

## Pearson Correlation factor
### Once we have the fluctuations, we compare these with the fluctuations from GROMACS simulations with the help of pearson correlation factor. This pearson correlation factor is calculated for different values of cutoff distance to get optimal cutoff distance to be used in the anm model which is used to calculate the hessian matrix.
