# VjetsPythia8
This is a GitHub repository created to store the VjetsPythia8 simulations, both the fiducial version and the updated simulation with matching &amp; merging implemented.

This document serves as a guide to the various files required to run the simulations, but it should not be regarded as exhaustive!  Please feel free to direct any questions to the author, Ben Johnson: bjohns18@tufts.edu.

After unpacking the VjetsPythia8 tarball, you should see the main code, VjetsPythia8.cc, in addition to a host of supporting files.  First, let's cover the command files.

The command files end in .cmnd, and they provide instructions for Pythia to run the physics simulations.  There are four primary command files and two support files.  The primary files are VjetsPythia8.cmnd, VjetsPythia8_kTDurham.cmnd, VjetsPythia8_PTLund.cmnd, and VjetsPythia8_Phase.cmnd.  These each represent different approaches to the W+jets simulation, with the former containing the fiducial version (no merging), while each of the last three implements a different CKKW-L merging scheme.  You will supply one of the primary .cmnd files as a command line input when running the script so that Pythia can perform the simulation as desired.

The two support command files are read in by the main program automatically, and they contain a variety of settings and parameters relevant to the simulation.  These include, but are not limited to, the number of events, the random seed, the tunes, and a variety of Standard Model values like particle masses.  It's essential to properly adjust the support command files when running the simulations, but you don't need to include them on the command line.

Next, we can cover the .sbatch files.  These are Slurm scripts which direct the cluster nodes to run the Pythia simulation.  There are four nearly identical versions, one for each of the command files.  They should be relatively straightforward, but, in a nutshell, they request time on a node, establish output files for information storage, ensure ROOT setup, then execute the script.  
