#
#Required input files for equilibration.

#Steps followed (Folder name)
1. Energy minimization-water (1.energy-minimization/1.water-minimization)
2. Energy minimization-protein (1.energy-minimization/2.protein-minimization)
3. Annealing for NVT (2.anneal+298K)
4. NVT without position restraining on non-hydrogen atoms of MOF (3.nvt-wo-mofpOSRES-298K)

Command used:
gmx_mpi grompp -f em_water_up.mdp -c addions-manual-protein-moved.gro -r addions-manual-protein-moved.gro -p master-manual.top -o em_water.tpr -po grompp_em_water.mdp -n index.ndx -maxwarn 1
gmx_mpi grompp -f em_protein_up.mdp -c em_water.gro -r em_water.gro -p master-manual.top -o em_protein.tpr -po grompp_em_protein.mdp -n index.ndx
gmx_mpi grompp -f nvt-anneal+298K_up.mdp -c em_protein.gro -r em_protein.gro -p master-manual.top -o nvt.tpr -po grompp_nvt-anneal.mdp -n index.ndx
gmx_mpi grompp -f nvt-wo-mofPOSRES_up.mdp -c nvt.gro -p master-manual.top -o nvt-woPOSRES-298K.tpr -po grompp_nvt-wo-mofPOSERS-298K.mdp -n index.ndx
