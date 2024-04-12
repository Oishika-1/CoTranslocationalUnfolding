Commands used:

gmx_mpi grompp -f em_water.mdp -c addions-manual.gro -r addions-manual.gro -p master-manual.top -o em_water.tpr -po grompp_em_water.mdp
gmx_mpi grompp -f em_protein.mdp -c em_water.gro -r em_water.gro -p master-manual.top -o em_protein.tpr -po grompp_em_protein.mdp
gmx_mpi grompp -f nvt-anneal.mdp -c em_protein.gro -r em_protein.gro -p master-manual.top -o nvt-anneal.tpr -po grompp_nvt-anneal.mdp
gmx_mpi grompp -f nvt.mdp -c nvt-anneal.gro -r nvt-anneal.gro -p master-manual.top -o nvt.tpr -po grompp_nvt.mdp
