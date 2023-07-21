#Workshop 25 July 2023

## MPI with Python
[200~Parallel Computing in Python using mpi4py](https://research.computing.yale.edu/sites/default/files/files/mpi4py.pdf)

### How:
$  module load anaconda3

$ conda create -n mpi mpi4py numpy scipy

$ conda init bash

Logout and login again

## Introduction to Conda for (Data) Scientists
[Link](https://carpentries-incubator.github.io/introduction-to-conda-for-data-scientists/)

### Pull Singularity

Docker: gcr.io/ris-registry-shared/cistem

#### Build Singularity image:

$ singularity pull docker://gcr.io/ris-registry-shared/cistem

#### Check Display:

$env | grep DIS

DISPLAY=localhost:11.0

#### Run programm:
$ singularity run --nv --env DISPLAY=localhost:11.0 cistem_latest.sif

Or

$ singularity exec --nv --env DISPLAY=localhost:11.0 cistem_latest.sif /usr/local/bin/cisTEM

#### For end user:
#### Check display env:

$ env | grep DISPLAY

DISPLAY=localhost:11.0

$ singularity exec --nv --env DISPLAY=localhost:11.0 /shared/software/singularity/images/cistem_latest.sif /usr/local/bin/cisTEM

