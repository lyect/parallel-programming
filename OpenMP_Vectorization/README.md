### Task description

Finding inverse matrix using power series.

There was three subtasks:
1) Write a sequential program.
2) Write a program with vectorization (using SSE instructions).
3) Add threading (OpenMP) to the vectorized program. Try different scheduling strategies.

Final results of the optimizations represented in the `measurements.ods` file.

### Compilation

Sequential and vectorized programs were compiled using this command:

```
g++ -std=c++11 -O0 prog_seq.cpp -o prog_seq.out
```

Combined program (with vectorization and OpenMP) was compiled using this command:

```
g++ -std=c++11 -O0 -fopenmp prog_comb.cpp -o prog_comb.out
```

The `-O0` flag was added to get rid of the optimizations done by compiler.
