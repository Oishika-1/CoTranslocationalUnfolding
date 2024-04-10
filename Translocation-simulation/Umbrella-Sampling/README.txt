Required input files for umbrella sampling.

Commands used for running umbrella sampling simulations.

gmx_mpi grompp -f us-modified.mdp -c input.gro -r input.gro -p master-manual.top -o us.tpr -po grompp-us.mdp -n index.ndx -maxwarn 1
gmx_mpi mdrun -deffnm us -v

For run input file (.tpr), only the first .tpr file is given. Extension for particular windows has been carried out by running the following commands.

gmx_mpi convert-tpr -s old.tpr -o new.tpr -extend ...
gmx_mpi mdrun -deffnm new -cpi old.cpt

Contents of each folder (corresponding to each umbrella window).

1. Initial coordinates of the complete system (.gro)
2. Gromacs run binary file containing all input information (.tpr)

Run input file (.mdp) is common for all umbrella windows. Hence, has been kept in the parent folder.
