# A script for automatically making a C++ build environment wtihin /home, or any other folder.

This is a script for automatic setup of a build environment within the home folder. Here the two folders $HOME/opt and $HOME/shared are used as install target, and folder where files are downloaded to and compiled in.

The idea is to have a recent gcc as well as open MPI and boost version ready to build out of the home folder using

`export PATH=$HOME/opt/bin:$PATH`

`export LD_LIBRARY_PATH=$HOME/opt/lib64:$LD_LIBRARY_PATH`


This script can be used to automatically setup a uniform build environment on each node of an MPI cluster.
The network configuration as well as key exchanges however are a necessary prequisite for 
executing such C++ projects on a MPI cluster and are not (yet?) handlede in this script.

## Useage

Just specify `HOME=...`
and then after adding execution right with

  `chmod u+x make_mpi_environment	`
  
simply execute

  `./make_mpi_environment`
