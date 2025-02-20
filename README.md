# PML
Parallel finite element forward modeling of 3-D magnetotelluric conductivity and permeability anisotropy with coupled PML boundary conditions

# Getting Started
## Installation
Clone  
$ git clone https://github.com/  
$ cd PML

## Configure your environment
1、You will need to install the following external libraries:  
gcc9.3.0、mpich、superlu_dist-8.0.0、petsc-3.20.5 
2、Then you need to modify the make.inc file: 
BLAS_DIR     =/Your path/openmp  
LAPACK_DIR   =/Your path/gcc9.3.0  
PARMETIS_DIR =/Your path/parmetis-4.0.3  
METIS_DIR    =/Your path/metis  
SUPERLU_DIST =/Your path/superlu_dist-8.0.0  
EIGEN_DIR     =/Your path/eigen-git-mirror-master  
PETSC_DIR    =/Your path/petsc-3.20.5  

3、Compile your code  
$ make

4、Run your code
$ sh mybatch.sh X1 X2 (X1 represents the number of nodes used at run time and X2 represents the total number of processes used at run time)  

$notice  
You need to select the mpi run command based on your environment, as shown below:  
mpiexe -n numpro(Number of processes) ./main


