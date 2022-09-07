# MPI basics

### Task descrition

Solving system of linear equations using [conjugate gradient method](https://en.wikipedia.org/wiki/Conjugate_gradient_method).

System of equations was represented as a square symmetric matrix. There were two subtasks:
* Scatter the equations matrix by rows. Therefore pre-found X and a solution of the system must be copied to each MPI process.
* Scatter the equations matrix by columns. Therefore pre-found X and a solution of the system must be scattered the same way as the equations matrix.

There are three different programs:
 * sequential - the program without MPI. It was used to test perfomance of parallel programs.
 * parallel1 - the program with MPI. A variant of the program in which matrix was scattered by rows.
 * parallel2 - another the program with MPI. A variant of the program in which matrix was scattered by columns.

### Generating data

There is a small python script in repo. It is being used to generate the system of linear equations.
Run it before using the program. 

### Compilation

Sequential program was compilated with GNU C++ compiler:

```
g++ -std=c++11 -O3 *paths_to_source_files* -o a.out
```

And parallel programs were compilated using OpenMPI C++ compiler

```
mpicxx -std=c++11 -O3 *paths_to_source_files* -o a.out
```
