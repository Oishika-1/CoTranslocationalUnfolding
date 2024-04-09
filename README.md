# CoTranslocationalUnfolding
# This is under a project called Co-translocational unfolding of HP35 in MIL-101(Cr).
# It contains input files to simulate translocation of a protein across pores of metal-organic frameworks (MOFs) using Molecular Dynamics (MD) simulations.
# HP35 and MIL-101(Cr) have been used as the protein and the MOF for current project.

# Required input files for each step of simulations have been kept in seperate folders.
# Description of the folders:
  1. Topology folder: contains Forcefield files.
  2. CanonicalSampling folder: contains input files corresponding to the canonical sampling run.
  3. Translocation-simulation folder: contains input files for carrying out translocation simulation.
# Folders contain nested subfolders. When required, we have provided a README.txt file in some of the subfolders.
# Contents of each folder or subfolder:
  1. Run input file (.mdp).
  2. Initial coordinates of the complete system (.gro).
  3. Gromacs run binary file containing all input information (.tpr).
