## MOLECULAR MODELING OF MATERIALS A.Y. 2023-2024
##### Project by Giuseppe Gentile (HPC)
Lennard Jones cluster optimization via Genetic Algorithm and Simulated Annealing.

# Lennard Jones cluster optimization

## Introduction
In computational chemistry, optimizing the arrangement of atomic clusters is crucial for understanding the properties of materials at the molecular level.

Initially inspired by the Au-Pt system proposed in the paper [1], it was soon realized that the Lennard-Jones potential, which is effective for modeling noble gas interactions, was inadequate for accurately modeling metallic interactions. 
Therefore, this project focuses on optimizing Lennard-Jones clusters of Argon (Ar) and Krypton (Kr) instead.

Lennard-Jones potentials are commonly used to model the interaction between a pair of neutral atoms, capturing the balance between attractive and repulsive forces. The optimization of such clusters aims to find the most stable configuration, which corresponds to the global minimum of the potential energy surface.

To accurately model the interatomic distances and interactions, a voxel grid[2] was used. In this context, a voxel grid divides the three-dimensional space into discrete units, known as voxels, with each voxel representing a specific volume element in space measured in angstroms (Å). This method is particularly effective for visualizing and calculating spatial distributions of atoms within a cluster, allowing precise control over atomic positions and distances.

Genetic Algorithm (GA)[3] (invented by John H. Holland in the 1960s) is an heuristic search technique inspired by the principles of natural selection and genetics. 

It iteratively evolves a population of potential cluster configurations through selection, crossover, and mutation processes. By evaluating the fitness of each configuration (that is the the Lennard-Jones potential in this case), the GA progressively leads to the optimal atomic arrangement by performing be above metioned operations.

GA-s tends to be quite good at finding generally good global solutions due to their broad exploration of the surface, but somehow inefficient at finding the last few mutations to find the absolute optimum. 
For this reson, the new proposed approach (GASA) combines the global search capabilities of GA with the local search efficiency of SA.

In addition, all results are cross-validated and compared with calculations from the Tinker's software. 

<br>

Notebook with code, discussion of results and comments is available [here](https://github.com/giuseppeegentile/LJ-cluster-minimization/blob/main/LJ%20cluster%20opt%20GASA.ipynb).

### References
[1] Genetic algorithms for computational materials discovery accelerated by machine learning, P. C. Jennings et al. \
[2] Curless, B., & Levoy, M. (1996). A Volumetric Method for Building Complex Models from Range Images.\
[3] Holland, J. H. (1992). Adaptation in Natural and Artificial Systems: An Introductory Analysis with Applications to Biology, Control, and Artificial \Intelligence. MIT Press. 
