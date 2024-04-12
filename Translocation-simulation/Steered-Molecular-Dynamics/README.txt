Commands used:

gmx_mpi grompp -f smd-pull-0.2Aperns-wofreeze-mofPOSRES.mdp -c nvt-woPOSRES-298K-nojump.gro-triclinic.gro -r nvt-woPOSRES-298K-nojump.gro-triclinic.gro -p master-manual.top
-o pull-posresMOF.tpr -po grompp-pull-posresMOF.mdp -n index.ndx -maxwarn 1
