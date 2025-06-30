# VjetsPythia8
Repo to store the VjetsPythia8 simulations, both the fiducial version and the updated simulation with matching &amp; merging implemented.

After unpacking the VjetsPythia8 tarball, you should see the main code, VjetsPythia8.cc, in addition to a host of supporting files.  First, let's cover the command files.

The command files end in .cmnd, and they provide instructions for Pythia to run the physics simulations.  There are four primary command files and two support files.  The primary files are VjetsPythia8.cmnd, VjetsPythia8_kTDurham.cmnd, VjetsPythia8_PTLund.cmnd, and VjetsPythia8_Phase.cmnd.  These each represente different approaches to the W+jets simulation, with the former containing the fiducial version (no merging), while each of the last three implements a different CKKW-L merging scheme.  You will supply one of the primary .cmnd files as a command-line input when running the script so that Pythia can perform the simulation as desired.

The two support command files are read in by the main program automatically, and they contain a variety of settings and parameters relevant to the simulation.  These include, but are not limited to, the number of events, the random seed, the tunes, and a variety of Standard Model values like particle masses.
