# parallel sand simulator
Implementation of a material simulator in C, user can add material and see how they interact over time.

## Dependencies
* GCC
* GNU Make
* SDL2
* CUDA
* MPI
* OPENMP
* must be on linux for the <sys/time.h>, SDL and TTF typography 
* 
## Demo
Graphical interface of the simulation

<img width="364" alt="sandsim" src="https://user-images.githubusercontent.com/80784724/153083285-99e0e162-d3ab-4130-b7ca-eee35bf88c18.png">

Top menu with the frames per second 

<img width="374" alt="menu" src="https://user-images.githubusercontent.com/80784724/153083517-486992f2-19fe-4f26-8cb8-1f14716f0cc1.png">

## Sequential version

Secuential version is based on a founded SDL implementation of a cellular automata, with the implemented logic for the sansimulation, the element rules, rendering etc..

run the makefile to compile

# OpenMp parallel version

optimiced parallel version with OpenMp.
<img width="374" alt="openMP" src="https://user-images.githubusercontent.com/80784724/153083403-7c9871f5-2bea-4562-87e4-cfaf6ddd11f0.png">

# Cuda paralell version

Functional Cuda paraller version, result are slower for this application

# MPI paralell version

OpenMPI paraller version of the logic, console simplified app that calculate the matrices but does not display, implementation was done in a 8 computers Aws cluster

to run: after all the configuration it is compiled and run with 8 nodes

mpicc sandsim.c -o sandsim
mpirun -np 8 -host nodo0,nodo1,nodo2,nodo3,nodo4,nodo5,nodo6,nodo7 ./sandsim

## Extra info

* Press spacebar to toggle between paused and unpaused.
* Press the mpuse to draw with the elements
* Press the keys to change the elemnts.
F= fire, R= rock, A= air, W= water, S= sand, H= smoke/humo...




